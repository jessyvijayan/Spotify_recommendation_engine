# Spotify_recommendation_engine

Spotify Music Recommendation Engine: Latent Factor Modeling
This project implements a high-scale recommendation system using Collaborative Filtering and Matrix Factorization techniques. By decomposing a user-song interaction matrix, the system identifies hidden musical preferences to deliver highly personalized song suggestions to 1,000+ unique users.

🚀 Key Features
Latent Factor Discovery: Utilized Non-Negative Matrix Factorization (NMF) to decompose a sparse 1,000x5,000 interaction matrix into user-feature and item-feature components, uncovering hidden dimensions of musical taste.
Similarity Search: Integrated a Nearest Neighbors algorithm to calculate distance metrics between latent vectors, enabling real-time "user-to-user" and "item-to-item" discovery.
Scalable Architecture: Designed the system to handle a high-dimensional dataset of 5,000 individual song tracks, optimizing for sparse data handling.
Unsupervised Clustering: Applied K-Means Clustering to the latent feature space to segment users into distinct "musical personas" for targeted content delivery.

🛠️ Tech Stack
Decomposition: Sklearn NMF (Matrix Factorization)
Unsupervised Learning: Sklearn K-Means, Nearest Neighbors
Data Handling: Pandas (Pivot Tables, Sparse Matrices), NumPy
Visualization: Matplotlib (Cluster Analysis)

📊 Technical Workflow
Interaction Matrix Construction: Transformed raw Spotify listening data into a massive User-Item matrix where each cell represents a frequency/rating score.
Dimensionality Reduction: Used NMF to reduce the 5,000 song features into a smaller set of latent components, capturing the "essence" of different music genres/styles.
Top-K Recommendations: Implemented a prediction engine that calculates the dot product of latent matrices to estimate scores for songs a user hasn't heard yet.
Cluster Validation: Used the "Elbow Method" with K-Means to determine the optimal number of user segments, ensuring high intra-cluster similarity.

📈 Impact
Personalization: Capable of generating the "Top 5 Recommended Songs" for any user in the dataset based on their similarity to other high-frequency listeners.
Discoverability: The NMF approach allows the system to recommend "long-tail" songs that a user might not find through standard popularity-based sorting.

💻 How to Run
Clone the repository:
git clone [git@github.com:jessyvijayan/Spotify_recommendation_engine.git]

Install Dependencies:
pip install pandas numpy scikit-learn matplotlib

Run Engine:
[python spotify_recommender.py](https://github.com/jessyvijayan/Spotify_recommendation_engine/blob/main/Spotify_recommendation_system.ipynb)
Use code with caution.
