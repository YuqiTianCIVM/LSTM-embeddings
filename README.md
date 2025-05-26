# LSTM-embeddings
A lightweight toolkit for learning fixed-length sequence embeddings using LSTM models, demonstrated on synthetic casino session data (and easily extended to other domains like finance).

## Features
- **Sequence Encoder**: Chronologically ordered session features → 64-dim LSTM embedding  
- **Cyclical Time Encoding**: Day-of-week and hour-of-day converted to sine/cosine  
- **Rare-Event Weighting**: Optional sample weighting for sparse “win” sessions  
- **Similarity Search**: Cosine similarity on embeddings to find behavioral peers  
- **Churn & Risk Detection**: Examples of flagging likely churners and high-risk players  

## Repository Structure
 ```
lstm-embeddings/
├── data/
│   └── synthetic_casino_sessions.csv   # Generated session records
├── models/
│   └── lstm_player_embedding.py        # LSTM encoder & embedding extraction
├── notebooks/
│   └── analysis.ipynb                  # Exploratory data analysis & plausibility checks
├── finance/                            # Placeholder for future finance embeddings
│   └── notebook_finance_embeddings.ipynb
└── README.md                           # Project overview and usage
 ```
## Installation
1. Clone the repo:  
```
   bash
   git clone https://github.com/yourusername/lstm-sequential-embeddings.git
   cd lstm-sequential-embeddings
```
2.	Create a virtual environment and install dependencies:
 ```
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
 ```


Usage
1.	Generate or place your data in data/.
2.	Run the LSTM embedding script:
 ```
python models/lstm_player_embedding.py
 ```

3.	Extract embeddings and compute cosine similarities for downstream tasks.

Extensibility
 ```
	•	Add new domains: drop your time-series CSV into a subfolder (e.g. finance/), adapt feature engineering, and reuse the LSTM model.
	•	Customize: tweak maxlen, embedding size, loss-weighting, or switch to Transformer encoders.
 ```
Contributing

Feel free to open issues or pull requests to add new datasets, improve model architectures, or extend examples!


