# 🎟️ Transparent Giveaway

A web application that validates Instagram giveaway entries and performs **fair, reproducible, and auditable random draws**, overcoming the limitations of traditional giveaway tools.

---

## 🚀 Why I Built This Project

While organizing a giveaway for my small business **Caserito Bakery**, I discovered that several popular Instagram giveaway tools only processed the **first 100 comments** of a post.

Since the giveaway had more than **150 comments**, many participants were automatically excluded from the draw.

Instead of accepting that limitation, I built my own tool capable of processing every comment and generating a transparent, verifiable giveaway.

---

## ✨ Features

- 📂 Supports **CSV** and **Excel** files.
- 🔍 Automatically detects username and comment columns.
- ✅ Validates giveaway rules (e.g., mentioning another user).
- 🚫 Removes duplicate entries.
- 🎲 Uses the **Fisher–Yates Shuffle** algorithm for fair random selection.
- 🏆 Selects one winner and multiple backup winners.
- 📄 Generates an audit report containing all giveaway information.
- 💻 Runs entirely in the browser with **no backend required**.

---

## ⚙️ How It Works

### 1. Comment Extraction

Comments are extracted from Instagram's rendered HTML using **Python** and **BeautifulSoup**, avoiding the limitations found in many existing giveaway tools.

### 2. Entry Validation

The application analyzes the generated file and automatically checks whether each entry satisfies the giveaway rules:

- Valid mention of another Instagram user.
- Only one valid entry per participant.
- Automatic removal of invalid or duplicate entries.

### 3. Random Draw

After validating all participants, the application performs a **Fisher–Yates Shuffle**, ensuring an unbiased and statistically uniform random selection of the winner and backup winners.

### 4. Audit Report

Once the draw is completed, the application generates a report containing:

- Draw date and time.
- Random seed used.
- Complete list of valid participants.
- Winner.
- Backup winners.

This makes the entire process transparent and verifiable.

---

## 🛠️ Technologies

### Frontend

- HTML5
- CSS3
- Vanilla JavaScript

### File Processing

- SheetJS

### Data Extraction

- Python
- BeautifulSoup

### Algorithms

- Fisher–Yates Shuffle

---

## 📊 Real-World Use Case

This application was developed and used for an actual Instagram giveaway organized by **Caserito Bakery**, a handmade cookie business.

### Results

- 💬 182 comments processed.
- ✅ 19 valid entries after applying the giveaway rules.
- 🏆 1 winner and 2 backup winners selected.
- 📄 Audit report automatically generated.

---

## 📚 What I Learned

During this project I worked on:

- Data cleaning and validation.
- Business rule implementation.
- CSV and Excel file processing.
- Client-side data manipulation with JavaScript.
- HTML parsing using Python and BeautifulSoup.
- Randomization algorithms.
- Building a complete web application without a backend.

---

## 🎯 Project Goal

The goal of this project was to build a tool capable of running **transparent, fair, and verifiable Instagram giveaways** without the arbitrary limitations imposed by existing solutions.

By combining automated validation, unbiased random selection, and an audit trail, the application ensures that every eligible participant has an equal chance of winning.
