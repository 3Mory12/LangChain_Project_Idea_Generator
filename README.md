# LangChain App Idea Generator 💡

An AI-powered **app idea generator** built with **LangChain** and **Mistral-Nemo-Instruct**.

The project takes a topic as input and uses a sequence of LangChain chains to generate a creative app idea, its top features, and a catchy tagline.

## 🚀 Project Workflow

```text
Topic
  ↓
App Idea Generation
  ↓
Feature Generation
  ↓
Tagline Generation
  ↓
Final Output
```

For example:

```text
Topic: Football

        ↓

App Idea:
A football-focused app for tracking matches and discovering players.

        ↓

Features:
• Live match tracking
• Player statistics
• Team updates

        ↓

Tagline:
"Everything Football, All in One Place."
```

## 🛠️ Technologies Used

* Python
* LangChain
* Hugging Face Transformers
* Hugging Face Hub
* Mistral-Nemo-Instruct-2407
* PyTorch

## 🧠 LangChain Components

The project uses multiple `LLMChain` instances, where each chain performs a specific task.

### 1. Idea Chain

Takes the user's topic and generates a creative application idea.

```text
Topic → App Idea
```

### 2. Feature Chain

Takes the generated app idea and produces its top 3 features.

```text
App Idea → Features
```

### 3. Tagline Chain

Uses the app idea and generated features to create a short, catchy tagline.

```text
App Idea + Features → Tagline
```

## 🤖 Language Model

The project uses:

```text
mistralai/Mistral-Nemo-Instruct-2407
```

The model is loaded using Hugging Face Transformers and used as a custom LangChain LLM.

## 📂 Project Structure

```text
langchain-app-idea-generator/
│
├── langchain_app_idea_generator.ipynb
└── README.md
```

## ⚙️ Installation

Install the required packages:

```bash
pip install -U transformers==4.52.4 langchain-classic huggingface_hub
```

You also need to authenticate with Hugging Face:

```python
from huggingface_hub import login

login()
```

## ▶️ Usage

Run the pipeline by providing a topic:

```python
run_all("Football")
```

You can use different topics, for example:

```python
run_all("Healthcare")
run_all("Education")
run_all("Travel")
run_all("Programming")
```

The system will generate:

1. An app idea
2. Three main features
3. A catchy tagline

## 🎯 Learning Objectives

This project demonstrates how to:

* Build custom LLM integrations with LangChain
* Use Hugging Face models with LangChain
* Create and use `PromptTemplate`
* Build multiple LLM chains
* Pass the output of one chain into another
* Create a simple sequential AI workflow
* Generate structured creative content using an LLM

## 🔮 Future Improvements

* Add a web interface using Gradio or Streamlit
* Generate more detailed project descriptions
* Add technology stack recommendations
* Generate target audience and business models
* Add project difficulty levels
* Replace the deprecated `LLMChain` approach with modern LangChain Runnable pipelines

## 👨‍💻 Author

**Omar Ayman**

Computer Science Student | AI/ML Enthusiast
