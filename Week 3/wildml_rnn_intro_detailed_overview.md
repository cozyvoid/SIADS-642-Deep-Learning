# Detailed Overview: *Recurrent Neural Networks Tutorial, Part 1 – Introduction to RNNs*

**Source article:** Denny Britz, “Recurrent Neural Networks Tutorial, Part 1 – Introduction to RNNs”  
**Archived URL:** Wayback Machine capture of the WildML post

---

## 1. Central purpose of the article

This article is an introductory tutorial on **recurrent neural networks (RNNs)**, aimed at readers who already have some familiarity with basic neural networks and want to understand how RNNs work, why they matter, and what kinds of problems they solve.

The author frames the post as the first part of a larger tutorial series covering four steps:

1. Introduction to RNNs  
2. Implementing an RNN in Python and Theano  
3. Backpropagation Through Time (BPTT) and the vanishing gradient problem  
4. Implementing GRU/LSTM variants  

The tutorial series is built around implementing a **recurrent neural network language model**, which can both score sentences by likelihood and generate new text.

---

## 2. Article structure

The article is organized into five main conceptual sections:

1. **What are RNNs?**
2. **What can RNNs do?**
3. **Training RNNs**
4. **RNN Extensions**
5. **Conclusion**

It is written as a conceptual primer rather than a math-heavy derivation.

---

## 3. What RNNs are

### 3.1 The core idea: using sequential information

The article defines RNNs as models designed to handle **sequential data**, where the current input or output depends on what came before. This is contrasted with traditional feedforward neural networks, which typically assume that inputs and outputs are independent of one another.

That assumption fails in many real tasks. The author gives a direct example:
- if you want to predict the next word in a sentence, you need the previous words.

This is the central motivation for RNNs: they are built to model **dependence across time steps**.

### 3.2 Why they are called “recurrent”

RNNs are called recurrent because the same computational operation is applied repeatedly across the elements of a sequence. At each time step:
- the network takes the current input,
- combines it with information from prior steps,
- and produces an updated hidden representation and possibly an output.

### 3.3 Hidden state as memory

The article emphasizes that the hidden state acts like a **memory**:
- it stores information about what the network has processed so far,
- and it allows later outputs to depend on earlier inputs.

### 3.4 Practical limitation of vanilla RNN memory

The article makes an important distinction between theory and practice:
- **in theory**, RNNs can use information from arbitrarily long sequences,
- **in practice**, vanilla RNNs typically only look back a limited number of steps effectively.

---

## 4. Unrolling an RNN through time

A core explanatory device in the article is the idea of **unrolling** or **unfolding** the RNN.

### 4.1 What unrolling means
Unrolling means writing out the repeated computation as if it were a deep network over time:
- one copy of the same recurrent cell for each time step in the sequence.

### 4.2 Why unrolling matters conceptually
This view makes it easier to understand:
- how information flows from earlier to later positions,
- why gradients need to be propagated backward through multiple steps during training,
- and how one set of parameters is reused across all positions.

---

## 5. Main components of the vanilla RNN

The article introduces three main quantities at each time step:

### 5.1 Input \(x_t\)
The input at time step \(t\).  
For language tasks, this might be a word representation such as a **one-hot vector**.

### 5.2 Hidden state \(s_t\)
The hidden state at time step \(t\), which serves as the model’s memory.

The hidden state is computed from the current input and the previous hidden state, usually with a nonlinearity such as **tanh** or **ReLU**. The initial previous state is typically set to zeros.

### 5.3 Output \(o_t\)
The output at time step \(t\).  
In a language model, this output is often a probability distribution over the vocabulary, typically formed by applying **softmax** to a transformed hidden state.

---

## 6. The role of the parameter matrices

The article describes three parameter matrices:

- **U**: input-to-hidden parameters  
- **W**: hidden-to-hidden recurrent parameters  
- **V**: hidden-to-output parameters  

A major design property of RNNs is that the same parameters are used at every time step.

This:
- reflects the idea that the same type of computation is performed at each step,
- reduces the total number of parameters,
- allows the model to generalize across sequence positions.

---

## 7. Important notes the article makes about RNN behavior

### 7.1 Output is based on memory
At each step, output is computed from the hidden state, which summarizes past information.

### 7.2 Memory is imperfect in practice
Although the hidden state is intended to summarize all prior time steps, it often cannot retain distant information well in vanilla RNNs.

### 7.3 Outputs are task-dependent
Not every RNN problem needs an output at every time step.

The article points out:
- some tasks only need the **final output**,
- others need **outputs at every step**.

---

## 8. What RNNs can do

The article’s next major section surveys applications, especially in **natural language processing**.

The author also notes that the most commonly used RNNs in practice are often **LSTMs**, because they handle long-term dependencies better than vanilla RNNs.

---

## 9. Application 1: Language modeling and text generation

This is the article’s main running example.

### 9.1 Language modeling objective
Given previous words, predict the probability distribution for the next word.

### 9.2 Why this matters
Language models help:
- score sentence likelihood,
- support systems like machine translation,
- and generate text by sampling from the next-word probabilities.

### 9.3 Generative aspect
Because the model predicts the next token repeatedly, it can also generate novel text.

### 9.4 Training target in this setup
For language modeling:
- the input is the current sequence prefix,
- the target at step \(t\) is the actual next word.

---

## 10. Application 2: Machine translation

The article explains machine translation as a sequence-to-sequence problem.

### 10.1 Input and output
- input = source-language word sequence,
- output = target-language word sequence.

### 10.2 Key difference from language modeling
In machine translation, the output sequence may begin only after the full input has been processed, because early translated words may depend on the meaning of the whole source sentence.

---

## 11. Application 3: Speech recognition

The article briefly describes speech recognition as another sequence problem.

- input = acoustic signal sequence,
- output = sequence of phonetic segments with associated probabilities.

This example shows that RNNs are a general tool for temporal and ordered data, not only text.

---

## 12. Application 4: Generating image descriptions

The article also discusses image captioning.

### Main idea
RNNs can be combined with **convolutional neural networks (CNNs)** to generate captions for images.

This shows that:
- RNNs can generate output sequences conditioned on non-sequential inputs,
- and they can be part of a multimodal system.

---

## 13. Training RNNs

### 13.1 Similarity to ordinary neural network training
The author says training an RNN is similar to training a standard neural network:
- use backpropagation to compute gradients,
- then update parameters.

### 13.2 The key twist: shared parameters across time
Because the same parameters are reused at every time step, the gradient at one output depends not only on the current step, but also on earlier steps that influenced the hidden state.

### 13.3 Backpropagation Through Time (BPTT)
This leads to **Backpropagation Through Time**:
- the RNN is unrolled,
- gradients are propagated backward through the time-unfolded network,
- and gradient contributions from multiple time steps are accumulated.

---

## 14. Vanishing and exploding gradients

The article introduces one of the main technical problems of vanilla RNNs.

### 14.1 The issue
When training with BPTT, gradients passed backward across many time steps can:
- shrink toward zero (**vanishing gradients**),
- or grow too large (**exploding gradients**).

### 14.2 Consequence
Vanilla RNNs struggle to learn **long-term dependencies**, meaning relationships between sequence elements that are far apart.

### 14.3 Preview of solutions
The article signals that there are methods to mitigate these problems, and that architectures such as **LSTMs** were designed specifically to address them.

---

## 15. RNN extensions

The article closes the technical discussion with a short taxonomy of more sophisticated recurrent architectures.

---

## 16. Bidirectional RNNs

### 16.1 Motivation
Sometimes the right prediction at time \(t\) depends not only on the past, but also on the future.

Example:
- predicting a missing word can require both left and right context.

### 16.2 Architecture idea
A bidirectional RNN uses:
- one RNN reading the sequence forward,
- another reading it backward.

Their hidden states are combined to produce the output.

---

## 17. Deep bidirectional RNNs

### 17.1 What changes
The article then mentions **deep** bidirectional RNNs:
- multiple layers per time step,
- stacked recurrent processing.

### 17.2 Main tradeoff
This increases learning capacity, but also increases the need for more data and training complexity.

---

## 18. LSTM networks

This is the most important extension highlighted in the article.

### 18.1 Why LSTMs are popular
The author says LSTMs are widely used because they handle long-term dependencies much better than vanilla RNNs.

### 18.2 Architectural relationship to vanilla RNNs
LSTMs preserve the broad recurrent idea, but change how hidden state and memory are computed.

### 18.3 Cells and memory control
LSTMs use memory cells that take:
- the previous state,
- and the current input,

and internally decide:
- what to keep,
- what to forget,
- and how to combine previous memory with new information.

---

## 19. The tutorial’s pedagogical strategy

One of the article’s strengths is how it stages learning.

### 19.1 Start simple
The author starts with vanilla RNNs rather than immediately jumping to LSTMs.

### 19.2 Build progressively
The series is designed to move from:
- basic concepts,
- to implementation,
- to training mechanics,
- to more advanced recurrent architectures.

### 19.3 Application-driven teaching
The tutorial stays grounded in a concrete use case:
- building a language model.

---

## 20. Key subtopics to remember

### Conceptual subtopics
- sequential dependence
- hidden state as memory
- unrolling through time
- parameter sharing across time steps
- variable input/output sequence structure

### Mathematical / architectural subtopics
- input \(x_t\)
- hidden state \(s_t\)
- output \(o_t\)
- matrices \(U, W, V\)
- nonlinear update function such as tanh or ReLU
- softmax output

### Training subtopics
- Backpropagation Through Time
- shared-parameter gradient accumulation
- vanishing gradients
- exploding gradients
- long-term dependency challenges

### Model extension subtopics
- bidirectional RNNs
- deep bidirectional RNNs
- LSTMs
- improved hidden-state computation for long-range memory

### Application subtopics
- language modeling
- text generation
- machine translation
- speech recognition
- image captioning

---

## 21. Main takeaways

1. **RNNs are designed for sequential data**, unlike feedforward networks that assume independent inputs and outputs.
2. **The hidden state is the core mechanism** that lets the network carry information from earlier time steps forward.
3. **The same parameters are shared across all time steps**, which both defines the recurrent structure and reduces parameter count.
4. **RNNs can produce outputs at each step or only at the end**, depending on the task.
5. **Language modeling is the tutorial’s main example**, because it clearly illustrates next-step prediction and text generation.
6. **Training requires Backpropagation Through Time**, since outputs depend on chained recurrent computations across earlier steps.
7. **Vanilla RNNs struggle with long-term dependencies** because of vanishing and exploding gradient problems.
8. **LSTMs and related variants were developed to address those limitations** while keeping the basic recurrent modeling idea.

---

## 22. Study-guide summary

This article introduces recurrent neural networks as models for sequential data, where current predictions depend on earlier inputs. The core idea is that an RNN maintains a hidden state that functions as memory, updating that state at each time step using the current input and the previous hidden state. The same parameters are reused across all time steps, which distinguishes RNNs from ordinary feedforward networks and allows them to handle variable-length sequences efficiently. The article explains major RNN use cases including language modeling, text generation, machine translation, speech recognition, and image captioning. It also introduces the training procedure, Backpropagation Through Time, and explains why vanilla RNNs have trouble learning long-range dependencies due to vanishing and exploding gradients. Finally, it previews more advanced extensions such as bidirectional RNNs, deep recurrent models, and LSTMs, with LSTMs highlighted as especially effective for capturing longer-term context.

---

## 23. Good review questions

1. Why are feedforward neural networks a poor fit for many sequence tasks?
2. What does the hidden state represent in an RNN?
3. What does it mean to “unroll” an RNN through time?
4. Why does parameter sharing matter in recurrent models?
5. How does a language-modeling RNN define its training target at each time step?
6. Why might machine translation need the full input sequence before output begins?
7. What is Backpropagation Through Time, and why is it needed?
8. What are vanishing and exploding gradients?
9. Why do these gradient problems make long-term dependencies hard to learn?
10. How do bidirectional RNNs differ from standard RNNs?
11. What problem are LSTMs designed to solve?
12. Why does the tutorial start with vanilla RNNs before moving to LSTMs?

---

## 24. Bottom line

This article is a conceptual introduction to recurrent neural networks that explains their defining architecture, their role in sequence modeling, their main application areas, and their major training difficulty. Its main contribution is giving an intuitive foundation: RNNs are neural networks with memory, created to model ordered data where past context matters. From there, the tutorial prepares the reader for implementation details, gradient-based training across time, and more powerful recurrent variants such as LSTMs.
