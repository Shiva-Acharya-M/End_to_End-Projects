🎬 **Netflix Movie Recommendation Engine Using SVD**

📌 Project Overview

This project implements a personalized movie recommendation system inspired by Netflix, using Singular Value Decomposition (SVD) for collaborative filtering. The system learns latent user and movie preferences from historical rating data to predict how users are likely to rate unseen movies and generate meaningful recommendations.

🛠 Tech Stack
- Python
- Pandas, NumPy
- Jupyter Notebook
- Matplotlib / Seaborn (EDA & visualization)
- Surprise (SVD, BaselineOnly)

🧠 Approach & Methodology
- Used user–movie rating interactions to model preferences
- Performed data preprocessing and filtering:
  - Removed low-activity users 
  - Removed rarely rated movies 
- Neglected the date feature to focus on pure collaborative filtering
- Applied SVD from the Surprise library to decompose the user–item matrix into latent factors
- Tuned key SVD hyperparameters:
  - n_factors, n_epochs, learning rate, and regularization
- Evaluated performance using 3-fold cross-validation

📊 Model Performance: Model	RMSE
- Baseline (user + item bias)	: 0.9090
- Tuned SVD Model	: 0.9084
  - The SVD model consistently outperformed the baseline, confirming the presence of latent preference patterns
  - The marginal improvement highlights the high data sparsity and strong baseline bias signals in the dataset

⭐ Key Results
- Generated accurate rating predictions for unseen user–movie pairs
- Produced Top-5 personalized movie recommendations for a sampled user
- Achieved stable performance across cross-validation folds
- Demonstrated scalable recommendation modeling on 10M+ ratings

💼 Business Impact: A recommendation system like this can help streaming platforms such as Netflix to:
- Improve content discovery through personalization
- Increase watch time and user engagement
- Reduce decision fatigue for users
- Boost customer retention with relevant recommendations
- Enable data-driven content strategy decisions

🚀 Future Enhancements
- Incorporate time-aware models using rating timestamps
- Experiment with Hybrid recommender systems
- Add content-based filtering (genres, metadata)
- Deploy recommendations using a REST API or web app
