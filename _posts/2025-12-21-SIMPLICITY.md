---
title: From the book "Simplicity"
date: 2025-12-21 00:00:00 0000
categories: [book]
tags: [design]     # TAG names should always be lowercase
---

> You dont need libraries or design patterns to write a state machine

> Look for opportunities to transition to a more data driven style, e.g.
- repetitive stanzas of code that differ by a few values, make it list driven
- where a sequence of actions are taken, and that sequence changes depending on the circumstances, could be implmented as a simple interpreter
- to handle a stream of incoming events, and prior events affect the processing of next, then look into state machines

> `S` is simpler than `C` if:
- `S` is easier to understand than `C`
- `S` has fewer parts than `C`
- `S` reflects the problem more directly than `C`



