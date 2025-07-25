---
title: 'Open Source Contribution'
date: Wed, 24 Jul 2025 18:10:00 +0530
draft: false
tags: [java, json, boolean, parsing, open source, contribution, sjson]
---

Intro
-----

Doesn’t matter whether you’re building a toy JSON parser for learning or contributing to a production-ready library — **Boolean values like `true` and `false` are essential parts of JSON parsing**. Without them, the parser would reject even the simplest API response or config file.

In my first open source contribution to the `sjson` project, I added support for parsing Boolean values and introduced a new class: `JsonBoolean`. This small change made the parser smarter, more complete, and compliant with the JSON spec.

What are JSON Booleans?
-----------------------

In JSON, Boolean values come in two forms: `true` and `false`.  
That’s it. No quotes. No extra data. Just those two exact literals.

*   If the parser sees `"true"` or `"false"` (with quotes), it should treat them as strings — not booleans.
*   If it sees `True`, `FALSE`, or `1`, those are **invalid** as booleans in JSON.
*   Proper JSON boolean values are **lowercase only**, and **not wrapped in quotes**.

Before I implemented this, the parser didn't recognize these values. It would either throw an error or treat them as unknown input.

Now that you know what JSON booleans are, here’s how I made the parser support them.

How the Parsing Works
----------------------

When the parser begins reading input, it processes one character at a time.  
So when it encounters the start of a new token, it checks which type of data it is. Here’s what I added:

*   If the first character is `t`, it should try to read the full sequence `true`
*   If the first character is `f`, it should try to read the full sequence `false`
*   If any letter in the sequence doesn't match what's expected, the parser should fail immediately with an error.

I used a helper method called `expect()` to simplify the character-by-character checks.  
For example, to parse `true`, it calls:

