# Attention-mechanism-visualizer

A beginner-friendly AI application that extracts text from study-note images using OCR, converts words into numerical embeddings, and visualizes attention scores using a simple scaled dot-product attention mechanism.

## Project Overview

This project combines OCR, sentence embeddings, attention mechanism, and Streamlit into one application.

A user uploads an image containing study notes. The application:

1. Extracts text from the image using Tesseract OCR.
2. Splits the extracted text into words.
3. Converts the words into numerical embeddings using Sentence Transformers.
4. Creates Query (Q), Key (K), and Value (V) representations.
5. Calculates scaled dot-product attention.
6. Displays attention scores using progress bars.
7. Identifies the word with the highest calculated attention score.

## Project Flow

```text
Image → OCR → Extract Text → Word Processing → Embeddings → Q, K, V → Attention → Visualization
```

## Technologies Used

* Python
* Streamlit
* Tesseract OCR
* Pytesseract
* Sentence Transformers
* NumPy
* Pillow

## Project Structure

```text
AI-Attention-Visualizer/
│
├── app.py
├── ocr.py
├── embedding.py
├── attention.py
└── requirements.txt
```

## File Description

| File               | Description                                                   |
| ------------------ | ------------------------------------------------------------- |
| `app.py`           | Main Streamlit application                                    |
| `ocr.py`           | Extracts text from images using Tesseract OCR                 |
| `embedding.py`     | Generates text embeddings using Sentence Transformers         |
| `attention.py`     | Calculates Query, Key, Value and scaled dot-product attention |
| `requirements.txt` | Contains the required Python packages                         |

## Features

* Upload JPG, JPEG, and PNG images
* Extract text using OCR
* Generate numerical embeddings
* Calculate Query, Key and Value
* Apply scaled dot-product attention
* Visualize word attention scores
* Identify the highest-attended word
* Simple Streamlit web interface

## Installation

### 1. Clone the Repository

```bash
git clone <your-github-repository-link>
cd AI-Attention-Visualizer
```

### 2. Install Required Packages

```bash
pip install -r requirements.txt
```

Or:

```bash
pip install streamlit numpy pillow pytesseract sentence-transformers
```

## Tesseract OCR Setup

Tesseract OCR must be installed separately on Windows.

The default path used in this project is:

```text
C:\Program Files\Tesseract-OCR\tesseract.exe
```

If Tesseract is installed in another location, update the path in `ocr.py`.

## Run the Application

Open the project folder in VS Code and run:

```bash
python -m streamlit run app.py
```

The application will open in a web browser.

## Example

The application can process an image containing text such as:

```text
Artificial Intelligence uses machine learning to analyze data.
```

The application extracts the text, generates embeddings, calculates attention scores, and displays the scores using visual progress bars.

## How It Works

```text
Image
  ↓
Tesseract OCR
  ↓
Extracted Text
  ↓
Words
  ↓
Sentence Embeddings
  ↓
Query, Key, Value
  ↓
Scaled Dot-Product Attention
  ↓
Attention Scores
  ↓
Streamlit Visualization
```

## Important Note

This project is an educational demonstration of the attention mechanism.

The Query, Key, and Value projection matrices are randomly initialized. Therefore, the highest-attention word should not be interpreted as the most important word in a semantic sense.

The project demonstrates the mechanics of applying attention to embeddings rather than reproducing the internal attention maps of a pretrained Transformer.

## Limitations

* OCR accuracy depends on image quality.
* Handwritten text may not be recognized accurately.
* Only the first 20 cleaned words are visualized.
* `all-MiniLM-L6-v2` is mainly a sentence-embedding model but is applied to individual words for educational simplicity.
* The Q, K and V projection matrices are randomly initialized.
* The highest-attention word is not necessarily the most meaningful or important word.

## Future Enhancements

* Use a Transformer model with actual token-level attention weights
* Highlight important words in the extracted text
* Highlight words directly on the original image
* Add Tamil and other language support
* Add keyword extraction
* Add topic classification
* Add a study-notes summarizer
* Add question-answering functionality
* Allow users to download an attention report

## Work pictures

<img width="705" height="821" alt="image" src="https://github.com/user-attachments/assets/67a57e9f-8e2e-4f26-a7bc-60390bc02f56" />

<img width="737" height="847" alt="image" src="https://github.com/user-attachments/assets/593f7fb5-d695-49c7-91ea-1673eebc987d" />

<img width="757" height="741" alt="image" src="https://github.com/user-attachments/assets/95c57ee2-ff14-4906-94fa-9791e1290138" />

## Learning Outcomes

Through this project, we learn:

* How OCR converts images into text
* How embeddings represent text as numerical vectors
* How Query, Key and Value work
* How scaled dot-product attention is calculated
* How attention weights can be visualized
* How Python modules can be connected
* How to build and run a Streamlit AI application

## Author

**Mythili K**

B.Sc Computer Science with Artificial Intelligence
