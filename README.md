# Phishing URL Detection System

A machine-learning project for assessing whether a URL may be associated with phishing. It is intended to support security awareness and defensive analysis by highlighting suspicious URL characteristics. It is not a substitute for browser protections, threat-intelligence services, or human review.


## Contents

- [Overview](#overview)
- [How it works](#how-it-works)
- [Features](#features)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Data and privacy](#data-and-privacy)
- [Evaluation](#evaluation)
- [Limitations and safe use](#limitations-and-safe-use)
- [Project structure](#project-structure)
- [Troubleshooting](#troubleshooting)
- [Contributing](#contributing)
- [License](#license)

## Overview

Phishing URLs can imitate trusted services, use misleading hostnames, or hide their destination behind redirects and URL shorteners. This project provides a way to classify a submitted URL as **likely legitimate** or **potentially phishing**, based on the detection logic and data available in the implementation.

## How it works

A typical URL-classification workflow consists of:

1. **Input validation:** The user a URL into the web interface.
2. **Feature extraction:** Derive signals from the URL string, such as hostname and path characteristics, URL length, use of an IP address, unusual separators, or suspicious tokens. The implemented feature set may differ.
3. **Classification:** Apply the project's configured rules or trained model to the extracted signals.
4. **Result presentation:** The application returns a risk score, classification, and relevant detection.

## Features

- URL-based phishing classification.
- Automated extraction of URL characteristics.
- A command-line or API interface.
- Model training and evaluation utilities.
- A prediction score or label for review.

## Requirements

 - Python
 - Flask
 - Scikit-learn
 - Pandas
 - Numpy
 - HTML
 - CSS
 - Javascript
 - tldextract
 - python-Levenshtein

## Installation

Clone the repository
```bash
 git clone 
 cd
```

```bash
 python -m venv .env
```

On Windows:

```powershell
 .env\Scripts\Activate
```

On macOS or Linux:

```bash
 source .env/bin/activate
```

Install dependencies

```bash
 pip install -r requirements.txt
```

## Usage

Start the application:

```bash
 python app.py
```

or:
```bash
 python main.py
```

Open the local address displayed in your terminal
```bash
 http://127.0.0.1:5000/
```

### Example of the/an input

Input a full URL of the domain or site to be verified ie;

```text
 https://example.com/account
```

## Evaluation

- **Precision:** Of URLs flagged as phishing, how many are actually phishing?
- **Recall:** Of phishing URLs in the test set, how many were detected?
- **F1 score:** A combined measure of precision and recall.
- **False-positive rate:** How often legitimate URLs are incorrectly flagged.
- **Confusion matrix:** The counts of correct and incorrect predictions for each class.


## Project structure

The exact structure depends on the files included. A project of this type commonly contains some of the following:

```text
    URL Detection System
    ├── app.py          
    ├── features.py      
    ├── train_model.py       
    ├── templates/
    |   └──index.html       
    ├── static/
    |   ├──script.js
    |   └──style.css      
    ├── phishing_urls.csv
    ├── advanced_phishing_urls.csv
    ├── models.pkl
    ├── advanced_model.pkl  
    ├── requirements.txt
    └── README.md
```


## Limitations

- The model's performance depends on the quality and diversity of its training data.

- New or previously unseen phishing techniques may evade detection.

- A high risk score does not prove that a website is malicious, and a low score does not guarantee safety.

- The current feature-based approach does not independently verify domain registration or guarantee that a website is legitimate.

- The system is intended as a security-assistance tool, not a replacement for professional security analysis.


## Disclaimer

This project is intended for educational and defensive cybersecurity purposes. Predictions should be treated as risk indicators rather than definitive proof of a websites's safety or maliciousness.