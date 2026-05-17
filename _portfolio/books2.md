---
title: "Python Kivy Application — Books to Read 2.0"
date: 2025-04-01
excerpt: "OOP refactor of Books to Read into a Kivy GUI with dynamic book buttons, sort spinner, and JSON storage — CP1404 Programming II, T3 2025."
header:
  teaser: books2.png
collection: portfolio
---

**Course:** CP1404 Programming II — Trimester 3, 2025 — James Cook University, Cairns  
**Tools & Equipment:** Python, Kivy, PyCharm, GitHub, JSON file I/O  
**Source Code:** [github.com/quochuynh1/a2-books](https://github.com/quochuynh1/a2-books)

## Objective

Extend the Books to Read 1.0 console program into a Kivy-based GUI application using object-oriented design, replacing the list-of-lists data structure with custom `Book` and `BookCollection` classes and switching from CSV to JSON storage.

## What I Did

- Refactored the flat data structure into two OOP classes — `Book` (encapsulating title, author, pages, and completion status with methods like `mark_completed()`, `mark_unread()`, and `is_long()`) and `BookCollection` (managing the list with load, save, sort, add, and page-count methods)
- Switched persistent storage from CSV to JSON, updating load and save logic within `BookCollection` to serialise and deserialise `Book` objects
- Built a Kivy GUI with dynamically generated book buttons — colour-coded cyan for unread and grey for completed — that toggle read/unread status on press and update a live page count at the top of the screen
- Implemented a sort spinner allowing the user to sort books by title, author, pages, or completion status in real time, and added input validation for the add-book fields with user feedback via a status label

## Outcome

Delivered a fully functional GUI application demonstrating end-to-end OOP design and Kivy UI development. Gained hands-on experience with class design, separation of concerns between data model and UI, event-driven programming, and JSON serialisation.
