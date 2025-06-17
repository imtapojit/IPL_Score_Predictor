# 🏏 IPL Score Predictor : *Deep Learning-Based Forecasting of First Innings Score in IPL Matches*

---

## 📌 Project Overview

This project presents a deep learning-based approach to predict the *final first innings score* in Indian Premier League (IPL) matches. By merging detailed *ball-by-ball* and *match-level* datasets using a unique match identifier, the model learns patterns from historical match data to provide accurate score forecasts in real-time.

The goal is to empower data-driven decision-making for broadcasters, analysts, and cricket enthusiasts by capturing match context, player performance, and game progression dynamically.

---

## 📊 Datasets Used

Two primary datasets are used:

- *Ball-by-Ball Dataset*: Contains granular data of every delivery in IPL matches (2008–2022)
- *Match-Level Dataset*: Includes metadata such as team names, venue, toss result, match date, etc.

These datasets are merged using a matchID to align each ball event with its corresponding match details, enabling comprehensive feature engineering.

---

## 🔍 Key Features Extracted

- Batsman, Bowler names  
- Total runs, extras, wickets till current ball  
- Over and ball progression  
- Team info, venue, toss decision, match date  
- Batting and bowling performance history  
- Real-time metrics: run rate, wicket fall pattern

---

## 🧠 Model Overview

Multiple deep learning models were explored:

- *Deep Neural Network (DNN)*
- *Convolutional Neural Network (CNN)*
- *Recurrent Neural Networks (RNN, LSTM, Bi-LSTM,GRU)*
- *Transformer-Based Model* (best performer)
- *Ensemble Methods*

These models were trained on processed numerical and categorical inputs derived from the merged dataset. The Transformer model outperformed others with superior learning of match momentum and temporal dependencies.

---

## 🏗️ Workflow Summary

1. *Data Preprocessing*
   - Cleaned and standardized team/player names
   - Merged datasets via matchID
   - Encoded categorical features
   - Normalized numerical inputs

2. *Feature Engineering*
   - Aggregated statistics per over and inning
   - Generated real-time features up to each ball
   - Created match context indicators

3. *Model Training & Evaluation*
   - Trained models using training/validation split
   - Evaluated using R², RMSE, and MAE metrics
   - Visual comparison of predicted vs actual scores

---

## 📈 Model Performance

- *Best Model*: Transformer  
- *R² Score*: 0.93  
- *RMSE*: ~12 runs  
- Accurately captured momentum shifts and batting pace across various match situations

---

## 🧪 Sample Prediction

bash
Input:
- Team: RCB vs MI
- Over: 12.4
- Runs: 102
- Wickets: 3
- Batsmen: Kohli, Maxwell
- Bowler: Chawla
- Venue: M. Chinnaswamy

Output:
- Predicted First Innings Final Score: 182


---

## 📂 Project Structure


IPL-Score-Predictor/
├── data/              # Raw and processed datasets
├── notebooks/         # EDA and model experiments
├── models/            # Trained model files
├── utils/             # Helper functions/scripts
├── train.py           # Training script
├── predict.py         # Inference script
├── requirements.txt   # Package dependencies
└── README.md          # Project documentation


---

## 🔮 Future Scope

- Add real-time player form, pitch, and weather data
- Create a simple web app for user interaction
- Extend to predict second innings and win probabilities
- Try ensemble and hybrid models for robustness

---

## 🙌 Acknowledgements

- IPL datasets from Kaggle and public sources  
- Inspiration from CricAI, ESPNcricinfo Analytics  
- Libraries: PyTorch, NumPy, Pandas, Scikit-learn, Matplotlib

---

## 📜 License

This project is licensed under the MIT License.

---

> Built for cricket lovers who also speak code 🧠⚡
