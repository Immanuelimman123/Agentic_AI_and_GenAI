# STREAMLIT MODEL:
# 🛍️ ShopPulse – E-Commerce & Product Operations Dashboard

A modern, interactive **E-Commerce Analytics Dashboard** built using Python and Streamlit to monitor business performance, analyze sales trends, understand customer behavior, track product performance, and manage inventory and orders.

ShopPulse transforms synthetic e-commerce datasets into meaningful business insights through interactive visualizations, dynamic filters, and analytical reports.

---

## 🚀 Features

### 📊 1. Business Overview
- Monitor total revenue, orders, profit, and customers.
- Visualize monthly revenue trends.
- Analyze category-wise sales performance.
- Explore regional revenue distribution.
- Track order status distribution.

### 📈 2. Sales Analytics
- Analyze total revenue and profit.
- Monitor monthly sales performance.
- Compare sales across different regions.
- Analyze payment method distribution.
- Track order status and sales performance.

### 📦 3. Product Analytics
- Identify the top 10 revenue-generating products.
- Analyze best-selling products by quantity.
- Compare category-wise revenue and profit.
- View detailed product performance.
- Download product analytics reports in CSV format.

### 👥 4. Customer Analytics
- Monitor total and repeat customers.
- Analyze average customer spending.
- Identify the highest-spending customers.
- Understand one-time and repeat purchase behavior.
- Explore customer distribution by region.
- Download customer analytics reports in CSV format.

### 🏬 5. Inventory Management
- Monitor available stock levels.
- Identify low-stock and out-of-stock products.
- Calculate total inventory value.
- Analyze stock distribution by category.
- Search products by name or product ID.
- Generate low-stock alerts.

### 🧾 6. Order Management
- Search orders using Order ID, Customer ID, or Product Name.
- Sort orders by date and revenue.
- Filter orders using global dashboard filters.
- Browse order records with pagination.
- View individual order details.
- Analyze order revenue and profit.

---

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| Streamlit | Interactive dashboard development |
| Pandas | Data manipulation and analysis |
| NumPy | Numerical operations and synthetic data generation |
| Plotly Express | Interactive data visualizations |
| CSV | Dataset storage |

---

## 📁 Project Structure

```text
ShopPulse/
│
├── app.py
├── generate_data.py
├── requirements.txt
│
├── data/
│   ├── orders.csv
│   ├── customers.csv
│   ├── products.csv
│   └── inventory.csv
│
└── README.md
```

---

## 📂 Dataset Information

The project uses reproducible synthetic datasets generated using NumPy and Python's random module.

| Dataset | Records | Description |
|---|---:|---|
| orders.csv | 10,000 | Order-line records covering 2025 |
| customers.csv | 2,500 | Synthetic customer information |
| products.csv | 100 | Product and pricing information |
| inventory.csv | 100 | Product stock and inventory details |

**Note:** All datasets contain fictional records and are intended for dashboard development, learning, and practice purposes.

---

## ⚙️ Installation & Setup

Follow these steps to run ShopPulse on your local machine.

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/ShopPulse.git
```

### 2. Navigate to the Project Directory

```bash
cd ShopPulse
```

### 3. Create a Virtual Environment

```bash
python -m venv venv
```

### 4. Activate the Virtual Environment

**Windows:**

```bash
venv\Scripts\activate
```

**macOS / Linux:**

```bash
source venv/bin/activate
```

### 5. Install Dependencies

```bash
pip install -r requirements.txt
```

### 6. Generate Synthetic Datasets

```bash
python generate_data.py
```

This generates the required CSV files inside the `data/` directory.

### 7. Run the Streamlit Application

```bash
streamlit run app.py
```

The dashboard will open in your default browser.

Default local URL:

```text
http://localhost:8501
```

---

## 📦 Requirements

The project uses the following Python libraries:

```text
streamlit>=1.50
pandas>=2.2
numpy>=2.0
plotly>=5.24
```

---

## 🎯 Dashboard Capabilities

- Interactive multi-page navigation.
- Global region, category, and order-status filters.
- Custom date-range filtering.
- URL query parameter support for page and region selection.
- Dynamic KPI calculations.
- Interactive Plotly charts.
- Searchable product and order records.
- Paginated order tables.
- CSV report downloads.
- Reproducible synthetic data generation.

---

## 🔮 Future Enhancements

- Integration with real-time e-commerce databases.
- Advanced sales forecasting using Machine Learning.
- Customer segmentation using clustering algorithms.
- Automated inventory replenishment recommendations.
- Product recommendation system.
- User authentication and role-based access control.
- Cloud deployment and live dashboard hosting.

---

## 🤝 Contributing

Contributions are welcome!

If you would like to improve ShopPulse:

1. Fork the repository.
2. Create a new feature branch.
3. Commit your changes.
4. Push the branch to your fork.
5. Submit a Pull Request.

---

## 📜 License

This project is intended for educational, learning, and portfolio purposes.

You may add an MIT License if you want to distribute the project under that license.

---

## 👨‍💻 Author

**Immanuel**

GitHub: [GitHub Repository](https://github.com/Immanuelimman123/ShopPulse)

---

⭐ If you find this project useful, consider giving the repository a star!

**Built with Python, Streamlit, Pandas, NumPy, and Plotly.**
