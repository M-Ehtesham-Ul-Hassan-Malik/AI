# Transformers

## What Are Transformers?
A **Transformer** is a deep learning model that processes entire sequences (like sentences) at once using a technique called **self-attention**, allowing it to focus on different words and understand context better than older models like RNNs.

## Problem Before Transformers

Before Transformers, models like **RNN**  and **LSTM** were used for processing the sequences like sentences.
But they had their limitations with them:
- Could not process all the words in a sentence at once(had to go one by one).

- Hard to remember the **Long-Distance Words**(like start and end of a sentence).

## Transformer Architecture
Introduced in the 2017 paper [**“Attention is All You Need”**](https://arxiv.org/abs/1706.03762) by Vaswani et al., the Transformer is designed for sequence modeling and it is especially useful in NLP tasks like translation, summarization, and text generation.

### Transformer: High-Level Structure
A Transformer has two main components:

| Encoder (like BERT)    | Decoder (like GPT)     |
| ---------------------- | ---------------------- |
| Reads the input        | Generates the output   |
| Good for understanding | Good for generating    |

But in many cases (like BERT or GPT), we use only one side.

### Self-Attention (The Heart of Transformers)
Let’s say the sentence is:

“`The cat sat on the mat.`”

When understanding the word "**cat**", the model also looks at other words like "**sat**" or "**mat**" to understand the context.
Self-attention lets each word "**attend**" to every other word.

### Transformer Building Blocks
| Block                    | Role                                                          |
| ------------------------ | ------------------------------------------------------------- |
| **Embedding**            | Turns words into vectors                                      |
| **Positional Encoding**  | Adds position info (since Transformers don't go word-by-word) |
| **Multi-Head Attention** | Focuses on different relationships in the sentence            |
| **Feed-Forward Layer**   | Processes the attention output                                |
| **Layer Normalization**  | Stabilizes learning                                           |
| **Residual Connections** | Helps prevent loss of information during deep stacking        |


### Example: Why Attention Matters
**Sentence**:
`“The animal didn’t cross the street because it was too tired.”`

What does **“it”** refer to?
The Transformer attends to **“animal”** and figures out the connection.

## BERT – Bidirectional Encoder Representations from Transformers
- BERT is for understanding text
- BERT is **Bi-directional**, it looks at both left and right context at the same time. 

### How BERT Works:
- Uses only the Encoder part of the Transformer.
- Trained using the Masked Language Modeling:
    - “The cat sat on the **[MASK]**” → predict **“mat”**
- Also uses Next Sentence Prediction:
    - “Q: Where is the cat?” → “A: On the mat.”

### BERT Use Cases
- Text classification
- Sentiment analysis
- Named entity recognition
- Question answering 

## GPT – Generative Pretrained Transformer
- GPT is for generating text
- GPT is **Uni-directional** , it looks at left context only.

### How GPT Works

- Uses only the Decoder part of Transformer.
- Trained using causal (left-to-right) language modeling:
    - “The cat sat on the” → predict **“mat”**

### GPT Use Cases
- Text generation
- Chatbots (like ChatGPT!)
- Story and code writing
- Translation


## What's the difference between BERT and GPT?
| Feature        | BERT                   | GPT                            |
| -------------- | ---------------------- | ------------------------------ |
| **Architecture**   | Encoder-only           | Decoder-only                   |
| **Direction**      | Bidirectional          | Unidirectional (left-to-right) |
| **Use case**       | Understanding tasks    | Text generation tasks          |
| **Training style** | Masked words (MLM)     | Predict next word              |
| **Example task**   | Sentiment analysis, QA | Chatbot, story writing         |


## Analogy
Imagine you’re reading a mystery book:

- **BERT** reads the entire paragraph to understand the story (like a detective).
- **GPT** writes the next part of the story based on what’s already written (like a novelist).


## Ending Notes
The **Transformer** is an attention-based deep learning architecture that replaces recurrence with self-attention, allowing parallel processing of sequences. It has two parts an encoder and a decoder. Each part consists of multiple layers with multi-head attention, feed-forward networks, and positional encoding. It's the foundation of modern NLP models like BERT and GPT and many others and are the foundation of systems like **ChatGPT**, **Bard**, and **Claude**.



