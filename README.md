# Web Test Framework - Design Pattern Architecture

[![Build Status](https://img.shields.io/badge/build-passing-brightgreen.svg)]()
[![Java Version](https://img.shields.io/badge/Java-11%2B-blue.svg)]()
[![Selenium Version](https://img.shields.io/badge/Selenium-4.x-green.svg)]()

A robust, scalable, and maintainable Web Test Automation Framework built from scratch to demonstrate enterprise-level design patterns in test automation. 

##  Overview

This repository serves as a blueprint for structuring UI automation frameworks. Rather than writing procedural automation scripts, this framework implements standard software engineering design patterns to ensure the code is DRY (Don't Repeat Yourself), highly readable, and easy to scale across multiple projects or teams.

##  Design Patterns Implemented

*   **Page Object Model (POM):** Separates test logic from UI locators and interactions, making tests readable and reducing maintenance when UI changes occur.
*   **Singleton Pattern:** Ensures only one instance of the WebDriver is created and shared across tests, optimizing resource usage.
*   **Factory Pattern:** Manages the instantiation of different browser drivers (Chrome, Firefox, Edge) dynamically based on execution configurations.
*   **Facade Pattern:** Wraps complex WebDriver interactions (explicit waits, Javascript clicks, scrolling) into simple, reusable action methods.

## Technologies & Tools

*   **Language:** Java 
*   **Automation Tool:** Selenium WebDriver 
*   **Testing Framework:** TestNG / JUnit5
*   **Build Tool:** Maven / Gradle
*   **Assertions:** AssertJ / Hamcrest
*   **Reporting:** Allure / ExtentReports

##  Project Structure

```text
├── src/main/java
│   ├── core           # WebDriver factory, Singletons, and base configurations
│   ├── pages          # Page Object classes (Locators and Actions)
│   ├── utils          # Helper classes (Properties reader, Wait utils, Loggers)
│   └── data           # Test data providers and models
├── src/test/java
│   ├── base           # BaseTest class with Setup/Teardown hooks
│   └── tests          # Actual test classes categorized by feature
├── src/test/resources
│   ├── config.properties # Environment variables and browser selection
│   └── testdata.json     # Externalized test data
└── pom.xml            # Maven dependencies
