# YogaZen – Recommendation System

## 1. Project Overview

YogaZen Recommendation System is a Machine Learning-based product recommendation system designed to provide personalized product suggestions to customers based on their interests, preferences, and interaction history.

The system uses a Hybrid Recommendation Approach combining Collaborative Filtering and Content-Based Filtering.

## 2. Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- FastAPI
- TF-IDF
- Truncated SVD

## 3. Recommendation Algorithms

The model combines two techniques:

**Collaborative Filtering (65%)**

Recommends products based on customer behaviour and similarities between users.

**Content-Based Filtering (35%)**

Recommends products based on product categories and descriptions.

## 4. Dataset Information

The initial prototype uses a synthetic dataset containing:

- 1,000 customers
- 120 products
- Customer-product interaction records

The synthetic dataset will be replaced with actual YogaZen customer interaction data before production deployment.

## 5. Project Structure

- `train_model.py` – Python code for training the recommendation model.
- `app.py` – FastAPI application for generating recommendations.
- `requirements.txt` – Required Python libraries.
- `data/` – Customer, product and interaction datasets.
- `models/` – Saved trained ML model.
- `outputs/` – Recommendation results and evaluation metrics.

## 6. API Endpoints

- `GET /health` – Checks whether the ML service is running.
- `POST /predict` – Generates personalized product recommendations.
- `POST /recommend` – Provides product recommendations.

## 7. How to Run the Project

Install dependencies:

```bash
pip install -r requirements.txt
```

Train the recommendation model:

```bash
python train_model.py
```

Start the API service:

```bash
uvicorn app:app --reload
```

## 8. Model Evaluation

Initial evaluation using synthetic data:

- Recall@6: 0.4067
- NDCG@6: 0.8471

Note: These results are based on synthetic data and do not represent real-world production performance.

## 9. Future Improvements

- Integrate real YogaZen customer interaction data.
- Connect the ML API with the YogaZen backend.
- Improve recommendation accuracy using actual customer behaviour.
- Deploy the recommendation service for production use.

## 10. Project Status

Initial ML prototype completed. Backend integration and validation using real YogaZen data are pending.
