---
title: 'Blogs'
date: Wed, 24 Jul 2025 18:10:00 +0530
draft: false
tags: [java, json, boolean, parsing, open source, contribution, sjson]
---

I contributed to the sjson project by adding support for JSON boolean values like true and false. I created a JsonBoolean class and updated the parser to read these values character by character using a helper method. Earlier, the parser couldn't recognize booleans and failed on such inputs. Now, it correctly parses boolean values as per the JSON specification.



