---
title: "Python Kivy Application — Books to Read 2.0"
excerpt: "OOP refactor of Books to Read into a Kivy GUI with dynamic book buttons, sort spinner, and JSON storage — CP1404 Programming II, T3 2025."
header:
  teaser: books2.png
collection: portfolio
---

**Course:** CP1404 Programming II — Trimester 3, 2025 — James Cook University, Cairns  
**Tools & Equipment:** Python, Kivy, PyCharm, GitHub, JSON file I/O  
**Source Code:** [github.com/quochuynh1/a2-books](https://github.com/quochuynh1/a2-books){:target="_blank"}

## Objective

Extend the Books to Read 1.0 console program into a Kivy-based GUI application using object-oriented design, replacing the list-of-lists data structure with custom `Book` and `BookCollection` classes and switching from CSV to JSON storage.

## What I Did

- Refactored the flat data structure into two OOP classes — `Book` (encapsulating title, author, pages, and completion status with methods like `mark_completed()`, `mark_unread()`, and `is_long()`) and `BookCollection` (managing the list with load, save, sort, add, and page-count methods)
- Switched persistent storage from CSV to JSON, updating load and save logic within `BookCollection` to serialise and deserialise `Book` objects
- Built a Kivy GUI with dynamically generated book buttons — colour-coded cyan for unread and grey for completed — that toggle read/unread status on press and update a live page count at the top of the screen
- Implemented a sort spinner allowing the user to sort books by title, author, pages, or completion status in real time, and added input validation for the add-book fields with user feedback via a status label

# Books To Read 2.0 — Feature Screenshots

## 1. Book Tracking

<table>
  <tr>
    <td style="text-align:center;">
      <b>Default</b><br>
      <img src="/images/books2.png" width="240">
    </td>
    <td style="text-align:center;">
      <b>All Completed</b><br>
      <img src="/images/a2books/allbookscomplete.png" width="240">
    </td>
    <td style="text-align:center;">
      <b>None Completed</b><br>
      <img src="/images/a2books/nobookscomplete.png" width="240">
    </td>
  </tr>
</table>

The app displays a running total of unread pages in the header. Books marked as completed appear in a darker tile colour and are excluded from the page count. When all books are completed the total drops to 0.

---

## 2. Dynamic Sorting

<table>
  <tr>
    <td rowspan="2" style="text-align:center;vertical-align:middle;">
      <b>Dropdown</b><br>
      <img src="/images/a2books/dynamicsort.png" width="240">
    </td>
    <td style="text-align:center;">
      <b>By Pages</b><br>
      <img src="/images/a2books/sortbypages.png" width="240">
    </td>
    <td style="text-align:center;">
      <b>By Title</b><br>
      <img src="/images/a2books/sortbytitle.png" width="240">
    </td>
  </tr>
  <tr>
    <td style="text-align:center;">
      <b>By Author</b><br>
      <img src="/images/a2books/sortbyauthor.png" width="240">
    </td>
    <td style="text-align:center;">
      <b>By Completed</b><br>
      <img src="/images/a2books/sortbycompleted.png" width="240">
    </td>
  </tr>
</table>

Clicking "Sort by" reveals the available sort options: Pages, Title, Author, and Completed. This dropdown allows the user to reorder the book list dynamically. This was achieved by using the `Spinner` widget in Kivy.

---

## 3. Adding a Book

<table>
  <tr>
    <td style="text-align:center;">
      <b>Book Added</b><br>
      <img src="/images/a2books/addbooks.png" width="240">
    </td>
  </tr>
</table>

After filling in the Title, Author, and Pages fields and clicking "Add Book", the book appears in the list and the status bar confirms the addition. The page total updates automatically.

---

## 4. Input Validation

<table>
  <tr>
    <td style="text-align:center;">
      <b>Incomplete Form</b><br>
      <img src="/images/a2books/completeallfields.png" width="240">
    </td>
    <td style="text-align:center;">
      <b>Invalid Page Number</b><br>
      <img src="/images/a2books/invalidpageno.png" width="240">
    </td>
  </tr>
</table>

The app validates input before adding a book. If any field is empty the status bar displays "Please complete all fields." If the Pages field contains non-numeric text the status bar displays "Please enter a valid number." The form is not submitted until both conditions are met.

---

## Notes

- Completed books are shown in a **darker tile colour** and labelled `(completed)` — they are excluded from the pages-to-read total.
- The **status bar** (bottom strip) is the primary feedback mechanism for both success messages and validation errors.
- The **page total** in the header updates automatically whenever a book is added or marked complete.


## Outcome

Delivered a fully functional GUI application demonstrating end-to-end OOP design and Kivy UI development. Gained hands-on experience with class design, separation of concerns between data model and UI, event-driven programming, and JSON serialisation.
