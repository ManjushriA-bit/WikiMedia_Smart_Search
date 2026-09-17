# 🎯 WikiMedia Smart Search — Challenge 1

> **Wikimedia Structured Wikipedia Dataset — WikiQuiz Prototype**

This repository contains the **Challenge 1 — WikiQuiz** prototype developed using the Wikimedia Structured Wikipedia Dataset.

## 🧩 Challenge 1 — WikiQuiz

WikiQuiz lets a user search for a Wikipedia topic, select an article, generate quiz questions from the available article information, answer the questions, and receive a final score.

### Challenge Flow

```text
Search Topic → Select Article → Retrieve Information → Generate Questions → Answer → Check → Score → Result
```

## ✅ Core Requirements Implemented

- 🔎 Search/select a Wikipedia topic
- 📖 Retrieve article information from the dataset
- 📝 Generate quiz questions from article information
- 🔢 Multiple-choice questions
- ☑️ True/False questions
- ✅ Check submitted answers
- 📊 Calculate score and percentage
- 🏁 Display final result
- ⚠️ Handle empty or invalid input

## 🧠 How It Works

1. Load the Wikimedia Structured Wikipedia Dataset into Pandas.
2. Search article titles using the user's topic.
3. Display matching articles and allow the user to select one.
4. Retrieve the selected article's title, description and abstract.
5. Generate quiz questions using information available in the selected article.
6. Accept answers, check them against the correct answers, and calculate the final score.

## 🧪 Demonstrated Test

**Search:** `Basketball`

**Selected article:** `Basketball at the 1991 SEA Games`

**Documented result:** `4/5 — 80%`

## 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| Python | Quiz logic and application flow |
| Pandas | Dataset processing |
| Regex | Extracting article information |
| KaggleHub | Wikimedia dataset access |
| Google Colab | Development and testing |

## 📊 Dataset

The project uses the **Wikimedia Structured Wikipedia Dataset** available through Kaggle.

The following Parquet shard was used during development:

```text
enwiki/data/enwiki_namespace_0_00008.parquet
```

The loaded shard contains **25,000 articles and 19 columns**. The dataset itself is not stored in this repository.

## 📓 Notebook

**[Open Challenge 1 — WikiQuiz notebook](notebooks/Challenge_1_WikiQuiz.ipynb)**

The notebook contains the implementation for dataset loading, topic search, article selection, quiz generation, answer checking, scoring, and documented test output.

## 📸 Output Evidence

The `screenshots/` folder contains the documented output evidence for the Challenge 1 flow:

| Step | Evidence |
|---|---|
| Dataset loaded | `screenshots/01_dataset_loaded.svg` |
| Topic search | `screenshots/02_topic_search.svg` |
| Article selected | `screenshots/03_article_selected.svg` |
| Quiz generated | `screenshots/04_quiz_generated.svg` |
| Final result | `screenshots/05_final_result.svg` |

## 📁 Project Structure

```text
WikiMedia_Smart_Search/
│
├── README.md
├── requirements.txt
├── .gitignore
│
├── notebooks/
│   └── Challenge_1_WikiQuiz.ipynb
│
└── screenshots/
    ├── 01_dataset_loaded.svg
    ├── 02_topic_search.svg
    ├── 03_article_selected.svg
    ├── 04_quiz_generated.svg
    ├── 05_final_result.svg
    └── README.md
```

## 🔬 Testing

The prototype was tested using the `Basketball` topic and the selected article `Basketball at the 1991 SEA Games`.

The implementation also includes handling for:

- Empty topic input
- No matching articles
- Invalid article selection
- Different searchable topics

## 🌱 Future Improvements

Possible optional extensions include difficulty levels, a timer, randomized quizzes, quiz history, a leaderboard, explanations, categories, multiple rounds, and AI-assisted question generation.

## 📌 Status

**Challenge 1 — WikiQuiz: Core prototype completed ✅**

Developed as part of the **Wikimedia Structured Wikipedia Dataset hands-on challenge**.
