# Hotel Booking Prediction Project

## Project Overview
This project analyzes hotel booking data and predicts whether a booking will be canceled (`is_canceled`) using machine learning.  
The dataset includes booking details such as guest information, stay duration, ADR (Average Daily Rate), and booking channels.  

**Key Features of the Project:**
- Exploratory Data Analysis (EDA) with missing value and outlier detection
- Data Cleaning and Feature Engineering
- Categorical Encoding (One-Hot and Frequency Encoding)
- Outlier Handling and Data Leakage Prevention
- Train-Test Split for model preparation

---

## Dataset
- Source: [Include link if using Kaggle or other dataset source]  
- Columns include: `hotel`, `lead_time`, `arrival_date_year`, `adults`, `children`, `babies`, `meal`, `market_segment`, `distribution_channel`, `adr`, `is_canceled`, and more.

---

## Project Structure
hotel_booking_project/
│
├── data/
│ └── hotel_bookings.csv # Raw dataset
│
├── notebooks/
│ ├── Phase1_EDA.ipynb # Exploratory Data Analysis
│ └── Phase2_Cleaning.ipynb # Data Cleaning & Feature Engineering
│
├── src/
│ └── preprocessing.py #encoding scripts
│
├── README.md # Project description
└── requirements.txt # Required Python packages

---

## Setup & Installation
1. Clone the repository:
```bash
git clone https://github.com/yourusername/hotel_booking_project.git
cd hotel_booking_project
Data Cleaning & Preprocessing

Handle missing values:

children → filled with median

country → filled with mode or grouped into "Other"

company & agent → filled with 0

Remove duplicate rows

Handle outliers:

Cap extreme values (e.g., adr > 1000 set to 1000)

Create new features:

total_guests = adults + children + babies

total_nights = stays_in_weekend_nights + stays_in_week_nights

is_family flag for bookings with children or babies

Encode categorical variables:

One-Hot Encoding for low-cardinality features

Frequency encoding or grouping for high-cardinality features

Remove data leakage columns: reservation_status and reservation_status_date

Split dataset into training and testing sets (test_size=0.2, random_state=42)
Usage

After preprocessing, you can use the cleaned dataset to:

Train machine learning models to predict booking cancellations

Analyze factors influencing cancellations

Build dashboards for hotel management insights

Dependencies

Python 3.8+

pandas

numpy

matplotlib

seaborn

scikit-learn

Install all dependencies:
pip install pandas numpy matplotlib seaborn scikit-learn 

Author

Nada Maher Mohamed Elhady
Email: mahernada562@gmail.com
LinkedIn: https://www.linkedin.com/in/nada-maher-9b7327285/
