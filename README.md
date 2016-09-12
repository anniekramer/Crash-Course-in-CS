# Crash Course in CS
Demystify computer science with this fast and furious approach to the fundamentals of web development, data analysis, and more.

## Goals
- **High-level objectives**:
  * Triage and diagnose basic issues in code
  * Debug basic problems in JavaScript and Python
  * Build a simple web app with a Python backend and a JavaScript frontend
  * Perform simple programmatic data analysis using Python

- **Concrete skills for strong foundations in computer science:
  * Basic program execution and flow: be able to trace a piece of code line by line and say what it does/outputs)
  * Object-oriented programming (OOP): be able to explain methods and inheritance, the purpose of methods
  * Debugging fundamentals: be able to use the developer console to step through and debug simple programs
  * Fluency in parsing and understanding documentation: e.g. be able to use an official Python module by reading the documentation for it

- **Concrete skills for working on a software team**:
  * Code review: why it's important, what it entails, how to respond to feedback
  * Version control and Git fundamentals: be able to work on a feature branch, understand the relationship between the master branch and feature branches

- **Curriculum structure**:
  * Reading assignments
  * Deliverables: practical applications of reading material

# Curriculum
## Week 1: CS Fundamentals
- Pick a text editor.
  * Short discussion of VIM vs. EMACS vs. Sublime Text. What is a GUI?
- Pick a version control system to learn.
  * Short discussion of Git vs. Mercurial.
  * [Git tutorial] (https://git-scm.com/book/en/v1/Getting-Started)
  * [Interactive Git tutorial] (https://try.github.io/levels/1/challenges/1) from GitHub
  * [Mercurial tutorial] (http://hginit.com/)
- Intro to basic shell commands (bash).
  * Commands (incomplete list): `cd`, `ls`, `pwd`, `mv`, `cp`, `rm`, `echo`, `cat`, `wc`, `less`, `python`
  * Concepts: `$PATH`, tab completion, command line arguments, simple piping
  * [Cheat sheet] (http://cli.learncodethehardway.org/bash_cheat_sheet.pdf)
- Choose a Python resource that works well for your learning style (listed here in my order of preference).
  * [Python for Informatics] (http://www.pythonlearn.com/book_008.pdf)
  * [Codeacademy Python] (https://www.codecademy.com/learn/python): interactive tutorial
  * [Learn Python the Hard Way] (https://learnpythonthehardway.org/book/intro.html)
  * [Think Python] (http://www.greenteapress.com/thinkpython/thinkpython.pdf)
  * Official [Python Tutorial] (https://docs.python.org/2/tutorial/)
- Mercurial overview and why we use distributed version control systems (DVCS).
  * [Mercurial tutorial] (http://hginit.com/01.html)

### Deliverable: Hailstone Sequence
- Write a program that computes the length of the Hailstone sequence for a given natural number.
- Note on functions: functions should perform one discrete task. The main function should run behavior / actions on the smallest possible unit that makes sense in the context of the script. Functions should be well-defined and versatile so that they can be applied to small units.
- References: [blog post] (http://gabaix.us/blog/hailstone), [Wikipedia] (https://en.wikipedia.org/wiki/Collatz_conjecture#Statement_of_the_problem)
- [Solution] (https://github.com/goingglacial/hailstone)

### Okay, you're doing great! Let's continue. 

## Week 2: Let's Talk Basic Algorithms
### Deliverable: Random Writer
- Note that this assignment is taken from Stanford's CS106B course (Programming Abstractions).
- See problem 2 [here] (http://www.stanford.edu/class/archive/cs/cs106b/cs106b.1136/handouts/090%20Assignment%202.pdf).
- [Solution] (https://github.com/goingglacial/random_writer)

## Week 3: More Python
- Continue reading your Python material of choice (see above).

### Deliverable: Word Ladder
- Note that this assignment is taken from Stanford's CS106B course (Programming Abstractions).
- See problem 1 [here] (http://www.stanford.edu/class/archive/cs/cs106b/cs106b.1136/handouts/090%20Assignment%202.pdf).
- [Solution] (https://github.com/goingglacial/word_ladder).

## Week 4: Yet More Python
- Continue reading your Python material of choice and complete inline exercises along the way.
- Intro to classes: read chapters 15-17 of [Think Python] (http://www.greenteapress.com/thinkpython/thinkpython.pdf).
  * Skip 17.7, 17.8, and 17.9 (operator overloading, type-based dispatch, and polymorphism) for now as they're not yet relevant.
- Read the [Semantics] (http://www.itmaybeahack.com/book/python-2.6/html/p03/p03c01_class.html#semantics) section in Building Skills in Python.

### Deliverable: Payroll Program
- Objective: Work with reading files, string manipulation, lists, and dictionaries.
- Program requirements: The program takes one command line argument: the name of a text file to read.  The contents of the file will look like this:
```
Sam            Teacher       25   :   4  5  3  2  2  0  0
Annie          Programmer    40   :   7  7  9  8  5  1  1
Max            Programmer    43   :   9  9  9  10 7  5  0
Ryan           Teacher       55   :   10 9  11 9  6  3  3
Deats          Programmer    40   :   8  7  9  8  5  0  4
```
- **File specifications**:
  * The first column in the person’s name (first name only with no spaces).
  * The second column is the person’s role (again, no spaces).
  * The third column is each person's hourly wage.
  * The remaining columns are how much they worked on each day of the week, starting with Monday and ending with Sunday.
- **What if a given input file doesn't match this format?**
  * Your program is allowed to have undefined behavior on input files that do not match this format. In practice, this simply means that you don’t need to consider this case, so your program will most likely just crash.
- From this information, **compute payroll as follows**:
  * Normal pay for up to 40 hours of work during the work week (Monday-Friday).
  * 1.5x overtime pay for any hours above 40 worked during the week.
  * 1.5x overtime pay for all weekend hours.
- **Required output**:
  * Payroll: Print each person’s name and the amount of money they’re owed for that week.
  * Expense breakdown: For each role, print the total amount spent on that role and the percentage of the total of that role’s spend (rounded to the nearest percent). Also print the total expense for that week.
  * Slacker warnings: For each person who worked less than 20 hours in a week, print a warning about them being a slacker.
  * Example output (for the example input file above):
```
=== Payroll ===
Sam: $400.00
Annie: $1560.00
Max: $2300.50
Ryan: $3107.50
Deats: $1720.00

=== Expense Breakdown ===
Programmer: $5580.50, 61%
Teacher: $3507.50, 39%
Total: $9088.00

=== Slackers ===
Sam only worked for 16 hours!
```
- Remember: it’s easiest to build projects by breaking them down into small steps.
- To parse the file, you’ll want to use the Python [string methods] (https://docs.python.org/2/library/stdtypes.html#string-methods). See especially [split] (https://docs.python.org/2/library/stdtypes.html#string-methods) and [splitlines] (https://docs.python.org/2/library/stdtypes.html#str.splitlines).

## Week 5: Git-ing Up to Speed
- Objective: Develop working knowledge of Git sufficient to understand and actively participate in a software team's collaborative processes, including developing on feature branches and submitting code for review.
- Review the purpose of version control and the basic conceptual basis of Git by reading Chapter 1 of [Pro Git] (https://git-scm.com/book/en/v1/Getting-Started) (skip the installation instructions in section 1.4, as you already have Git installed).
- If you find yourself a little tripped up by the Git material, check out this phenomenal [Mercurcial tutorial] (http://hginit.com/), starting from “Ground Up Mercurial." The Git commands behave slightly differently from Mercurial commands (and basic syntax is slightly different), but the higher-level concepts map closely to one another.
- Read about basic Git commands in [Chapter 2] (http://git-scm.com/book/en/Git-Basics) of Pro Git. Some parts of this chapter (like adding and committing files) should be a review of what you already know. Consider making a test Git repository and playing around with it as you read.  Don’t be afraid of trying things out!
  * 2.1 covers getting a Git repository with `git init` and `git clone`.
  * 2.2 covers the concepts of staging, tracking, and ignoring files, as well as `git add`, `git diff`, `git commit`, `mv`, and `rm`. Skim the section on Ignoring Files; you don’t need to know how to write a `.gitignore` right now, but you should understand what it does.
  * 2.3 covers the `git log` command in depth. Read about halfway down until it starts discussing the format option, then move on.
  * 2.4 covers undoing various operations by amending commits, unstaging files, and throwing away changes to files
  * 2.5 covers basic operations involving remote repositories: adding, removing, and pulling from remotes. Focus on the "Fetching and Pulling" and "Pushing" sections; skip everything else.
  * The rest of Chapter 2 isn’t relevant (it covers tagging).
- Read about branching in [Chapter 3] (https://git-scm.com/book/en/v1/Git-Branching) of Pro Git. This covers the concept of a branch; creating, deleting, and merging branches; a few commonly-used branching workflows; remote branching; and rebasing. This whole chapter covers material that is germaine to how professional software teams use Git for version control and collaboration.
- Read more on rebasing in this [tutorial] (https://www.atlassian.com/git/tutorials/rewriting-history/#!rebase) from Atlassian.
- Topics to Google: remote repositories, commit messages, rebasing vs. merge commits.
- Read this [guide] (http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html) to writing high-quality commit messages.
- [Read] (https://www.atlassian.com/git/tutorials/undoing-changes/#!reset) about the `git reset` command.
- [Learn] (http://gitready.com/intermediate/2009/02/09/reflog-your-safety-net.html) how to undo mistakes with the `git reflog` command (but ignore the part at the end about freeing up space; there’s almost never any reason to do that).

## Week 6: Finalizing Python (for now, at least)
- Read the about [errors and exceptions] (https://docs.python.org/2/tutorial/errors.html) in Python; skip 8.5 (user-defined exceptions). Note that exceptions are errors detected during program execution.
  * **Exercise**: Write a program that takes in the name of a file as an argument and prints the number of lines in the file.  If the file cannot be opened or does not exist, print a nice error message (which does not have to describe the particular error) and exit. [Solution] (https://github.com/goingglacial/exceptions/blob/master/exceptions.py)
- Read about basic functional programming (Python functions as valuables)
- Tuples: Skim [Chapter 10] (http://www.pythonlearn.com/book_008.pdf) in Python for Informatics, which discusses the basic concept of tuples, multiple assignment, and some useful applications. The Decorate, Sort, Update pattern it describes is no longer considered idiomatic, but it works perfectly well until you learn a better way. Don’t worry about a deep understanding of tuples - familiarity is fine for now!
- Linting: Read this high-level [overview] (https://en.wikipedia.org/wiki/Lint_(software).
- What is JSON? And what's up with JSON serialization and deserialization? And how do we analyze JSON blobs using Python?
 * Read this Stack Overflow [answer] (http://stackoverflow.com/questions/383692/what-is-json-and-why-would-i-use-it) for the fundamentals of JSON.
 * Explore the basics of Python's standard JSON library by reading the first part of this [tutorial] (https://pymotw.com/2/json/). Stop at "Working with Your Own Types."
 * Read this [post] (http://www.joelonsoftware.com/articles/Unicode.html) on unicode by software/SaaS master Joel Spolsky for more background on working with JSON output.
 * **Exercise**: Download this [JSON file] (https://github.com/anniekramer/Crash-Course-in-CS/blob/master/fake_peeps.json) containing fake personal information. Use the Python JSON library to determine the average age of people listed in the file and the number of people of each gender. [**Solution**] (https://github.com/goingglacial/json_test) 

## Week 7: Transition to the Web
- Gain a conceptual understanding of HTML and CSS through practice, and learn enough to be able to build a simple webpage.
  * Complete Codecademy’s [Introduction to HTML and CSS tutorial] (https://www.codecademy.com/learn/web) to explore the fundamentals of HTML, lists, tables, divs, spans, and the fundamentals of CSS, including selectors, and positioning.
- Complete Codeacademy’s [Introduction to JavaScript] (https://www.codecademy.com/learn/javascript) tutorial to learn the fundamentals of the language.
