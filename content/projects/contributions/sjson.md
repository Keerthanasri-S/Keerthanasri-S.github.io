---
title: "sjson"
link: "https://github.com/techatpark/sjson"
# image: "/img/sjson-logo.png"
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

### Key Features

- **Custom JSON Type Support**:
  - Fully implemented types: `JsonString`, `JsonNumber`, `JsonBoolean`, `JsonNull`, `JsonArray`, and `JsonObjects`.
  - Example: `JsonBoolean` manually reads and validates boolean values (`true`, `false`) character-by-character from input.

- **Manual Stream-Based Parsing**:
  - Uses a custom-built `JsonReader` to read characters directly from input streams.
  - Parsing is done in a recursive-descent style for full understanding of nested structures.

- **Configurable Parse Modes**:
  - Provides `STRICT` and `LAX` parsing modes, offering flexibility for handling edge cases or malformed JSON.

- **Comparison and Testing**:
  - **Jackson** is used in tests to assert correctness of parsed output.
  - Custom `.equals()` and `.hashCode()` methods implemented for deep comparison (avoids relying on `.toString()`).

### Technologies Used

- **Java (Pure Core APIs)**: All parsing logic written using only core Java (`Reader`, `char[]`, etc.).
- **JUnit 5**: Unit testing framework used to verify parser behavior.
- **Jackson Databind**: Used only in test cases to validate the correctness of parsed data.
- **Git & GitHub**: Code collaboration with issues, branches, pull requests, and CI.
- **Modular Design**: Each JSON type (`JsonBoolean`, `JsonNumber`, etc.) is implemented as a separate class for clarity and testing.

This project is a great example for those wanting to dive deep into how JSON works, or for environments where using full libraries would be overkill.

> Project Link: [techatpark/sjson](https://github.com/techatpark/sjson)
