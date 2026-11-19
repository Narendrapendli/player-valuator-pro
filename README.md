# ⚽ PlayerValuator Pro v2.0

Advanced AI-Powered Football Player Valuation Platform using Machine Learning.

![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)
![Streamlit](https://img.shields.io/badge/Streamlit-1.28+-red.svg)
![FastAPI](https://img.shields.io/badge/FastAPI-0.100+-009688.svg)
![XGBoost](https://img.shields.io/badge/XGBoost-2.0+-green.svg)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)

## 🚀 Features

- 🤖 **AI-Powered Predictions** — XGBoost & LSTM hybrid models
- 📊 **Rich Analytics** — Interactive visualizations with Plotly
- ⚡ **Real-Time Performance** — FastAPI backend for instant predictions
- 🎯 **86% Model Accuracy** — Trained on 10,000+ player records
- 🔮 **Ensemble System** — Combines multiple ML techniques

## 📸 Screenshots

### 🏠 Home Dashboard
<img width="1919" height="712" alt="Home Dashboard" src="https://github.com/user-attachments/assets/78f3b53a-1a1b-4125-94fc-fca5f5dfaaa7" />

### 🤖 AI Predictor
<img width="1919" height="724" alt="AI Predictor" src="https://github.com/user-attachments/assets/4562c830-bd75-4843-b5c7-29e51a36c1e8" />

## 🛠️ Technology Stack

- **Frontend:** Streamlit, Plotly, HTML/CSS
- **Backend:** FastAPI
- **ML Models:** XGBoost, LSTM (TensorFlow/Keras)
- **Data Processing:** Pandas, NumPy
- **Visualization:** Plotly, Seaborn, Matplotlib

## 📦 Installation

### Prerequisites
- Python 3.9 or higher
- pip package manager

### Setup

1. **Clone the Repository**
```bash
git clone https://github.com/Narendrapendli/player-valuator-pro.git
cd player-valuator-pro
```

2. **Create Virtual Environment**
```bash
python -m venv venv
```

**Windows:**
```bash
venv\Scripts\activate
```

**Linux / macOS:**
```bash
source venv/bin/activate
```

3. **Install Dependencies**
```bash
pip install -r requirements.txt
```

4. **Run the Training Notebooks**
```bash
jupyter notebook
```
*Run the notebooks in order:*
1. Data Exploration
2. Model Training
3. LSTM Training
4. Ensemble Model Comparison

5. **Start the Streamlit Application**
```bash
streamlit run app.py
```

6. **Start the FastAPI Backend**
```bash
uvicorn api:app --reload
```

## 📊 Dataset

The system analyzes **10,754 football player records** with features including:
- Age
- Height
- Position
- Goals
- Assists
- Appearances
- Minutes Played
- Injury History
- Disciplinary Records
- Market Value

## 🧠 Model Architecture

### XGBoost Model
- **Type:** Gradient Boosting Regressor
- **Trees:** 1,000 estimators
- **Learning Rate:** 0.05
- **RMSE:** €7.4M
- **Training Samples:** 8,469

### LSTM Model
- **Architecture:** 3-layer LSTM neural network
- **Sequence Length:** 5 time steps
- **Features:** 19 engineered features
- **Activation:** ReLU + Linear output

### Ensemble System
The platform combines XGBoost and LSTM predictions using a weighted ensemble approach.
- **Method:** Weighted Average
- **Optimization:** Validation-loss minimization
- **Weights:** Dynamically determined based on model performance

## 📁 Project Structure

```
PlayerValuatorPro/
├── app.py                          # Main Streamlit application
├── api.py                          # FastAPI backend
├── final_data.csv                  # Player dataset
├── valuation_model.joblib          # Trained XGBoost model
├── lstm_model.h5                   # Trained LSTM model
├── lstm_scaler_X.joblib           # LSTM input scaler
├── lstm_scaler_y.joblib           # LSTM output scaler
├── lstm_metadata.joblib           # LSTM configuration
├── ensemble_weights.joblib        # Ensemble weights
├── 1_Data_Exploration.ipynb       # Data analysis notebook
├── 2_Model_Training.ipynb         # XGBoost training
├── 3_LSTM_Training.ipynb          # LSTM training
├── 4_Ensemble_Model_Comparison.ipynb  # Model comparison
├── requirements.txt               # Python dependencies
└── README.md                      # Project documentation
```

## 🎯 Usage

### Web Interface
1. Navigate to the **Home** page for a system overview.
2. Use the **AI Predictor** to estimate player market values.
3. Compare models using the **Model Comparison** dashboard.
4. Explore player data through the **Visualization Gallery**.
5. Review model performance through the **Model Performance** section.

### API Endpoint
Example prediction request:
```python
import requests

payload = {
    "age": 25,
    "height": 180,
    "appearance": 30,
    "goals": 15,
    "assists": 8,
    # ... other features
}

response = requests.post(
    "http://127.0.0.1:8000/predict",
    json=payload
)
print(response.json())
```

## 📈 Performance Metrics

| Model | RMSE | MAE | R² Score |
| :--- | :--- | :--- | :--- |
| **XGBoost** | €7.4M | €5.2M | 0.89 |
| **LSTM** | €8.5M | €6.0M | 0.85 |
| **Ensemble** | €6.8M | €4.8M | 0.92 |

## 🔮 Future Enhancements

- 🔄 Real-time football data integration
- 👤 Player comparison feature
- 🏟️ Team analysis dashboard
- 💰 Transfer value prediction
- 📱 Mobile application
- 🌍 Multi-league support
- 📈 Advanced player performance analytics

## 👨‍💻 Author

**Narendra Pendli**
- GitHub: [https://github.com/Narendrapendli](https://github.com/Narendrapendli)

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Football analytics datasets and publicly available player statistics
- Built with Streamlit and FastAPI
- ML models powered by XGBoost and TensorFlow/Keras
- Data processing and visualization powered by Pandas, NumPy, Plotly, Matplotlib, and Seaborn

## ⭐ Star this Repository

If you found this project useful, consider giving the repository a ⭐ Star!

---
Made with ❤️, 🤖 and ⚽ by **Narendra Pendli**
