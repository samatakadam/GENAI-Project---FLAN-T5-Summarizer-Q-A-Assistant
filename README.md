# 🧠 FLAN-T5 Summarizer & Q&A Assistant

This project demonstrates a **lightweight NLP assistant** built using **Google’s FLAN-T5 Small model** from Hugging Face Transformers.
It supports:

* 📄 **Text Summarization**
* ❓ **Question & Answering over a local context file**

The application runs in the terminal and is designed to be simple, educational, and easy to extend.

---

## 🚀 Features

* Uses **instruction-tuned FLAN-T5 Small** (~80M parameters)
* Generates:

* Bullet-point summaries
* Context-restricted answers
* Prevents hallucination by answering **only from provided context**
* Fully offline once the model is downloaded
* Simple command-line interface (CLI)

---

## 🛠️ Requirements

Make sure you have **Python 3.8+** installed.

### Required Python Packages

```bash
pip install transformers torch sentencepiece
```

---

## 📦 Model Used

* **Model Name:** `google/flan-t5-small`
* **Type:** Instruction-tuned Sequence-to-Sequence Transformer
* **Use Cases:** Summarization, Question Answering, Instruction Following

The model is automatically downloaded from Hugging Face on first run.

---

## 📁 Project Structure

```
.
├── main.py              # Main application code
├── context.txt          # Context file for Q&A (user-created)
├── README.md            # Project documentation
```

---

## ▶️ How to Run

From the project directory:

```bash
python main.py
```

You will see a menu like:

```
1. Summarize the data
2. Question & Answer over local context.txt
0. Exit
```

---

## 📝 Option 1: Text Summarization

1. Choose option `1`
2. Paste the text you want to summarize
3. Press **Enter on a blank line** to finish input
4. The model will generate **4–6 bullet points**

### Example

**Input:**

```
Artificial Intelligence is transforming industries...
```

**Output:**

```
- AI improves automation and efficiency
- It enhances data-driven decision making
- Widely used in healthcare, finance, and education
```

---

## ❓ Option 2: Question & Answer (Context-Based)

1. Create a file named **`context.txt`**
2. Add the content you want the model to answer from
3. Choose option `2`
4. Ask a question related to the context

⚠️ If the answer is not found in the context, the model will reply:

```
Not found.
```

This ensures **safe and grounded answers**.

---

## 📄 Example `context.txt`

```
Python is a high-level programming language.
It is widely used in data science and web development.
```

**Question:**

```
Where is Python commonly used?
```

**Answer:**

```
Python is commonly used in data science and web development.
```

---

## ⚙️ Customization

You can modify:

* `max_new_tokens` → control output length
* `temperature` → creativity level
* `top_p` → nucleus sampling
* Prompts → behavior tuning

---

## 🎯 Educational Use

This project is ideal for:

* Learning Hugging Face Transformers
* Understanding instruction-tuned models
* Building NLP CLI tools
* Summarization & Q&A experiments

---



## ✨ Author

"Samata Kadam"
*Marvellous FLAN-T5 Summarizer & Q&A Assistant*

