---
layout: post
title:  "Running Java in the command-line"
categories: Activity Sorting PA
---

I imagine that a lot of folks are compiling and running their Java code in the command-line for the first time for this assignment. This document is meant to help detail bits of that process that are useful to building the `pa1.sh` and `setup.sh` files to make sure your code is compiling and running properly for PA1 and beyond.

### Running Java from the command-line

The standard way to run Java code in the command-line is, as one might expect, with the `java` command. What it always wants passed in is the name of the main class to run. If you're running it from a directory that doesn't contain all of your compiled `.class` files, it will also want a *classpath*, which tells you where those classes are! This is specified by the `-cp` option. So the standard call to `java` for us will look like

```bash
java -cp [PATH TO .CLASS FILES] [NAME OF MAIN CLASS]
```
where you substitute for the things in brackets. Given the structure I've given you in the Java project, `pa1_template.pa1` is the name of the package/class our code is in, so we have to find the path where the `pa1_template` folder resides.

This is the line that should be in your `pa1.sh` file if you're using Java!

### Compiling Java Code

Your typical method for compiling Java code is probably either (1) just hitting compile & run in VSCode or (2) Using Gradle Build. The way things are set-up in VSCode, these may result in different locations where your code ends up! By default, running `gradle build` will put things in the `java/build/classes/main/` folder, and VSCode places it in `java/bin/main/` 
