# Tourist Safety System

## Overview

The Tourist Safety System is a web-based application developed to enhance the safety of tourists by combining machine learning, blockchain technology, and emergency communication services. The system predicts the risk level of a tourist based on different parameters and provides quick assistance during emergencies through SMS alerts and secure blockchain logging.

This project was developed as part of a college project to demonstrate the practical application of modern technologies in solving real-world safety challenges.

---

## Features

- User registration and login
- Secure password storage using Bcrypt
- Tourist risk prediction using a machine learning model
- Emergency SOS feature
- SMS notifications using Twilio
- Blockchain-based storage of emergency alerts
- Automatic Digital ID generation for each tourist
- MySQL database integration

---

## Technologies Used

### Backend
- Python
- Flask

### Database
- MySQL

### Machine Learning
- Scikit-learn
- Pandas
- NumPy

### Blockchain
- Ganache
- Web3.py

### Communication
- Twilio API

### Security
- Bcrypt
- SHA-256

---

## Project Structure

```
Tourist_Safety_System/
│
├── app.py
├── train_model.py
├── generate_dataset.py
├── tourist_risk_data.csv
├── tri_model.pkl
├── scaler.pkl
├── config.py
├── templates/
└── README.md
```

---

## Installation

### Clone the repository

```bash
git clone https://github.com/your-username/Tourist_Safety_System.git
cd Tourist_Safety_System
```

### Create a virtual environment

Windows

```bash
python -m venv venv
venv\Scripts\activate
```

Linux/macOS

```bash
python3 -m venv venv
source venv/bin/activate
```

### Install the required packages

If a `requirements.txt` file is available:

```bash
pip install -r requirements.txt
```

Otherwise install the dependencies manually:

```bash
pip install flask pymysql bcrypt pandas numpy scikit-learn twilio web3
```

---

## Database Setup

Create a MySQL database named:

```
tourist_safety
```

Update the database configuration in `config.py` (or `app.py`, depending on your project structure) with your MySQL credentials.

---

## Blockchain Setup

Start Ganache and make sure the local blockchain is running.

Example RPC URL:

```
http://127.0.0.1:7545
```

Update the blockchain configuration in the project if necessary.

---

## Twilio Configuration

Add your Twilio credentials before running the application.

Required details:

- Account SID
- Auth Token
- Twilio Phone Number

---

## Running the Application

Start the Flask server using:

```bash
python app.py
```

The application will be available at:

```
http://127.0.0.1:5000
```

---

## How It Works

1. A tourist registers and logs into the system.
2. The application collects the required information.
3. A machine learning model predicts the tourist's risk level.
4. If the user triggers the SOS feature, an SMS is sent to the registered emergency contact.
5. The emergency information is also stored on the blockchain, providing a secure and tamper-resistant record of the event.

---

## Machine Learning

The project includes a trained machine learning model that predicts the risk level of a tourist using the collected data.

Model files:

- `tri_model.pkl`
- `scaler.pkl`

The model can be retrained using:

```
train_model.py
```

---

## Security

The application includes several security measures:

- Password hashing using Bcrypt
- Secure user authentication
- SHA-256 based Digital ID generation
- Immutable emergency records using blockchain

---

## Future Enhancements

Some improvements that can be added in the future include:

- Live GPS tracking
- Google Maps integration
- Android mobile application
- Integration with nearby hospitals and police stations
- Cloud deployment
- AI-based route and safety recommendations

---

## Authors

Developed as a college project by:

- Laksh Khandelwal
- Team Members

---

## License

This project is intended for educational and learning purposes.
