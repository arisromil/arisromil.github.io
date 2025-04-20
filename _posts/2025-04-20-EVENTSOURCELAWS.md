---
title: Laws of Event Sourcing
date: 2025-04-20 00:00:00 0000
categories: [software]
tags: [design]     # TAG names should always be lowercase
---


- All Events Are Immutable and Past Tense

- Applying a Failure Event Must Always Return the Previous State

- All Data Required for a Projection Must Be on the Events

- Work Is a Side Effect

- All Projections Must Stem from Events

- Never Manage More than One Flow per Process Manager

- Process Managers Must Not Read from Projections

- Event Schemas Are Immutable

- Different Projectors Cannot Share Projections

- Never Test Internal State