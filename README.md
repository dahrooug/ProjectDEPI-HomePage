# 🛒 LambdaTest Automation Project

A robust Test Automation Framework built with **Java**, **Selenium WebDriver**, and **TestNG**, designed to automate and validate end-to-end user workflows for the Shopping Cart functionality on the **LambdaTest E-Commerce Playground**.

This project was developed as part of the **DEPI (Digital Egypt Pioneers Initiative)** training program, applying industry-standard design patterns like **Page Object Model (POM)** to ensure clean, maintainable, and scalable test code.

---

## 📌 Project Overview

The primary objective of this project is to automate functional and edge-case testing for the E-Commerce Shopping Cart module. It covers authenticating users, managing products, dynamically updating cart quantities via UI components (buttons, manual inputs, boundary testing), verifying price calculations, and testing shopping cart state transitions.

---

## 🛠️ Tech Stack & Tools

* **Programming Language:** Java 17
* **Automation Framework:** Selenium WebDriver (v4.40.0)
* **Test Runner / Assertions:** TestNG (v7.11.0)
* **Build Tool:** Apache Maven
* **Browser:** Mozilla Firefox (`FirefoxDriver`)
* **Design Pattern:** Page Object Model (POM)

---

## 📁 Project Architecture & Structure

```text
ProjectDEPI-HomePage/
│
├── src/
│   ├── main/java/pages/
│   │   ├── HomePage.java             # Web elements & actions for Home Page
│   │   ├── LoginPageProject.java     # Web elements & login flow
│   │   └── ShoppingCartPage.java     # Web elements & actions for Cart Page
│   │
│   └── test/java/
│       ├── projectDEPI/
│       │   └── BaseTest.java         # WebDriver setup, teardown & pre-test login hooks
│       └── tests/
│           └── ShoppingCartTest.java # Functional & boundary test execution scripts
│
├── pom.xml                           # Maven dependencies & build setup
└── README.md                         # Project documentation
````

---

## 🧪 Automated Test Scenarios (`ShoppingCartTest`)

The framework covers both positive user flows and negative/boundary validation cases:

| #  | Test Scenario                                | Description                                                                                               |
| -- | -------------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| 1  | `validAddOneProductToTheCart`                | Verifies adding a single product to the cart and checks the badge counter update.                         |
| 2  | `validMultipleAddProduct`                    | Validates adding multiple distinct items to the cart and verifies overall item count.                     |
| 3  | `removeProduct`                              | Tests removing a single item from the cart and verifies updated cart status.                              |
| 4  | `emptyTheCart`                               | Validates emptying the cart completely, verifying empty-state UI messages and button references.          |
| 5  | `continueShoppingFromTheCartAfterAddProduct` | Verifies navigation behavior when choosing to continue shopping from the cart.                            |
| 6  | `continueShoppingFromTheCartEmpty`           | Verifies the "Continue" navigation flow from an empty cart.                                               |
| 7  | `verifySubTotal`                             | Asserts that subtotal prices calculate accurately upon adding items.                                      |
| 8  | `verifyTotalUpdate`                          | Asserts the final order total matches expected values after item modifications.                           |
| 9  | `increaseProductQuantity`                    | Tests quantity spinner controls (increasing quantity) before cart submission.                             |
| 10 | `decreaseProductQuantity`                    | Tests decreasing quantity and manual input updates on the cart page.                                      |
| 11 | `invalidDecreaseProductQuantityMinus`        | **Negative Test:** Inputs negative quantity values (`-5`) to verify robust input handling and resilience. |
| 12 | `invalidDecreaseProductQuantityZero`         | **Negative Test:** Inputs `0` quantity to test empty edge-case handling.                                  |

---

## 🚀 Getting Started

### Prerequisites

1. **Java Development Kit (JDK 17+)** installed and configured in your environment.
2. **Apache Maven** installed.
3. **Mozilla Firefox** browser installed on your machine.
4. An IDE like **IntelliJ IDEA** or **Eclipse**.

### Installation & Setup

1. **Clone the repository:**
   `git clone https://github.com/dahrooug/ProjectDEPI-HomePage.git`

2. **Navigate to the project directory:**
   `cd ProjectDEPI-HomePage`

3. **Install Maven dependencies:**
   `mvn clean install -DskipTests`

---

## ⚙️ Running the Tests

You can execute the test suite directly via Maven CLI or through your preferred IDE.

* **Via Maven Command Line:** `mvn clean test`
* **Via IDE:** Navigate to `src/test/java/tests/ShoppingCartTest.java`, right-click on the class or individual test methods, and select **Run 'ShoppingCartTest'**.

---

## 👤 Author

* **Mohamed Mahmoud (Dahrooug)** — *Software Quality Assurance & Automation Tester*
* **GitHub:** [@dahrooug](https://github.com/dahrooug)

---

*Developed with ❤️ as part of the Digital Egypt Pioneers Initiative (DEPI).*
