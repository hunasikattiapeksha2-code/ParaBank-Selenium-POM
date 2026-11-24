# ParaBank Selenium POM Automation

An end-to-end UI test automation framework built with **Java**, **Selenium WebDriver**, **JUnit 5**, and **Maven** using the **Page Object Model (POM)** design pattern for the [ParaBank](https://parabank.parasoft.com/parabank/index.htm) demo banking web application.

## Project Architecture & Structure

The framework separates page locators and user interactions from test assertions for maintainability and reusability:

```text
parabank-web-selenium/
├── src/test/java/
│   └── com/parasoft/parabank/
│       ├── PageObject.java        # Base page initialization & WebDriver utilities
│       ├── register/
│       │   ├── RegisterPage.java  # User registration form locators & actions
│       │   └── RegisterTest.java  # Test cases for new customer registration
│       ├── overview/
│       │   ├── OverviewPage.java  # Account overview page elements & methods
│       │   └── OverviewTest.java  # Test cases verifying account balances & details
│       └── home/
│           └── HomeTest.java      # Login & home page validation tests
└── pom.xml                        # Maven dependencies & build configuration
```

## Tech Stack & Prerequisites

- **Java Development Kit (JDK):** 11 or higher
- **Build & Dependency Management:** Maven 3.8.1+
- **Browser Automation:** Selenium WebDriver 4.9.0+
- **Test Runner:** JUnit 5 (Jupiter) 5.9.3+
- **Browser Driver:** Google Chrome & matching ChromeDriver (managed automatically via Selenium Manager)

## Getting Started

### 1. Clone the Repository
```bash
git clone [https://github.com/hunasikattiapeksha2-code/ParaBank-Selenium-POM.git](https://github.com/hunasikattiapeksha2-code/ParaBank-Selenium-POM.git)
cd ParaBank-Selenium-POM/parabank-web-selenium
```

### 2. Run All Tests via Maven
```bash
mvn clean test
```

### 3. Run Individual Tests in Eclipse
1. Import the project into Eclipse as an **Existing Maven Project**.
2. Navigate to `src/test/java` and open any test class (such as [`RegisterTest.java`](src/test/java/com/parasoft/parabank/register/RegisterTest.java) or [`OverviewTest.java`](src/test/java/com/parasoft/parabank/overview/OverviewTest.java)).
3. Right-click inside the file and select **Run As → JUnit Test**.

## Automated Scenarios Covered

- **Customer Registration:** Validates form field inputs, account creation confirmation, and error handling for incomplete data.
- **User Authentication:** Verifies valid and invalid login flows on the ParaBank home portal.
- **Account Overview:** Confirms post-login account summary table visibility, account numbers, and balance formatting.

## References

- [ParaBank Demo Application](https://parabank.parasoft.com/parabank/index.htm)
- [Selenium WebDriver Documentation](https://www.selenium.dev/documentation/webdriver/)
- [JUnit 5 User Guide](https://junit.org/junit5/docs/current/user-guide/)
