# ✈️ Flight Price Prediction

A machine learning web application that predicts flight ticket prices based on journey details such as airline, source, destination, departure/arrival times, and total stops.

Built with **Flask**, **scikit-learn (Random Forest)**, and **HTML/CSS (Bootstrap)**.

---

## 📸 Demo

> Add a screenshot or GIF of your running app here.

---

## 🚀 Features

- ✅ Predict flight prices in Indian Rupees (₹)
- ✅ Input form for departure/arrival date & time
- ✅ Select source and destination cities
- ✅ Choose airline from 13 carriers
- ✅ Select number of stops (0–4)
- ✅ One-hot encoded categorical features
- ✅ Deployable to Heroku via `Procfile` + `gunicorn`

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|------------|
| Frontend | HTML5, CSS3, Bootstrap 4 |
| Backend | Flask (Python) |
| ML Model | Random Forest Regressor (scikit-learn) |
| Data Handling | pandas, numpy |
| Deployment | gunicorn, Heroku-ready |

---

## 📦 Installation

### 1. Clone the repository

```bash
git clone https://github.com/gracemann365/Flight-Price-Prediction.git
cd Flight-Price-Prediction
```

### 2. Create a virtual environment

```bash
python -m venv venv
# Windows
venv\Scripts\activate
# macOS/Linux
source venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Run the app

```bash
python app.py
```

Open your browser at **`http://127.0.0.1:5000/`**

---

## 📁 Project Structure

```
Flight-Price-Prediction/
├── app.py                  # Flask application entry point
├── flight_rf.pkl           # Trained Random Forest model
├── flight_price.ipynb      # Jupyter notebook: EDA + model training
├── Procfile                # Heroku deployment config
├── requirements.txt        # Python dependencies
├── .gitignore              # Git ignore rules
├── README.md               # Project documentation
├── templates/
│   └── home.html           # Frontend form template
└── static/
    └── css/
        └── styles.css      # Custom styles
```

---

## 🧠 Model Details

- **Algorithm:** Random Forest Regressor
- **Training Data:** Flight price dataset with ~10,000+ records
- **Features:** 29 engineered features including:
  - Journey date (day, month)
  - Departure & arrival time (hour, minute)
  - Duration (hours, minutes)
  - Total stops
  - Airline (one-hot encoded, 11 columns)
  - Source city (one-hot encoded, 4 columns)
  - Destination city (one-hot encoded, 5 columns)

See `flight_price.ipynb` for the full exploratory data analysis and training pipeline.

---

## ☁️ Deployment (Heroku)

This project is ready to deploy on Heroku:

```bash
heroku create your-app-name
git push heroku main
heroku open
```

The `Procfile` is configured to run with **gunicorn**:

```
web: gunicorn app:app
```

---

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -m 'Add some feature'`)
4. Push to the branch (`git push origin feature/your-feature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 👨‍💻 Author

**gracemann365**  
[GitHub Profile](https://github.com/gracemann365)

---

## ⭐ Acknowledgments

- Dataset: Flight price prediction dataset (Kaggle)
- Built with ❤️ using Flask and scikit-learn