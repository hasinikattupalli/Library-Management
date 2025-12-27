# 📚 Library Management System

## 🎯 Goal
To create a robust system for managing a library’s collection of books and its registered members. The system ensures:

- 📌 **Unique identifiers** for every book (ISBN) and member (Member ID)
- 📌 **Proper enforcement** of borrowing and return rules
- 📌 **Accurate tracking** of book availability and copies
- 📌 **Clear reporting** of library status and errors

This project showcases **object-oriented programming concepts** such as encapsulation, constructor overloading, data validation, and practical design patterns.

---

## 🛠 Main Modules

### 1️⃣ Book
- Represents an individual book entry.
- Handles borrowing, returning, and copy count adjustments.
- Enforces **unique ISBNs** and ensures available copies are never negative or beyond the set total.

### 2️⃣ Member
- Represents a library user.
- Tracks borrowed books and enforces borrowing limits.
- Supports handling multiple copies of the same book.

### 3️⃣ Library
- Central manager for all books and members.
- Handles addition of books/members with uniqueness checks.
- Coordinates borrowing and returning while applying constraints.
- Provides detailed printing of current library status, books, and members.

---

## 📥 Command Input Format
The system accepts commands in structured form, such as:

```
Book <Title> <Author> <ISBN> <CopiesAvailable> <TotalCopies>
Book None
Book ExistingBook <OldISBN> <NewISBN>
UpdateCopiesCount <ISBN> <NewCount>
Member <MemberID> <Name> <BorrowLimit>
Member NoBorrowLimit <MemberID> <Name>
Borrow <MemberID> <ISBN>
Return <MemberID> <ISBN>
PrintBook <ISBN>
PrintMember <MemberID>
PrintLibrary
Done
```

---

## 📏 Constraints
- Maximum **50 books** in the library
- Maximum **150 members**
- Up to **15 copies** of a single book
- Up to **15 borrowed copies** per member

---

## ✅ Features & Expected Output
The system will:
- Add/manage books and members while keeping identifiers unique
- Borrow/return books within set rules
- Keep book availability updated and safe from errors
- Print details of books, members, or the entire library
- Show clear, descriptive error messages such as:
  ```
  Invalid request! Book with same ISBN already exists
  Invalid request! Borrow limit exceeded
  ```

---

## 📄 Summary
This project demonstrates a fully functional, constraint-driven Library Management System that integrates **OOP principles** with clear, user-friendly input commands.
