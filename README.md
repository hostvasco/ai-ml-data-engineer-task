# 🛠️ [WIP] Hostaway Senior Data Engineer, AI Team: Take-Home Task

**Objective:**
This task is designed to assess your data engineering and AI skills in a scenario relevant to Hostaway's focus on improving customer interactions through intelligent data analysis. You will build a data pipeline to process and analyze conversations, extracting insights on sentiment and topic.

---

## 💾 Dataset
You will use the **Ubuntu Dialogue Corpus**, which contains multi-turn dialogues from users seeking technical support.

* **Access:** [https://www.kaggle.com/datasets/rtatman/ubuntu-dialogue-corpus/data](https://www.kaggle.com/datasets/rtatman/ubuntu-dialogue-corpus/data)
* **Estimated Time:** 4 hours

---

## Part 1: Data Engineering - Conversation and Sentiment Analysis

In this part, you will construct a data pipeline to process the raw chat data and perform sentiment analysis and topic extraction.

### Tasks: Data Ingestion and Structuring

* Develop a **Python-based pipeline** to ingest the chat data from the provided CSV files.
* Structure the data to represent **conversations**, where each conversation consists of multiple turns.
* For each conversation, calculate the **overall sentiment**. You can use a pre-trained sentiment analysis model for this.

### Output:

Produce a final output (e.g., a **CSV file** or a **DuckDB database file**) with each row representing a **single conversation**.

This output should include the:
1.  `dialogueID`
2.  `full conversation text`
3.  `calculated sentiment score` (e.g., positive, negative, neutral).

---

## Part 2: AI/ML - Topic Extraction and Alignment

In this section, you will focus on extracting topics from the conversations and aligning them with a predefined list of topics relevant to a technical support context.

### Predefined Topics:

* Hardware Issues
* Software Installation
* Network Configuration
* Pizzas with Ketchup
* User Permissions
* Dog Walking
* System Performance
* Climbing Mountains
* Data Recovery

### Tasks:

#### Topic Extraction:

* For each conversation, extract the main topic or topics being discussed. You should specifically use **BERTopic** for this part of the task.

#### Topic Alignment:

* Develop a method to align the extracted topics with the predefined list above.
* The goal is to categorize each conversation under **one or more** of the predefined topics.
* If possible, expose the topics *before* alignment for inspection (so we can evaluate the alignment).

> **Example:** Chat #23 → `extracted_topics`: ["linux", "tech support", "gpu drivers", "install"] → `aligned_topics` to: "Software Installation"

### Output:

Extend your output from Part 1 to include the:
* `extracted topic(s)`
* `aligned predefined topic(s)` for each conversation.

---

## 📦 Deliverables

1.  **Code:** Submit your complete, **well-documented Python code**. Your code should be able to run locally independently by a reviewer, so make sure you have instructions on how to do it.
2.  **Output Data:** Provide the final processed data file containing the conversation, sentiment, and topic information.
3.  **Brief Explanation:** A short document (e.g., a `README.md` file) explaining your approach, the tools and libraries you used, and any assumptions you made.

---

## 📈 Future Improvements

Explain how you’d change this approach with **online topic modeling**, so that we wouldn’t need to start with a list of topics that is manually created by a human.
