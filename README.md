# 🎯 WikiQuiz — Challenge 1

> **Wikimedia Structured Wikipedia Dataset Hands-on Project**

This repository contains the **Challenge 1 — WikiQuiz** prototype built using Wikimedia's Structured Wikipedia Dataset.

## 🧩 Problem Statement

Wikipedia contains a large amount of educational information. The challenge is to convert that information into an interactive quiz experience where users can search for a topic, select an article, answer questions, and receive a score.

## 🔄 Expected Flow

```text
Search / Select Topic
        ↓
Retrieve Article
        ↓
Extract Information
        ↓
Generate Questions
        ↓
Answer Questions
        ↓
Calculate Score
        ↓
Display Result
```

## ✅ Implemented Features

- Search for a Wikipedia topic
- Display matching articles from the dataset
- Select an article
- Retrieve article title, description and abstract
- Generate quiz questions from available article information
- Multiple-choice questions
- True/False questions
- Randomized question/option order where supported
- Answer validation
- Immediate correct/incorrect feedback
- Answer explanations
- Score calculation
- Final percentage/result
- Handling for empty searches, no matching articles and invalid selections

## 🧪 Demonstrated Dataset

The notebook uses the Wikimedia Structured Wikipedia Dataset through KaggleHub.

```text
dataset: wikimedia-foundation/wikipedia-structured-contents
shard: enwiki/data/enwiki_namespace_0_00008.parquet
```

The loaded shard contains **25,000 rows and 19 columns** in the demonstrated run.

## 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| Python | Quiz logic and processing |
| Pandas | Dataset loading and filtering |
| Regex | Extracting years, locations and text patterns |
| KaggleHub | Accessing the Wikimedia dataset |
| Google Colab | Development and execution |

## 📓 Notebook

The main project notebook is:

**`WikiQuiz(2).ipynb`**

It contains the Challenge 1 implementation, dataset exploration, article search/selection, information extraction, quiz generation, answer checking and final scoring flow.

## 📸 Example Test

One demonstrated run searches for a topic related to **Basketball**, selects an article from the returned dataset results, generates questions, accepts user answers and produces a final score.

The notebook also demonstrates another article search and a generated quiz with explanations and final scoring.

## 📁 Project Structure

```text
WikiMedia_Smart_Search/
├── README.md
├── requirements.txt
└── WikiQuiz(2).ipynb
```

## ▶️ How to Run

1. Open `WikiQuiz(2).ipynb` in Google Colab or Jupyter.
2. Install the dependencies from `requirements.txt`.
3. Run the dataset-loading cells.
4. Enter a Wikipedia topic when prompted.
5. Select an article from the displayed results.
6. Answer the generated questions.
7. View the final score and feedback.

## 📌 Challenge Requirements Covered

Challenge 1 requires topic search/selection, article retrieval from the dataset, question generation from article information, MCQ and/or True/False questions, answer submission and checking, score calculation, and a final result. This repository is organized around those requirements.

## 🌱 Optional Extensions

Possible extensions include difficulty levels, a timer, random questions, score history, a leaderboard, answer explanations, quiz categories, multiple quiz rounds and AI-assisted question generation.

## 📌 Status

**Challenge 1 — WikiQuiz: Prototype completed ✅**

Built for the **Wikimedia Structured Wikipedia Dataset hands-on project**.
