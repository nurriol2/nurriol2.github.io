---
title:  Today I Learned - Software Versioning Numbers
permalink:  til/versioning-numbers.html
---

Different machine learning projects I'm working on use the same data source, but in different ways. As a result, I'm required to repeat the same data processing steps across multiple projects. Like any programmer, I prefer automation to repetition. So over time, I've built a small collection of convenience programs to automatically handle the repetitive parts. This collection has been so useful to me that I want to release it a Python package for everyone to try. 

Part of maintaining an open source project like this is effectively communicating changes. Software versioning is a numbering scheme that communicates when a change has happened and the severity of the change. You're probably familiar with software versioning if you play any online games. For instance, a game might release an expansion and the version may change from v1.0.0 to v1.1.0. 

Notice, too, that this numbering system provides concise language for talking about different points in time throughout the software's lifecycle. Here's a real example within the `urllib` documentation. 

> `class urllib.request.URLopener(proxies=None, **x509)`  
> Deprecated since version 3.3.

By checking which version of `urllib` is installed for my project, I can easily tell if `URLopoener` is supported.

# Absolute Basics of Version Numbers #
The following sections are the "at a glance" notes I have about how to get off the ground with software versioning.

## How to Build a Version Number ##
All version numbers follow this pattern: `MAJOR.MINOR.PATCH`

## The First Version Number ##
Start at 0.1.0 for development.  
1.0.0 is when the software is being used in production.

## When to Change a Version Number ##
Version numbers are only ever incremented. 

- `MAJOR`:  Large, incompatible API changes made
- `MINOR`:  Added functionality
- `PATCH`:  Bug fixes

## Resetting to 0 ##
- Reset `PATCH` when `MINOR` is incremented
- Reset `PATCH` and `MINOR` when `MAJOR` is incremented

# Learning Resources #
In this post, I quickly covered what I thought to be the absolute basics of software versioning numbers. I learned about this tool over at [semver.org](https://semver.org/). There you will find an detailed guide on *Semantic Versioning*. 