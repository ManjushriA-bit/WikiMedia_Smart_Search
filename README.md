# 🎯 WikiQuiz — Wikimedia-Powered Interactive Quiz

> Turn Wikimedia content into an interactive learning experience.

WikiQuiz is a Challenge 1 prototype built using the **Wikimedia Structured Wikipedia Dataset**. The application lets a user search for a topic, select an article, extract information from the article, generate quiz questions, answer them, and receive a final score.

## 🚀 Challenge 1 — WikiQuiz

The prototype follows the required flow:

```text
Search / Select Topic
        ↓
Retrieve Wikimedia Article
        ↓
Extract Information
        ↓
Generate Questions
        ↓
Answer Questions
        ↓
Check Answers
        ↓
Calculate Score
        ↓
Display Result
```

### Core requirements implemented

- 🔎 Search/select a Wikipedia topic
- 📖 Retrieve a relevant article from the Wikimedia dataset
- 🧠 Extract available article information
- ❓ Generate quiz questions from extracted information
- 🔘 Multiple-choice questions
- ☑️ True/False questions
- ✅ Answer validation
- 📊 Score and percentage calculation
- 💡 Answer explanations
- 🏆 Final quiz result

## 🧠 How It Works

### 1. Topic Search

The user enters a topic such as `Football` or `Basketball`. The system searches article titles available in the loaded Wikimedia dataset.

### 2. Article Selection

Matching articles are displayed and the user selects one article. The selected dataset row is then used as the source for the quiz.

### 3. Information Extraction

The prototype works with information available in the selected dataset, including fields such as:

```text
name
description
abstract
sections
infoboxes
references
tables
url
```

For the current prototype, the main quiz-generation logic uses the article title, description and abstract, while extracting factual information such as years, locations, sports and factual statements where available.

### 4. Question Generation

Questions are generated programmatically from information found in the selected article. The prototype avoids presenting unsupported article facts as quiz answers.

Supported formats:

- Multiple Choice Questions (MCQ)
- True / False

### 5. Scoring

The selected answer is checked against the generated answer. The application calculates the final score and percentage and displays feedback.

## 🏗️ System Architecture

```text
                 USER
                   │
                   ▼
          ┌─────────────────┐
          │   Topic Search  │
          └────────┬────────┘
                   │
                   ▼
          ┌─────────────────┐
          │ Wikimedia       │
          │ Structured Data │
          └────────┬────────┘
                   │
                   ▼
          ┌─────────────────┐
          │ Article Select  │
          └────────┬────────┘
                   │
                   ▼
          ┌─────────────────┐
          │ Information     │
          │ Extraction      │
          └────────┬────────┘
                   │
                   ▼
          ┌─────────────────┐
          │ Question        │
          │ Generation      │
          └────────┬────────┘
                   │
                   ▼
          ┌─────────────────┐
          │ Quiz & Answers  │
          └────────┬────────┘
                   │
                   ▼
          ┌─────────────────┐
          │ Score Engine    │
          └────────┬────────┘
                   │
                   ▼
          ┌─────────────────┐
          │ Final Result    │
          └─────────────────┘
```

## 💻 Technology Stack

| Technology | Purpose |
|---|---|
| Python | Core application logic |
| Pandas | Dataset processing |
| PyArrow | Parquet support |
| KaggleHub | Dataset access |
| Google Colab | Development and testing |
| Wikimedia Structured Contents | Source dataset |

## 📊 Dataset

The prototype uses the **Wikipedia Structured Contents** dataset. A single Parquet file from the dataset was used during development rather than downloading the complete dataset.

The loaded development file contains **25,000 articles and 19 columns**.

The project does **not** store the large Wikimedia dataset inside this repository.

## 🔗 Working Notebook

The current development notebook is available here:

**[Open WikiQuiz in Google Colab](https://colab.research.google.com/drive/1LyiTgwznT0XThpcEdf-zd2_y0ez6641)**

## 📸 Prototype

The prototype demonstrates the complete Challenge 1 pipeline from topic search to final score.

Screenshots can be added to the `screenshots/` folder as the visual evidence for:

1. Dataset loaded
2. Topic search
3. Article selection
4. Quiz generation
5. Final result

## 🧪 Example

Example topic:

```text
Football
```

Example selected article:

```text
Avelino Lopes (footballer)
```

Example generated question:

```text
Which sport is mentioned in the article?

1. Basketball
2. Swimming
3. Hockey
4. Football
```

The user receives immediate feedback and a final score after completing the generated quiz.

## 📁 Project Structure

```text
WikiMedia_Smart_Search/
│
├── README.md
│
├── notebooks/
│   └── Challenge_1_WikiQuiz.ipynb
│
├── screenshots/
│   ├── 01_dataset_loaded.png
│   ├── 02_topic_search.png
│   ├── 03_article_selected.png
│   ├── 04_quiz_generated.png
│   └── 05_final_result.png
│
├── requirements.txt
│
└── .gitignore
```

## 🌱 Future Improvements

Possible extensions include:

- Difficulty levels
- Timed quizzes
- Random question selection
- Score history
- Leaderboards
- Multiple rounds
- Topic categories
- Improved question generation
- Interactive web interface

## 📌 Project Status

**Challenge 1 — Core Prototype: Completed ✅**

The current prototype demonstrates the basic WikiQuiz workflow using information available from the Wikimedia dataset.

---

### Challenge Context

Developed as part of the Wikimedia Structured Wikipedia Dataset hands-on challenge.

**Challenge:** Challenge 1 — WikiQuiz  
**Language:** Python  
**Environment:** Google Colab  
**Dataset:** Wikimedia Structured Wikipedia Dataset
