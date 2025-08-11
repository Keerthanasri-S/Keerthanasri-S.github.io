---
title: 'Blogs'
date: Wed, 24 Jul 2025 18:10:00 +0530
draft: false
tags: [java, json, boolean, parsing, open source, contribution, sjson]
---

I contributed to the `sjson` project by adding support for JSON boolean values like `true` and `false`. I introduced a `JsonBoolean` class and implemented character-by-character parsing using a helper method. Earlier, the parser failed to recognize booleans, but now it handles them correctly as per the JSON spec.

### Why Booleans Matter in JSON

Booleans (`true`, `false`) are core JSON values — lowercase, without quotes. Values like `"true"`, `1`, or `FALSE` are invalid as booleans. Supporting them is essential for reading any valid JSON structure.


