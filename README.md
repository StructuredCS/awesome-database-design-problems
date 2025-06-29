# Awesome Database Design Problems

## Table of Contents

- [Introduction](#-introduction)
- [Who This Is For](#-who-this-is-for)
- [How to Use This Repository](#-how-to-use-this-repository)
- [Table of Problems](#-table-of-problems)
- [Contributing](#-contributing)
- [Attribution & Sources](#-attribution--sources)

## 📘 Introduction

Welcome! This is a curated and growing collection of high-quality, real-world **database design challenges**. It's built for anyone who wants to go beyond just writing SQL and focus on the **core skill of data modeling**.

The problems here are drawn from textbooks, university assignments, industry-inspired scenarios, and original case studies. The goal is to provide a **practical, structured way to master relational schema design** — moving past simple queries into thoughtful, real-world modeling decisions.

Each problem includes a sample solution, typically in the form of an **ER diagram using Crow’s Foot notation**. Why Crow’s Foot? Because it’s clear, widely recognized, and supported by most professional database design tools. It provides an intuitive visual language for modeling entities, attributes, and relationships.

If you're interested in understanding the **why** behind these designs — the tradeoffs, the design principles, and the relational theory — check out [this **open-access lecture series** on YouTube](https://www.youtube.com/playlist?list=PL3fg3zQpW0k4UO9eBDLdroADnB18ZAOgj). This video series is based on the book [*Grokking Relational Database Design*](https://mng.bz/PRER), and explores the reasoning behind good schema design, including normalization, cardinality, keys, and common pitfalls.

## 🎯 Who This Is For

- 🧑‍🎓 Computer science and software engineering students
- 👨‍🏫 Educators looking for teaching materials or assignments
- 💼 Developers preparing for system design or database interviews
- 🧪 Self-learners seeking structured practice with schema design

## 🛠️ How to Use This Repository

1. **Choose a problem**: Pick a problem that interests you from [the problem list](# Problems).
2. **Read the problem statement**: Understand the requirements, entities, attributes, relationships, and extra information provided.
3. **Design the schema**: Create an ER diagram or SQL schema based on the problem.
4. **Review the sample solution**: If you get stuck, refer to the provided sample solution (if available).
5. **Discuss solutions**: If available, [review the provided solutions or discuss with peers](https://github.com/StructuredCS/awesome-database-design-problems/discussions).

## 📋 Table of Problems

| Title                        | Domain        | Difficulty | Source / Credit                            |
|------------------------------|---------------|------------|---------------------------------------------|
| [Library Lending System](problems/library-system.md) | Education | Easy | [Fundamentals of Database Systems](https://www.pearson.com/en-us/subject-catalog/p/fundamentals-of-database-systems/P200000003546) |
| [Bookstore Inventory System](problems/bookstore-system.md) | Retail | Medium | [Database System Concepts](https://db-book.com/)   |
| [The Sci-Fi Collective](problems/The-Sci-fi-collective.md) | E-commerce | Medium | [Grokking Relational Database Design](https://mng.bz/PRER) |
| [SHIPS R US](problems/SHIPS-R-US.md) | Manufacturing | Medium | [Grokking Relational Database Design](https://mng.bz/PRER) |
| [University Course System](problems/university-system.md) | Education | Hard | [Database System Concepts](https://db-book.com/) |

## 🤝 Contributing

If you have a database design problem you'd like to contribute, please follow these steps:

1. **Fork the repository**: Create your own copy of the repo.
2. **Add your problem**: Create a new markdown file in the root directory with a clear title.
3. **Follow the format**: Use [the given template](format.md) for structure.
4. **Include references**: If your problem is based on a textbook or course, provide proper attribution.
5. **Submit a pull request**: Once your problem is ready, submit a PR for review.
6. **Engage with feedback**: Be open to suggestions and improvements from the community.

Please note that your solution sample should adopt the Crow's Foot notation for ER diagrams.

## 🏷 Attribution & Sources

All problems include attribution when adapted from books, courses, or websites. This repo is educational and open-access; original sources retain their copyright. If you're the original author of a referenced problem and want it removed or reworded, please open an issue.

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## 👤 About the Maintainer

This repository is maintained by [Dr. Qiang Hao](https://qhao.info/), a Computer Science professor and the lead author of [*Grokking Relational Database Design*](https://mng.bz/PRER). You can find more of his teaching at [his YouTube channel @StructuredCS](https://www.youtube.com/@structuredcs).