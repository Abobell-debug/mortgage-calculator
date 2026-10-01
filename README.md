# Mortgage Calculator

A Java-based mortgage calculator built as part of my journey into object-oriented programming and software design.

The project started as a single-class console application and was progressively refactored into separate classes with clearly defined responsibilities. The goal was not only to make the calculator work, but also to practice writing cleaner, more maintainable, and more object-oriented Java code.

## Overview

The Mortgage Calculator is a console application that collects mortgage information from the user and calculates:

- Monthly mortgage payments
- Remaining mortgage balance throughout the payment period
- A complete payment schedule

The project demonstrates how a procedural-style implementation can be refactored toward a more organized object-oriented design.

## Features

- Accepts the following user inputs:
  - Principal amount
  - Annual interest rate
  - Mortgage period in years
- Validates user input within defined ranges
- Calculates monthly mortgage payments
- Calculates remaining mortgage balances
- Displays a formatted mortgage report
- Displays a payment schedule
- Separates input handling, calculations, and reporting into dedicated classes

## Project Structure

The application is organized into the following classes:

### `MainMortgage`

Acts as the entry point and coordinates the flow of the application.

Responsibilities include:

- Collecting required mortgage information
- Calling the appropriate classes and methods
- Coordinating the overall application flow

### `Console`

Handles interaction with the console.

Responsibilities include:

- Reading user input
- Validating numerical input
- Returning valid values to the calling code

### `MortgageCalculation`

Contains the mortgage calculation logic.

Responsibilities include:

- Calculating the monthly mortgage payment
- Calculating the remaining mortgage balance

### `MortgageReport`

Handles presentation of the calculated results.

Responsibilities include:

- Displaying the monthly mortgage payment
- Displaying the payment schedule
- Formatting monetary values for the user

## Object-Oriented Design

This project was refactored to practice several fundamental object-oriented programming principles and techniques, including:

- Classes and Objects
- Encapsulation
- Abstraction
- Separation of Responsibilities
- Reducing Coupling
- Constructors
- Method Overloading
- Constructor Overloading
- Static Members
- Refactoring toward an Object-Oriented Design

The refactoring process focused on giving each class a clear and specific responsibility rather than placing all application logic inside the `main` method.

## Refactoring Journey

The initial implementation contained user input, mortgage calculations, and report generation inside a single class.

The code was then progressively reorganized into separate classes:

```text
                 MainMortgage
                      |
          +-----------+-----------+
          |           |           |
          v           v           v
       Console   MortgageCalculation   MortgageReport
          |           |           |
       Input      Calculations      Output
