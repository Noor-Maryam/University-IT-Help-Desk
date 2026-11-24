
# University IT Help Desk Assistant

## 1. Project Overview
This project classifies student IT support tickets into 10 predefined categories.

## 2. Categories
1. Login & Account Access
2. Wi-Fi & Network
3. Software Installation
4. Hardware Problem
5. Email Issue
6. LMS & Portal Issue
7. Printer Issue
8. Data & File Access
9. Security & Phishing
10. General IT Support

## 3. Dataset
The project uses 100 fictional student support tickets:
- 80 development tickets
- 20 evaluation tickets

## 4. Classification Methods
Two methods were evaluated:

- Keyword Baseline: Uses predefined keywords and rules.
- TF-IDF: Uses text similarity and cosine similarity.

## 5. Evaluation Results

| Method | Accuracy | Correct | Incorrect |
|---|---:|---:|---:|
| Keyword Baseline | 85% | 17 | 3 |
| TF-IDF | 75% | 15 | 5 |

## 6. Prompt Engineering
Two prompts, V1 and V2, were designed.
They specify category selection and one-sentence summaries.
No external language model was connected, so the prompts were compared by design rather than actual model performance.

## 7. Validation
Pydantic validates:
- Category membership
- Summary length
- Response structure

Invalid categories and short summaries were tested.

## 8. Backend
FastAPI provides a POST endpoint:

`/analyze`

It accepts ticket text and returns a category and summary.

## 9. Frontend
Gradio provides a user interface for submitting tickets and viewing results.

## 10. Limitations
- Classification uses keyword rules, not a trained machine-learning classifier.
- Summaries use a template, not AI-generated summarization.
- The Gradio classroom demo uses an in-process API client.
- The public Gradio share link is temporary.

## 11. Technologies
- Python
- Google Colab
- Pandas
- Scikit-learn
- Pydantic
- FastAPI
- Gradio
