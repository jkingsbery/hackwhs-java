
Instructions

(this exercise is from Java Structures by Duane Bailey)

The goal of this exercise is to learn some simple Java numeric calculations
to figure out the day of the week for different dates.

This algorithm relies on the following adjustment table:

Month   Adjustment
1       1
2       4
3       4
4       0
5       2
6       5
7       0
8       3
9       6
10      1
11      4
12      6

The algorithm for figuring out the date has the following steps:
1. Write the date numerically, with the year as the number of years since 1900.
   Today, for example, is 108 (2018-1900) - 12 - 8
2. Add together:
   - the month adjustment from the table
   - the day of the month
   - the year
   - the whole number of times 4 divides the year
3. Computer the remained of step 2 when divided by 7

The game we'll be making has the following steps:
1. Create a random date in the years 1900-2099.
2. Ask the user to guess the day of the week
3. If the user was correct, add one to the score.
4. Keep looping 1-3 until the user has gotten 10 correct. Output the time it took.

Before we get started, we'll need to set up the following:
1. Install the JDK. I find the easiest thing to do is download it from Oracle's site.
2. Set up your editor. Eclipse and Intellij are two popular choices, emacs and vim are also good (but old school)
3. Download Maven. Ensure it's added to your PATH
4. Run mvn archetype:generate to set up your hello world project

The suggested steps for doing the project once you have a hello world
1. Rather than just start coding, instead write the tests you want to see working. Edit the tests in AppTest.java. They won't work,
   or even compile, but it will help you to ensure you're done.
2. Add the main program in App.java.
3. Finally, you can run your program (after adding a snippet to your pom.xml file) by typing `mvn exec:java`