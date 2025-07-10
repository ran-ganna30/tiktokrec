# 🎵 TikTok-Style Recommendation System (Collaborative + Content-Based Filtering)

This project implements a simplified version of TikTok’s recommendation algorithm using **PySpark's ALS (Alternating Least Squares)** for collaborative filtering, and **cosine similarity** for content-based filtering.

Inspired by the conceptual workings of TikTok’s algorithm shared publicly, this repo brings those concepts into code. The system predicts and recommends videos based on user interaction history (likes, watch time, comments) and video content attributes (duration, text, audio).


## 🧠 Overview

TikTok’s recommendation system is a blend of:

- **Collaborative Filtering** — Suggests videos based on user similarity
- **Content-Based Filtering** — Suggests videos based on video feature similarity

This project recreates both strategies and combines them to build an ensemble recommendation pipeline.

---

## ⚙️ Tech Stack

- Python 3.8+
- PySpark
- Spark MLlib
- scikit-learn
- pandas
- JDK 11+

---

## 📁 Data Format

### `tiktok_data.txt` (Collaborative Filtering)
Format: `user_id::video_id::interaction_score`

```txt
1::101::4.5
1::102::5.0
2::103::3.0
````

### `video_features.csv` (Content-Based Filtering)

Format: A table with numerical features of videos

```csv
video_id,length,audio_energy,text_score
101,15,0.8,0.9
102,30,0.6,0.7
...
```

---

## 🔍 How It Works

### Collaborative Filtering

* Read user-video interaction data
* Use Spark’s ALS algorithm to train a matrix factorization model
* Predict ratings for unseen videos
* Generate top-N recommendations per user

### Content-Based Filtering

* Use cosine similarity on video feature vectors
* Recommend videos with similar attributes to those previously liked by the user

---


#

## 🔮 Future Work

* Add hybrid recommender (ALS + content similarity)
* Incorporate session-based behaviors (watch time patterns)
* Build frontend interface with Streamlit
* Save/load models and recommendations
