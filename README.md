
Built by https://www.blackbox.ai

---

```markdown
# MemoryMesh - Resume & Quiz Generator

## Project Overview
MemoryMesh is a Python-based tool designed to analyze documents and extract useful information, generating concise summaries and quizzes. Users can upload PDF, PPTX, or TXT files, and the application utilizes the DeepSeek API for advanced content analysis. It aims to enhance the learning process through structured summaries and interactive quizzes, while also tracking retention metrics based on user performance.

## Installation

To run MemoryMesh, ensure you have Python installed on your machine. Then, follow these steps to set up the environment:

1. Clone the repository or download the source code:
   ```bash
   git clone <repository-url>
   cd <repository-dir>
   ```

2. Install the required Python packages:
   ```bash
   pip install requests PyPDF2 python-pptx fpdf
   ```

3. Set up your OpenRouter API key in the script:
   Replace the `API_KEY` in `testV2.py` with your actual API key.

## Usage

To use MemoryMesh, follow these instructions:

1. Run the script:
   ```bash
   python testV2.py
   ```

2. You will be prompted to choose what you want to do:
   - **1**: Generate a Summary
   - **2**: Generate a Quiz
   - **3**: Generate both a Summary and Quiz

3. Enter the path to the document you wish to analyze (supports PDF, PPTX, or TXT formats).

4. After processing, the results will be saved in both TXT and PDF formats, and you will receive interactive quiz questions if you choose the quiz option.

## Features
- **Multi-Format Support**: Analyze documents in PDF, PPTX, and TXT formats.
- **Dynamic Summaries**: Automatically generate concise summaries of documents.
- **Interactive Quiz Generation**: Create quizzes from the extracted content, including multiple-choice questions and true/false questions.
- **Retention Metrics**: Assess performance and track learning through detailed metrics such as score, average time taken, and next review reminders.

## Dependencies
MemoryMesh requires the following Python libraries, which can be installed via `pip`:
- `requests`
- `PyPDF2`
- `python-pptx`
- `fpdf`

Ensure that your Python environment has these dependencies installed for the application to function correctly.

## Project Structure
The main structure of the project is as follows:

```
/MemoryMesh
  ├── testV2.py            # Main script to run the analyzer and quiz
  ├── requirements.txt      # Optional: List of required libraries (if needed)
```

### Important Classes and Functions
- **SmartPDF**: A custom class extending `FPDF` to format PDF output.
- **extract_text(file_path)**: Extracts text from different document formats.
- **analyze_content(text, action)**: Interfaces with the DeepSeek API to summarize or generate quizzes.
- **present_quiz(quiz_data)**: Displays and evaluates an interactive quiz session.
- **calculate_retention_metrics(quiz_results, total_time)**: Computes learning metrics based on quiz results.

## Conclusion
MemoryMesh leverages advanced content analysis to enhance learning through structured summaries and quizzes. It's a versatile tool for students, educators, and anyone looking to deepen their understanding of various topics through engaged learning.
```