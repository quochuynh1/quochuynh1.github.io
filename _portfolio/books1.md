---
title: "Python Console Program — Books to Read 1.0"
excerpt: "Command-line book tracker in Python with CSV persistence, modular design, and robust input validation — CP1404 Programming II, T3 2025."
header:
  teaser: books1.png
collection: portfolio
---

**Course:** CP1404 Programming II — Trimester 3, 2025 — James Cook University, Cairns  
**Tools & Equipment:** Python, PyCharm, GitHub, CSV file I/O  
**Source Code:** [github.com/quochuynh1/a1-books](https://github.com/quochuynh1/a1-books){:target="_blank"}

![Cover Photo](/images/books1.png){: style="border-radius: 8px"}

## Objective

Design and implement a command-line book tracking application in Python that allows the user to load, display, add, and mark books as completed, with persistent CSV-based storage.

## What I Did

- Designed a modular program structure with separate functions for loading, saving, displaying, adding, and completing books, keeping `main()` as a clean menu-driven loop
- Implemented dynamic column-width formatting so book titles, authors, and page counts align neatly regardless of data length; sorted output alphabetically by author then title
- Built robust input validation for all user entries — blank string rejection, integer range checking, and `IndexError` handling for invalid book selection
- Managed persistent CSV storage — loading books on startup and saving all changes on quit; tracked read/unread status with a status flag and provided a running total of unread pages and books

## Gallery 🖼️
<div style="display: grid; grid-template-columns: repeat(2, 1fr); gap: 12px; margin-top: 12px;">

  <figure style="margin: 0;">
    <img src="/images/a1books/addbooks.png" alt="Adding a book" style="width: 100%; border-radius: 6px;">
    <figcaption style="font-size: 0.75rem; color: #888; margin-top: 4px; text-align: center;">Adding a new book</figcaption>
  </figure>

  <figure style="margin: 0;">
    <img src="/images/a1books/completebooks.png" alt="Completing a book" style="width: 100%; border-radius: 6px;">
    <figcaption style="font-size: 0.75rem; color: #888; margin-top: 4px; text-align: center;">Marking a book as completed</figcaption>
  </figure>

  <figure style="margin: 0;">
    <img src="/images/a1books/abc.png" alt="Input validation" style="width: 100%; border-radius: 6px;">
    <figcaption style="font-size: 0.75rem; color: #888; margin-top: 4px; text-align: center;">Input validation in action</figcaption>
  </figure>

  <figure style="margin: 0;">
    <img src="/images/a1books/def.png" alt="Saving and quitting" style="width: 100%; border-radius: 6px;">
    <figcaption style="font-size: 0.75rem; color: #888; margin-top: 4px; text-align: center;">Saving to CSV on quit</figcaption>
  </figure>

</div>

## Outcome

Delivered a fully functional console program with clean modular design and thorough input validation. Developed practical experience in Python file I/O, data structures (lists of lists), exception handling, and applying software design principles (SRP, DRY) in a real assignment context.
