PSL Team Winning Prediction API (Live Data)
https://img.shields.io/badge/Python-3.8%252B-blue?logo=python
https://img.shields.io/badge/Libraries-NumPy%252C%2520Pandas%252C%2520Matplotlib%252C%2520Scikit--learn-orange
https://img.shields.io/badge/Framework-FastAPI-brightgreen
https://img.shields.io/badge/Status-Development-yellow

A RESTful API that dynamically fetches live player and match data to predict the likely winner of Pakistan Super League (PSL) cricket matches. This project uses machine learning on real-time statistics to provide data-driven insights.

🚀 Features
Live Data Integration: Fetches real-time player statistics and match information from external cricket APIs

Machine Learning Predictions: Uses a pre-trained model to calculate win probabilities based on current team data

Dynamic Visualization: Generates real-time charts and graphs to visualize prediction insights

RESTful API: Simple endpoints for accessing predictions and match data

Easy Integration: Well-documented API suitable for integration with other applications

🛠️ Tech Stack
Backend Framework: FastAPI

Programming Language: Python 3.8+

Data Processing: Pandas, NumPy

Machine Learning: Scikit-learn

Data Visualization: Matplotlib

HTTP Requests: Requests library

Data Sources: CricAPI or Cricket-Live-Data API

📦 Installation
Clone the repository

bash
git clone https://github.com/your-username/psl-winning-prediction.git
cd psl-winning-prediction
Create and activate a virtual environment

bash
python -m venv venv
source venv/bin/activate  # On Windows: .\venv\Scripts\activate
Install dependencies

bash
pip install fastapi uvicorn requests python-multipart numpy pandas matplotlib scikit-learn python-dotenv
Set up environment variables
Create a .env file in the root directory:

bash
# For CricAPI
CRIC_API_KEY=your_cricapi_key_here

# OR for RapidAPI
X_RAPIDAPI_KEY=your_rapidapi_key_here
X_RAPIDAPI_HOST=cricket-live-data.p.rapidapi.com
Run the application

bash
uvicorn main:app --reload
🚦 API Usage
Get Prediction Between Two Teams
http
GET /predict?team1=Islamabad United&team2=Lahore Qalandars
Response:

json
{
  "team1": "Islamabad United",
  "team2": "Lahore Qalandars",
  "venue": "Gaddafi Stadium, Lahore",
  "prediction": "Islamabad United",
  "probability": 0.67,
  "confidence": "High",
  "key_factors": [
    "Islamabad has won 60% of their last 5 matches",
    "Lahore is missing their key bowler Shaheen Afridi"
  ]
}
Get Upcoming Fixtures
http
GET /fixtures
Get Player Statistics
http
GET /player/{player_id}
📊 How It Works
API Request: User requests a prediction between two teams

Data Fetching: System fetches current player statistics and match data from external APIs

Feature Engineering: Data is processed into meaningful features (team form, player strength, venue advantage)

Prediction: Pre-trained ML model calculates win probability

Response: API returns prediction with confidence level and key factors

🗂️ Project Structure
text
psl-winning-prediction/
├── src/
│   ├── main.py                 # FastAPI application entry point
│   ├── data_fetcher.py         # Module for fetching external API data
│   ├── predictor.py            # ML model and prediction logic
│   ├── visualizer.py           # Data visualization functions
│   └── cache_manager.py        # Request caching functionality
├── models/
│   └── trained_model.pkl       # Pre-trained ML model
├── requirements.txt            # Project dependencies
├── .env.example               # Example environment variables
└── README.md
🔮 Future Enhancements
Player vs Player (PvP) performance analysis

Real-time prediction updates during matches

Fantasy cricket points predictor

Web dashboard with interactive visualizations

Docker containerization for easy deployment

Webhook support for automatic predictions

🤝 Contributing
Contributions are welcome! Please feel free to submit a Pull Request.

Fork the project

Create your feature branch (git checkout -b feature/AmazingFeature)

Commit your changes (git commit -m 'Add some AmazingFeature')

Push to the branch (git push origin feature/AmazingFeature)

Open a Pull Request

📄 License
This project is licensed under the MIT License - see the LICENSE file for details.

⚠️ Disclaimer
This prediction API is for educational and entertainment purposes only. Predictions are based on statistical models and may not reflect actual match outcomes.
