🛒Customer Retail Classification

A machine learning project that classifies customer transactions by country using retail invoice data. Three classification models are compared: Logistic Regression, Decision Tree, and K-Nearest Neighbors (KNN).

📁 Dataset

File: customer_retail.csv

The dataset contains online retail transaction records with the following columns:
ColumnTypeDescriptionInvoiceNoobjectUnique invoice identifierStockCodeobjectProduct codeDescriptionobjectProduct descriptionQuantityint64Number of units purchasedInvoiceDatedatetimeDate and time of transactionUnitPricefloat64Price per unit (£)CustomerIDfloat64Unique customer identifierCountryobjectCountry of the customer

Total records: 541,909
After dropping nulls: ~406,829 usable rows


🔧 Preprocessing

Dropped rows with missing values (dropna())
Selected features: Quantity, UnitPrice
Target variable: Country (label-encoded using LabelEncoder)
Train/test split: 80% / 20%, random_state=42


🤖 Models & Results
ModelAccuracyLogistic Regression88.97%Decision Tree89.03%K-Nearest Neighbors88.42%

Note: The high accuracy is largely driven by class imbalance — United Kingdom dominates the dataset (~90% of transactions).


📊 Visualizations

Scatter Plot — Quantity vs. Unit Price distribution across transactions
Bar Chart — Accuracy comparison across all three models
