---
title: "CS 499 Computer Science ePortfolio"
---

# Computer Science ePortfolio

**[Anteneh Denbel]**
Bachelor of Science in Computer Science — Southern New Hampshire University


---

## About This Portfolio

This ePortfolio is the capstone of my Bachelor of Science in Computer Science at SNHU.
It showcases my growth across the three core areas of the program — **software design
and engineering**, **algorithms and data structures**, and **databases** — through
enhancements made to a single real-world artifact: a Warehouse Inventory Management
Android application originally built in CS 360.

A full professional self-assessment introducing my skills and career goals will appear
here in the final submission.

---

## Professional Self-Assessment

*Coming soon*

---

## Code Review

*Coming soon*

---

## The Artifact

**Warehouse Inventory Management App** — CS 360 (Mobile Architecture and Programming)

An Android application written primarily in Java, with Kotlin used for Jetpack Compose
theming. The app uses Room (SQLite) for local persistence, Material Components for the
UI, a RecyclerView grid of inventory cards, and conditional SMS notifications for
low-stock alerts.

- 🔗 [Original source code](https://github.com/AntenehDenbel/Mobile-Architecture)

---

## Enhancements

### 1. Software Design and Engineering
**Refactor to MVVM + Repository architecture**

Re-architect the monolithic `InventoryActivity` around the Model–View–ViewModel pattern
using Android Jetpack. Extract business logic into an `InventoryViewModel`, centralize
data access in an `InventoryRepository`, remove the `allowMainThreadQueries()`
anti-pattern, migrate Java business logic to Kotlin, introduce Hilt for dependency
injection, and fix the broken delete path in `InventoryAdapter`.


---

### 2. Algorithms and Data Structures
**In-memory indexing with Trie, HashMap, and min-heap**

Add a dedicated `ItemIndex` component between the Repository and ViewModel that
maintains three coordinated data structures: a Trie for prefix search (O(k + m)),
a HashMap for O(1) lookup by ID, and a min-heap for O(log n) low-stock retrieval.
Replaces the current O(n) linear scans over the full item list.


---

### 3. Databases
**Migration from local Room/SQLite to Firebase Firestore**

Replace the local, single-device database with a cloud-backed document store. Adds
real-time multi-device sync, salted BCrypt password hashing (replacing the current
plaintext `User.java`), role-based access control via Firestore security rules, an
immutable audit log, and offline-first caching.


---

## Course Outcomes

This portfolio demonstrates mastery of the five CS 499 course outcomes:

1. **Collaborative environments** — architecture, documentation, and code review
   practices that support team-based development.
2. **Professional-quality communication** — the code review video, written narratives,
   and this portfolio itself.
3. **Algorithmic design and trade-offs** — deliberate data structure choices with
   justified Big-O trade-offs.
4. **Innovative techniques and tools** — modern Android (Jetpack, Kotlin coroutines,
   Hilt) and cloud (Firestore) tooling.
5. **Security mindset** — BCrypt password hashing, server-enforced authorization,
   and audit logging.

---

<sub>Last updated: Module One · CS 499 Capstone</sub>
