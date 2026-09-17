# 🔎 WikiMedia Smart Search

> Wikimedia Structured Wikipedia Dataset — hands-on challenge prototypes

This repository contains working prototypes built with the **Wikimedia Structured Wikipedia Dataset**.

## 🚀 Challenge 2 — WikiKnowledge Explorer

### Problem

Wikipedia contains information about topics, people, places, organizations and related articles, but discovering useful connections across articles can be difficult.

**WikiKnowledge Explorer** provides a simple interactive way to search an article, inspect its information, discover content-similar articles, view structured entities/references, and explore related information.

### Challenge flow

```text
Search Article
      ↓
Retrieve Article Information
      ↓
Find Related Information
      ↓
Organize Information
      ↓
Display Connections
      ↓
Explore Related Information
```

### ✅ Core requirements implemented

- 🔎 Search/select an article or topic
- 📖 Retrieve article title, description and abstract
- 🔗 Discover related/content-similar articles from the dataset
- 🧩 Display `main_entity` and `additional_entities`
- 📚 Display references when available
- 🧭 Explore a selected related article
- ❌ Handle empty/invalid input and missing information
- 📊 Display a clear final summary

### 🧠 How related articles are found

The prototype combines the article's **title, description and abstract** and represents them using **TF-IDF**. Cosine similarity is then used to identify the most content-similar articles in the loaded Wikimedia dataset.

> The similarity results are derived from text available in the dataset. They are presented as **content-similar articles**, not as guaranteed semantic or Wikidata relationships.

## 🧪 Tested example

Search term:

```text
files
```

Selected article:

```text
1060 aluminium alloy
```

Example related results included:

```text
3004 aluminium alloy
6005 aluminium alloy
1050 aluminium alloy
1070 aluminium alloy
1100 aluminium alloy
```

The prototype also displayed the selected article's structured entity information and completed the related-information exploration flow.

## 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| Python | Core application logic |
| Pandas | Dataset processing |
| NumPy | Data handling |
| Scikit-learn | TF-IDF and cosine similarity |
| PyArrow | Parquet support |
| KaggleHub | Wikimedia dataset access |
| Google Colab | Development and testing |

## 📊 Dataset

The project uses the **Wikimedia Structured Wikipedia Dataset** available through Kaggle.

During development, a single Parquet shard containing **25,000 articles and 19 columns** was loaded. The large dataset itself is **not stored in this repository**.

Important fields used by the explorer include:

```text
name
description
abstract
main_entity
additional_entities
references
```

## 📓 Challenge 2 Notebook

**[Open the Challenge 2 WikiKnowledge Explorer notebook](notebooks/Challenge_2_WikiKnowledge_Explorer.ipynb)**

The notebook contains the visible implementation code, dataset setup, and tested output.

## 📸 Output Evidence

The `screenshots/` folder contains visual evidence for the tested Challenge 2 flow:

1. Search and article selection
2. Related article discovery
3. Structured information
4. Final result

| Evidence | File |
|---|---|
| Search & Selection | `screenshots/01_challenge2_search_selection.svg` |
| Related Articles | `screenshots/02_challenge2_related_articles.svg` |
| Structured Information | `screenshots/03_challenge2_structured_information.svg` |
| Final Result | `screenshots/04_challenge2_final_result.svg` |

## 📁 Project Structure

```text
WikiMedia_Smart_Search/
│
├── README.md
├── requirements.txt
├── .gitignore
│
├── notebooks/
│   ├── Challenge_1_WikiQuiz.ipynb
│   └── Challenge_2_WikiKnowledge_Explorer.ipynb
│
└── screenshots/
    ├── 01_challenge2_search_selection.svg
    ├── 02_challenge2_related_articles.svg
    ├── 03_challenge2_structured_information.svg
    └── 04_challenge2_final_result.svg
```

## 🔬 Testing

The Challenge 2 prototype was tested for:

- Valid article/topic search
- Multiple matching articles
- Article selection
- Invalid selection numbers
- Missing descriptions/abstracts
- Structured entity information
- References stored as list/array-like data
- Related article discovery
- Related article exploration

## 🌱 Optional future improvements

The challenge specification also suggests extensions such as:

- Interactive graph visualization
- Clickable nodes
- Search and filters
- Zoom/navigation
- Category-based organization
- Visual relationship connections
- Recommended articles
- Improved UI

## 📌 Challenge Status

**Challenge 1 — WikiQuiz:** Core prototype completed ✅

**Challenge 2 — WikiKnowledge Explorer:** Core prototype completed ✅

---

### Challenge Context

Developed as part of the **Wikimedia Structured Wikipedia Dataset hands-on challenge**.

**Challenge:** Challenge 2 — WikiKnowledge Explorer  
**Language:** Python  
**Environment:** Google Colab  
**Dataset:** Wikimedia Structured Wikipedia Dataset
