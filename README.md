# 📚 Book Recommendation System using Collaborative Filtering

## 🔍 Project Overview

This project implements a **user-based collaborative filtering recommendation system** that suggests books to users based on their past ratings and reading behavior. The system leverages similarity between users to recommend books that similar users have enjoyed.

The project is built using the **Book-Crossing dataset** and demonstrates key concepts in **data cleaning, sparse matrices, similarity computation, and recommendation generation**.

---

## 🎯 Objective

To design and implement a scalable **book recommendation system** that:

* Identifies users with similar reading preferences
* Predicts ratings for unread books
* Recommends the **top 5 books** for each user

---

## 🧠 Methodology

### 1️⃣ Data Preparation (Project Part 1)

* Cleaned raw ratings data
* Removed missing and zero ratings
* Standardized column names
* Converted data into **LIBSVM format** to represent a **user–book rating matrix**
* Used a dummy label (`y = 0`) as required by LIBSVM (not used in analysis)

📄 Output:

* `user_book_matrix.libsvm`

---

### 2️⃣ Recommendation System (Project Part 2)

* Filtered:

  * Users with **≥ 65 ratings**
  * Books with **≥ 65 ratings**
* Constructed a **User × Book matrix**
* Converted matrix into a **sparse representation**
* Computed **cosine similarity** between users
* Selected **K = 10 nearest neighbors** for each user
* Predicted ratings using **weighted averages**
* Recommended **Top 5 unread books per user**

📄 Final Output:

* `Books_Recommended.csv`

---

## 🛠️ Technologies Used

* **Python**
* **Pandas**
* **NumPy**
* **Scikit-learn**
* **SciPy (Sparse Matrices)**
* **Jupyter Notebook**

---

## 📂 Project Structure

```
├── Books.csv
├── Ratings.csv
├── Users.csv
├── user_book_matrix.libsvm
├── Books_Recommended.csv
├── Project-Part-1.ipynb
├── Project-Part-2.ipynb
├── Project-Part-2.pdf
└── README.md
```

---

## 📊 Sample Recommendation Output

| User_ID | Book_Title      | Recommendation_Score |
| ------- | --------------- | -------------------- |
| 243     | Animal Dreams   | 10.0                 |
| 243     | A Fine Balance  | 10.0                 |
| 243     | Prodigal Summer | 9.0                  |

---

## 🚀 Key Learnings

* Handling large-scale datasets efficiently
* Working with sparse matrices
* Implementing collaborative filtering from scratch
* Measuring similarity using cosine similarity
* Translating theory into a real-world recommender system

---

## 📌 Future Enhancements

* Item-based collaborative filtering
* Hybrid recommendation models
* Model evaluation using RMSE / MAE
* Deployment using Flask or Streamlit

