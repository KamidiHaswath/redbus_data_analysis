🚌 RedBus Seat Count Prediction Analysis
📌 Project Overview
This repository contains a machine learning solution for predicting bus seat occupancy for RedBus, a leading online bus ticketing platform. The objective is to forecast the final seat count for specific bus routes on given dates, aiding in smarter operational decisions.

📂 Dataset Overview
The analysis utilizes three key datasets:

🔹 1. Train Dataset (train.csv)
Records: 67,200

Contains route and date information (doj, srcid, destid)

Target variable: final seat count

🔹 2. Test Dataset (test.csv)
Records: 5,900

Similar to train data, but without the target variable

Used for model inference and generating predictions

🔹 3. Transactions Dataset (transactions.csv)
Records: 2,266,100

Granular transaction-level data

Includes features like bus_type, fare, seat_capacity, ratings, booked seats

🛠️ Feature Engineering
Key features derived for improved predictive performance:

Time-based Features:

Day of week

Month

Weekend/holiday indicators

Route-level Aggregations:

Average final seat counts

Route popularity metrics

Historical fare statistics

Bus Characteristics:

Bus type encoding (AC, Non-AC, Sleeper, etc.)

Operator ratings

Seat capacity

🤖 Machine Learning Approach
🔍 Model Used: LightGBM (Light Gradient Boosting Machine)
Handles large datasets efficiently

Supports categorical variables natively

Provides feature importance for interpretability

Robust to missing values

📈 Validation Strategy
Train-validation split based on journey date

Evaluation Metric: Root Mean Square Error (RMSE)

Achieved RMSE: ~479.5 on validation data

🧠 Business Use Cases
Predictions from this model can support:

📊 Dynamic Pricing — Adjust ticket prices based on forecasted demand

🧭 Route Planning — Allocate more buses to high-demand routes

🪑 Inventory Management — Optimize seat allocation and avoid under/overbooking

💰 Revenue Optimization — Maximize seat utilization and profitability

💻 Tech Stack
Language: Python

Libraries:

pandas, numpy – data processing

scikit-learn – preprocessing & evaluation

lightgbm – model training

matplotlib, seaborn – data visualization

Environment: Jupyter Notebook

Output: CSV file for submission (submission.csv)

🚀 How to Run
Clone the repository:

bash
Copy
Edit
git clone https://github.com/<your-username>/redbus-seat-prediction.git
cd redbus-seat-prediction
Install dependencies:

bash
Copy
Edit
pip install -r requirements.txt
Run the notebook:

bash
Copy
Edit
jupyter notebook notebooks/RedBus_Prediction.ipynb
Output will be saved as submission.csv

📊 Sample Output
ID	Predicted Final Seat Count
1001	38
1002	52
...	...

📎 Repository Structure
bash
Copy
Edit
📁 redbus-seat-prediction/
│
├── 📁 data/                  # Raw datasets (not included in repo)
├── 📁 notebooks/
│   └── RedBus_Prediction.ipynb
├── 📁 models/                # Saved model files
├── 📁 utils/                 # Feature engineering, preprocessing scripts
├── submission.csv           # Final prediction file
├── requirements.txt
└── README.md
📬 Contact
For questions or collaborations, feel free to connect:

Author: Kamidi Haswath

Email: kamidihaswath@example.com

LinkedIn: linkedin.com/in/haswath

⭐ Acknowledgements
Thanks to the RedBus Data Decode Hackathon team for providing the dataset and challenge!
