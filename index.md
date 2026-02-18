---
layout: default
---

# Introduction

## About Me & Self-Assessment

I am Christian Clark, a student at Southern New
Hampshire University. I am currently pursuing a Bachelor
of Science in Computer Science. 

My time in this course has taught me quite a lot about the deeper aspects of mobile development, and even though it's not my ideal career path, I believe that my ability to learn and adapt to more complex problems is a valuable skill that will serve me well in the future. Application development is not as simple as some might think at first glance, and I think my demonstration of my ability to take my old application code and rewrite it to improve it will help my future. 

In particular, I enjoy the small little uses of languages like Kotlin's ability to overload classes with new methods. 
```

private const val HIGHEST_WEIGHT: Float = 3000f
private const val LOWEST_WEIGHT: Float = 0.1f
fun Float.isValidWeight(): Boolean = this in LOWEST_WEIGHT..HIGHEST_WEIGHT

```
Something like this might seem insignificant, but just having the ability to, from anywhere in the code, validate a float keeps my code secure. I can have a much easier way to prevent invalid weights from being entered and having localized constants means that any time I need to change the weight range, I only have to change it in one place. These small optimizations can make a big difference in the long run.

CONTINUE SELF ASSESSMENT

## Code Review

<iframe width="560" height="315" src="https://www.youtube.com/embed/az0HTZNs1O8" frameborder="0" allowfullscreen></iframe>

## [CS370 Weight-Tracker Android Application](https://github.com/Cclark50/CS360-Weight-Tracker)

This is the artifact that I will be enhancing over the
course of my CS499-Capstone project for Southern New
Hampshire University. This is an android application
used to track weight, store previous days weights, and
send SMS notifications when the user either reaches
their goal or gets close to their goal.

## [CS499 Weight-Tracker Android Application - Software Design and Engineering Category](https://github.com/Cclark50/CS360-Weight-Tracker/tree/CS499-Base)

Using the Weight-Tracker artifact as a base, I enhanced
the application by rewriting the entire application,
execept for the database adapter because that will be
enhanced in a later enhancement, from Java to Kotlin. In
addition to a Kotlin rewrite, other quality of life
enhancements were made, such as the ability to remember
the user's last login username and autofill it, a
progress bar to show a user's progress towards their
goal, and a change from SMS notifications to native push
notifications.

This was a journey of learning a new language and rewriting an already existing application into another language. While I am fluent in Java, I had never touched Kotlin before this rewrite. During this enhancement, I was also able to touch up on some smaller parts of the application I was unhappy with and make those improvements, even if they're invisible to the end user. 

By introducing Kotlin, I was able to demonstrate the ability to support decision making for software design stakeholders by creating an environment where both Kotlin and Java developers can work together on the same project, thus increasing the possible engineering pool. Kotlin also allows me to overload the Float class and add a custom method to calculate whether or not a particular float is within a valid range, ensuring data integrity and accuracy and demonstrating the ability to define an approach that ensures all data are explicitly validated. Finally, Kotlin gives me the ability to use more modern features that Java still lacks, meaning I can use more targeted features of the language to demononstrate the ability to create more robust and efficient code to deliver value and accomplish industry-specific goals. The 

## [CS499 Weight-Tracker Android Application - Data Structures and Algorithms Category](https://github.com/Cclark50/CS360-Weight-Tracker/tree/Adding-graph)

Continuing on from the kotlin rewrite, I implemented a graph fragment that allows the user to view their weight history in a graph format. Using a library called MPAndroidChart, I was able to create a line chart that displays the user's weight over time. This allows the user to easily see their progress and identify any trends in their weight loss or gain. Using O(n) time and space complexity to transform and store the data, I was able to create a graph that is both efficient and accurate.

This was a feature I wanted to implement for my CS360 class, but was not required for the rubric and I was already pressed for time. This gave me the chance to actually implement the feature and learn about external libraries for android development. Originally I was going to use Vico for my graph library, but after trying to get Vico to work for 2 days, I decided to switch to MPAndroidChart instead. Sometimes simpler solutions are better.

With my creation of this graph fragment, I had to create an algorithm that tied data points to indexes and reverse them to ensure that the graph was displayed correctly. This demonstrates the ability to program solutions to solve logic problems and implement them in software. By having a graph in my application, I demonstrated my ability to communicate appropriately to specific audiences and contexts by giving the user a visual representation of their data. Frequent comments in this fragment clearly express the time and space complexities of the algorithm used to generate the graph points and demonstrates my ability to provide contextual, in-code comments that result in easily readable and understandable code.

## [CS499 Weight-Tracker Android Application - Databases Category](https://github.com/Cclark50/CS360-Weight-Tracker/tree/Room)

As one last enhancement continuing from the previous category, I replaced my SQLite database with Room, a modern persistence library for Android. Room provides a simple and powerful API for accessing data in SQLite databases, and it also provides compile-time checks for SQL queries, which helps to prevent common errors and improve performance. 

By implementing Room I was able to see just how much extra code it required to use SQLite by itself. Room made using SQLite databases much easier to work with as I didn't need to write 50+ lines of boilerplate code to interact with the database. It did require a good amount of set up but should I want to, I can scale my database queries much faster and easier than having to write the same code to access a table. Using Room I was also able to consolidate my data classes making it much easier to pass around data. But, by implementing Room, I had to refactor all of my code to implement threading so that all database operations are performed on a background thread to avoid blocking the UI thread. This was actually the most heavy of my refactorings, as I had to modify all my existing code to use threading, along with adding an entity and DAO for each table in my database.

Using Room and its compile time query validation, I can catch errors early, demonstrating the ability to address potential design flaws in software architecture during the requirements phase and find and eradicate security vulnerabilities or bugs. Additionally, by using Room instead of raw SQLite, I demonstrate my ability to create industry-standard software designs (Google Developers, 2025).

### REFERENCES:

Google Developers. (December 4, 2025). Save data in a local database using Room. Google Developers. https://developer.android.com/training/data-storage/room
