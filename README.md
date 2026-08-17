# Fast-Food Billing & Inventory Management System

A Desktop Application built using **Java Swing** and **NetBeans IDE** for managing fast-food restaurant orders, price updates, and stock inventory. Data persistence is handled via a lightweight CSV file (`restaurant_billing.csv`).

## 🚀 Features

* **Billing & Order Management:** Calculate order totals, unit prices, tax, and change for menu items (Pizza, Burger, Fries, Sandwich).
* **Admin Price Panel (`NewJDialog`):** Real-time update for menu item unit prices with input validation (decimal support and leading-zero cleaning).
* **Admin Stock Panel (`stockqty`):** Real-time inventory tracking and stock updates with strict integer validation.
* **CSV Data Persistence:** Saves stock levels, unit prices, and transaction records to `restaurant_billing.csv`.

---

## ⚠️ IMPORTANT: CSV File Path Configuration

> **CRITICAL REQUIREMENT:** The application reads and writes data to `restaurant_billing.csv`. **You MUST manually set/update the `.csv` file path in the source code before running the application.** If the file path is not configured correctly, data will NOT save or load!

### How to set the file path:
1. Open the project in **NetBeans IDE**.
2. Locate the file handling logic in `billing_systems.java`, `NewJDialog.java`, and `stockqty.java`.
3. Find the `File` object path declaration (e.g., `File file = new File("...");` or inside `BufferedReader`/`BufferedWriter`).
4. Replace the existing path string with the correct path on your local computer:
   ```java
   // Example for Windows (Absolute Path):
   File file = new File("C:\\Users\\YourUsername\\Documents\\restaurant_billing.csv");

   // Example for Relative Path:
   File file = new File("src/restaurant_billing.csv");
   ```
5. Save all updated files and re-compile the project before testing.

---

## 🛠️ Tech Stack & Requirements

* **Language:** Java (JDK 8 or higher)
* **GUI Framework:** Java Swing / AWT
* **IDE:** NetBeans IDE
* **Storage:** CSV (`restaurant_billing.csv`)

---

## 📁 Project Structure

```text
├── billing_system/
│   ├── billing_systems.java    # Main Billing UI & Calculation Engine
│   ├── NewJDialog.java         # Admin Panel - Unit Price Update
│   ├── stockqty.java           # Admin Panel - Stock Quantity Update
│   └── restaurant_billing.csv  # Database file for Prices & Stock
└── README.md                   # Project Documentation
```

---

## 💻 How to Run

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/your-username/your-repo-name.git
   ```
2. **Open in NetBeans:**
   * Open NetBeans IDE.
   * Navigate to `File` > `Open Project` and select the cloned folder.
3. **Set CSV File Path:**
   * Update the path as mentioned in the [IMPORTANT](#-important-csv-file-path-configuration) section.
4. **Build and Run:**
   * Right-click `billing_systems.java` in the Projects tab.
   * Click **Run File** (or press `Shift + F6`).

---

## 📝 License & Info
Developed for Fast-Food Restaurant Management. Feel free to clone and customize!
