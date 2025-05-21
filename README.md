# Semantic Book Recommender App

This is a portfolio project demonstrating a **semantic book recommendation system** powered by LLMs and built with **Gradio**. Users can describe the type of book they're looking for in natural language, select a category and emotional tone, and receive personalized book recommendations based on semantic similarity and sentiment analysis.

## 🚀 Features

- 🔍 **Semantic Search**: Find books based on natural language queries (e.g. *"a story about children"* or *"a sad romance"*).
- 🧠 **Emotion-based Filtering**: Classify book descriptions by emotional tone using LLMs (e.g. *Happy*, *Sad*, *Suspenseful*).
- 📚 **Interactive Interface**: Clickable vertical book list that displays the selected book's cover and full description.
- ⚡ **LLM-Powered Classification**: Automatically detect and categorize genres and emotional tone using zero-shot classification.

## 🛠️ Installation

To run this app locally:

1. Clone this repository:

   ```bash
   git clone https://github.com/your-username/book-recommender.git
   cd book-recommender
   ```

2. (Optional) Create a virtual environment:

   ```bash
   python -m venv venv
   source venv/bin/activate  # or venv\Scripts\activate on Windows
   ```

3. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

4. Run the Gradio app:

   ```bash
   python gradio-dashboard.py
   ```

## 📦 Requirements

This project was developed using Python 3.11 and requires the following key packages:

- `gradio`
- `pandas`
- `transformers`
- `langchain`
- `kagglehub`
- `scikit-learn`
- `python-dotenv`
- `seaborn`, `matplotlib` (for analysis notebooks)

Full list in `requirements.txt`.

## 🔐 API Keys

Some features (like emotion classification with OpenAI, HuggingFace) may require an `.env` file in your root directory:

```
OPENAI_API_KEY=your-api-key-here

HF_API_KEY=your-hf-key-here
```

## 📊 Data

The book dataset is sourced from Kaggle and can be downloaded programmatically using `kagglehub`:

```python
import kagglehub

# Download latest version of the dataset
kagglehub.dataset_download("dylanjcastillo/7k-books-with-metadata")
```