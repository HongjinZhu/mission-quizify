# Gemini Quizify

This project is an AI-powered quiz generator built using Streamlit. It leverages several custom modules to process documents, create embeddings, store data in a Chroma collection, and generate quizzes based on a specified topic. Users can ingest documents, specify a topic, and generate multiple-choice questions automatically.

## Features

- **Document Processing**: Ingests PDFs and extracts textual content.
- **Embedding Creation**: Uses a pre-trained model to generate embeddings from the document content.
- **Chroma Collection**: Stores embeddings in a Chroma database for efficient retrieval.
- **Quiz Generation**: Generates multiple-choice questions based on a specified topic.
- **Interactive Quiz Interface**: Allows users to navigate through questions and get instant feedback on their answers.

## Getting Started

### Prerequisites and Installation

**Install Dependencies**

   ```sh
   pip install -r requirements.txt
   ```

### Configuration

Update the `embed_config` dictionary in the `main.py` file with your embedding model configuration:

```python
embed_config = {
    "model_name": "textembedding-gecko@003",
    "project": "YOUR-PROJECT-ID",
    "location": "us-central1"
}
```

### Running the Streamlit Application

```sh
streamlit run main.py
```

## Usage

1. **Load Data to Chroma**
   - Select the PDFs you want to ingest.
   - Specify the topic for the quiz.
   - Choose the number of questions.
   - Click on "Submit" to generate the questions.

2. **Take the Quiz**
   - Navigate through the questions using "Next Question" and "Previous Question" buttons.
   - Select your answer and submit to get instant feedback.

## Code Overview

### Main Components

- **DocumentProcessor**: Handles the ingestion and processing of PDF documents.
- **EmbeddingClient**: Generates embeddings for the processed document content.
- **ChromaCollectionCreator**: Creates and manages the Chroma collection for storing embeddings.
- **QuizGenerator**: Generates quiz questions based on the specified topic and document content.
- **QuizManager**: Manages the display and navigation of quiz questions.

