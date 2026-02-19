#### This repository contains two end-to-end Generative AI projects built using Hugging Face Transformers and Python. These projects demonstrate practical implementation of modern NLP models for text generation and question answering tasks.

# 📌 Project 1: AI Storyteller – Text Generation using Transformer Models

## 🎯 Objective

To build a Generative AI system that creates coherent and creative stories based on user prompts using pre-trained transformer-based language models.

---

## 🧠 Model Used

* Pretrained Transformer-based Language Model (e.g., GPT-style architecture)
* Loaded using Hugging Face `pipeline("text-generation")`

---

## ⚙️ How It Works

1. Load a pretrained text generation model.
2. Accept a prompt from the user.
3. Generate a continuation of the story.
4. Control creativity using:

   * `max_length`
   * `temperature`
   * `top_k`
   * `top_p`

---

## 🧾 Example

**Input Prompt:**

```
Once upon a time in a futuristic city
```

**Generated Output:**

```
Once upon a time in a futuristic city, robots and humans lived side by side...
```

---

## 📊 Analysis

### ✅ Strengths

* Generates creative and fluent text.
* Handles open-ended prompts well.
* Produces coherent short stories.

### ⚠️ Limitations

* May sometimes generate repetitive text.
* Longer outputs may lose coherence.
* Factually incorrect content possible (hallucinations).

### 🎯 Learning Outcome

* Understanding generative language models.
* Working with decoding strategies.
* Controlling creativity vs determinism.

---

# 📌 Project 2: Ask Me Anything – Question Answering with BERT

## 🎯 Objective

To build an extractive question-answering system that returns factual answers from a given context paragraph.

---

## 🧠 Model Used

* `bert-base-cased-squad2`
* Loaded using Hugging Face `pipeline("question-answering")`
* Based on BERT architecture trained on SQuAD2 dataset

---

## ⚙️ How It Works

1. Load the Question Answering pipeline.
2. Provide a context paragraph.
3. Accept one or more questions.
4. The model extracts the most relevant answer span from the context.

---

## 🧾 Example

### Context

```
Artificial Intelligence is a branch of computer science.
Machine Learning is a subset of AI.
Python is widely used in AI development.
```

### Questions & Model Output

| Question                         | Model Answer                 | Confidence |
| -------------------------------- | ---------------------------- | ---------- |
| What is Artificial Intelligence? | A branch of computer science | 0.98       |
| What is Machine Learning?        | A subset of AI               | 0.99       |
| Which language is used in AI?    | Python                       | 0.97       |

---

## 📊 Analysis

### ✅ Strengths

* High accuracy for factual, direct questions.
* Extracts precise answer spans.
* Confidence score helps evaluate reliability.

### ⚠️ Limitations

* Cannot answer if information is not in context.
* Struggles with reasoning-based or inferential questions.
* Sensitive to poorly structured context.

### 🎯 Learning Outcome

* Understanding extractive QA systems.
* Working with contextual embeddings.
* Evaluating model confidence and performance.

---

# 🔍 Comparative Analysis: Generative vs Extractive AI

| Feature            | AI Storyteller             | Ask Me Anything                      |
| ------------------ | -------------------------- | ------------------------------------ |
| Type               | Generative AI              | Extractive QA                        |
| Output Style       | Creates new text           | Extracts from context                |
| Creativity         | High                       | None                                 |
| Accuracy           | Variable                   | High (if answer exists in context)   |
| Hallucination Risk | High                       | Very Low                             |
| Use Case           | Chatbots, content creation | Search systems, knowledge assistants |

---

# 🛠 Tech Stack

* Python
* Transformers (Hugging Face)
* PyTorch
* Jupyter Notebook

---

# 💡 Real-World Applications

### AI Storyteller

* Creative writing assistants
* Content generation
* Marketing copy generation
* Story-based games

### Ask Me Anything

* Customer support automation
* Document search systems
* FAQ bots
* Internal knowledge base systems
