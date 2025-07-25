---
title: "sjson"
link: "https://github.com/techatpark/sjson"
image: "/img/sjson-logo.png.jpeg"
description: "A custom-built lightweight JSON parser implemented from scratch in Java"
featured: true
tags: ["Java", "Parser", "Custom JSON", "JUnit", "Jackson"]
fact: "Build your own JSON parser and understand the internals of data parsing."
weight: 110
sitemap: 
    priority: 0.8
---

**sjson** is an open-source project aimed at building a **lightweight JSON parser** completely from scratch in Java, without depending on libraries like `org.json`, `Gson`, or `Jackson` for parsing. It’s a low-level educational tool designed to give full control over how JSON data is read, interpreted, and validated.

The project supports complete JSON parsing capabilities with custom classes for each type and uses **Jackson** only in unit tests as a reference to validate correctness.

###  My Contribution

I implemented the logic to **parse JSON boolean values** — converting `true` and `false` in the raw JSON into structured `JsonBoolean` objects. This involved handling character-level parsing using a `Reader` and ensuring accurate type conversion and validation within the custom parser framework.

### Technologies Used

- **Java (Pure Core APIs)**: All parsing logic written using only core Java (`Reader`, `char[]`, etc.).
- **JUnit 5**: Unit testing framework used to verify parser behavior.
- **Jackson Databind**: Used only in test cases to validate the correctness of parsed data.
- **Git & GitHub**: Code collaboration with issues, branches, pull requests, and CI.
- **Modular Design**: Each JSON type (`JsonBoolean`, `JsonNumber`, etc.) is implemented as a separate class for clarity and testing.

This project is a great example for those wanting to dive deep into how JSON works, or for environments where using full libraries would be overkill.

> 🔗 Project Link: [techatpark/sjson](https://github.com/techatpark/sjson)
