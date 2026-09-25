# Library Management System

A small Object-Oriented Programming (OOP) project that models a library — items, members,
and borrowing/returning logic — built to demonstrate the core pillars of OOP in clean,
readable Python.

### Project Description

This project simulates a basic **Library Management System**. It supports adding
different kinds of library items (`Book`, `DVD`), registering members, and letting
members borrow and return items — with proper validation and error handling for
invalid operations (missing items, unavailable items, unknown members).

### OOP Concepts Used

- **Classes & Objects** — `Book`, `DVD`, `Member`, `Library`, and their instances
- **Encapsulation** — `Member`'s balance is private and only modified through controlled
  methods (`add_fine`, `pay_fine`) and exposed via a read-only property
- **Abstraction** — `LibraryItem` is an abstract base class exposing `describe()` and
  `checkout_period_days()` without revealing implementation details
- **Inheritance** — `Book` and `DVD` inherit shared behavior from `LibraryItem`
- **Polymorphism** — `Library.catalog()` calls `describe()` on every item and gets a
  different result depending on the actual item type
- **Constructors** — every class initializes its state via `__init__`, including
  `super().__init__()` calls in subclasses
- **Exception Handling** — a custom exception hierarchy (`LibraryError`,
  `ItemNotFoundError`, `ItemNotAvailableError`, `MemberNotFoundError`) replaces generic
  errors with clear, specific ones
- **Static / Class Members** — `LibraryItem._total_items` tracks the total number of
  items created across the whole library

### Project Features

- Add library items (`Book`, `DVD`) with type-specific attributes and behavior
- Register members and track their borrowed items
- Borrow and return items with full validation
- Encapsulated member fines (add/pay balance safely, no negative values allowed)
- Polymorphic catalog listing that adapts its output per item type
- Custom, descriptive exceptions instead of generic errors
- Class-level counter for total items created

### How to Run the Project

1. Clone the repository:
```bash
   git clone <repository-url>
   cd <repository-folder>
```
2. Open `Library_Management_System.ipynb` in Jupyter Notebook / JupyterLab / VS Code:
```bash
   jupyter notebook Library_Management_System.ipynb
```
3. Run all cells in order (**Cell → Run All**). No external dependencies are required —
   the project only uses the Python standard library (`abc`).

### Implementation

This project is implemented as a **Jupyter Notebook**.
(The multi-file implementation is considered a bonus and is not included here.)

### Author

**Mohammad Al Mukadam**
