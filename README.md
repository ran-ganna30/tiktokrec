# TikTok-Style Video Recommendation System (PySpark + ALS)

This project demonstrates a simplified version of the TikTok recommendation algorithm using **Apache Spark's ALS (Alternating Least Squares)** collaborative filtering model. It predicts video recommendations based on user interaction history such as watch time, likes, and skips.

## 🔍 Features

- Collaborative Filtering using PySpark's MLlib
- Matrix factorization via ALS
- Evaluation with RMSE
- Scalable for large datasets
- Sample interaction data provided

## 📁 Dataset Format

The dataset used is a synthetic interaction log named `tiktok_data.txt`. Each line follows the format:

```

user\_id::video\_id::interaction\_score

```

Example:
```

1::101::4.5
2::103::3.0
3::105::4.0

````

The `interaction_score` can represent a combination of likes, watch time, comments, etc., mapped to a numerical scale.

## 🛠️ Technologies Used

- Python 3.8+
- Apache Spark (PySpark)
- Spark MLlib
- JDK 11+
- Pandas (for content-based filtering extension)
- scikit-learn (for cosine similarity)



## 🧠 Model Overview

The ALS algorithm learns latent features for users and items, using implicit or explicit feedback. The model:

* Splits data into train/test
* Trains ALS using user/video/interaction triples
* Evaluates using RMSE
* Outputs top-20 video recommendations per user



## 🚀 Future Enhancements

* Add content-based filtering using cosine similarity
* Build a hybrid recommender (collaborative + content-based)
* Visualize recommendations
* Deploy via Streamlit or Flask

## 🙌 Acknowledgements

Inspired by [The Clever Programmer](https://thecleverprogrammer.com/) blog post on TikTok algorithm implementation.


