# Crash Course in CS
Demystify computer science with this fast and furious approach to the fundamentals of web development, data analysis, and more.

## Goals
- **High-level objectives**:
  * Triage and diagnose basic issues in code
  * Debug basic problems in JavaScript and Python
  * Build a simple web app with a Python backend and a JavaScript frontend
  * Perform simple programmatic data analysis using Python

- **Concrete skills for strong foundations in computer science and working on a software team**:
  * Basic program execution and flow: be able to trace a piece of code line by line and say what it does/outputs)
  * Object-oriented programming (OOP): be able to explain methods and inheritance, the purpose of methods
  * Debugging fundamentals: be able to use the developer console to step through and debug simple programs
  * Fluency in parsing and understanding documentation: e.g. be able to use an official Python module by reading the documentation for it

- **Concrete skills for working on a software team**:
  * Code review: why it's important, what it entails, how to respond to feedback
  * Version control and Git fundamentals: be able to work on a feature branch, understand the relationship between the master branch and feature branches

# Curriculum
## Week 1: CS Fundamentals
- Pick a text editor.
  * Short discussion of VIM vs. EMACS vs. Sublime Text. What is a GUI?
- Pick a version control system to learn.
  * Short discussion of Git vs. Mercurial.
- Intro to basic shell commands (bash).
  * Commands (incomplete list): `cd`, `ls`, `pwd`, `mv`, `cp`, `rm`, `echo`, `cat`, `wc`, `less`, `python`
  * Concepts: `$PATH`, tab completion, command line arguments, simple piping
  * [Cheat sheet] (http://cli.learncodethehardway.org/bash_cheat_sheet.pdf)
- Choose a Python resource that works well for your learning style (listed here in my order of preference).
  * [Python for Informatics] (http://www.pythonlearn.com/book_008.pdf)
  * [Codeacademy Python] (https://www.codecademy.com/learn/python): interactive tutorial
  * [Learn Python the Hard Way] (https://learnpythonthehardway.org/book/intro.html)
  * Official [Python Tutorial] (https://docs.python.org/2/tutorial/)
- Mercurial overview and why we use distributed version control systems (DVCS).
  * [Mercurial tutorial] (http://hginit.com/01.html)
### Deliverable: Hailstone Sequence
- Write a program that computes the length of the Hailstone sequence for a given natural number.
- Note on functions: functions should perform one discrete task. The main function should run behavior / actions on the smallest possible unit that makes sense in the context of the script. Functions should be well-defined and versatile so that they can be applied to small units.
- References: [blog post] (http://gabaix.us/blog/hailstone), [Wikipedia] (https://en.wikipedia.org/wiki/Collatz_conjecture#Statement_of_the_problem)
- [Solution] (https://github.com/goingglacial/hailstone)
