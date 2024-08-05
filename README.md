This summer I taught local middle and high school students introductory java lessons.  I created the lesson plans, material, and activities myself, based on past java learning experiences in "AP Computer Science A" in high school, "Introduction to Computer Science" in college[^1] and my own personal projects and interests.  Here is everything I taught them.

[^1]: A big help was [learncs.online](https://learncs.online), which allows public access to our freshman java lessons, meaning I could continually reference the lessons while no longer being enrolled in the class.



# Java Cheatsheet
This is a copy of the written packet I gave my students to reference as we moved through the course.


## Printing to the Console
Print → `System.out.print(“Message”);`

Print and skip the next line → `System.out.println(“Message”);`


## Literals
***Definition:*** A value that appears directly in your code

***Example:*** 0, 8.2, true, ‘c’, “Hello World”


## Comments
***Definition:*** The words the computer doesn’t read
Used to make your code more understandable and readable for yourself and other coders

// comment → single line comment

/* comment */ → multi-line comment

--

***Examples:***

`// here is a single line comment`

```
/*

here is a multi-line comment. Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.

*/
```



## Variables
***Definition:*** A way to store literals under a name

### Primitive Types:

***4 Categories of Java Primitive Types:***

* **Integer values:** byte, short, int, and long (each holds a different range of data)

* **Floating point values:** float and double (each holds a different range of data)

* **Boolean values:** boolean

* **Characters:** char

### Non - Primitive Types:

These variables store references to objects in memory.  We will explore more on primitive vs. non-primitive later, so don't worry too much about it right now.

These types are capitalized.

***Examples:***

* String
* Arrays
* Classes

### Important to Know:

1. **int** → stores an integer / whole number

    * Example: 5, 8, 96, 324

2. **double** → stores a number with a decimal
	
    * Example: 9.2, 34.9, 67.0, 143.2
    
3. **char** → stores a single character

    * Example: d, !, 4, B, :

4. **boolean** → stores either true or false

    * Example: true, false

5. **String** → stores text

    * Example: hello, John, giraffe, Florida

## come back to below ------------------
Variable Assignment
= symbol is the assignment operator
Assigns the right side of the = to the left side
Ex: int value = 10;
10 is being assigned to the integer value	

Concatenation:
Allows the combination of strings with the + operator
Ex:
String firstName = “Johnny”
String lastName = “John”
System.out.println(firstName + ‘ ‘ + lastName);
Camel Case:
Common in Java, JavaScript, and TypeScript

Naming convention, when using a variable whose name is multiple words long
No spaces
Write the first letter of all but the first word in uppercase
		Ex: variableName, numPeople, piecesOfPieAtDinner
Variable Assignment
= symbol is the assignment operator
Assigns the right side of the = to the left side
Ex: int value = 10;
10 is being assigned to the integer value	

## come back to above ------------------




## Operations on Variables

### Operators:

**+** → Addition

**-** → Subtraction

**\*** → Multiplication

**/** → Division

You can modify variables through re-assignment.

***Examples:***

```
int count = 10;
int count = count * 2;` // count is now 20
```

```
double netWorth = 20;
double payCheck = 60;
newNetWorth = netWorth + payCheck;
```

***Shortcuts:***

**+=** → adds the value on the right side to the left side

**-=** → subtracts the value on the right side to the left side

***=** → multiplies the value on the right side to the left side

**/=** → divides the value on the right side to the left side

***Examples:***

```
int score = 15;
int score += 5; // score is now 20
```

```
double price = 30;
double discount = 0.5;
price *= discount; // price is now 15
```


## Conditional Expressions:

Expressions that evaluate either true or false.

Often used in "control flow statements" like if-statements, while loops, and for loops (more on these later).


## Conditional Operators:

**<** → less than

**>** → greater than

**<=** → less than or equal to

**>=** → greater than or equal to

**==** → equal to (VERY different from the = symbol)

**!=** → not equal to

***Examples:***

`95 > 90` → true

`5 == 8` → false

`12.3 != 12.9` → true

`6 <= 6` → true



## Blocks:

Begin and end in { and }, and consists of everything between the brackets.

### If - statements:

```
if (condition) {
  // do something
}
```

***Real world example:***

**If** my clothes are dirty, **then** I will wash them.

**Else**, I will put them away.

```
if (clothesAreDirty == true) {
  // wash clothes
} else {
  // put clothes away
}
```

Think of it as falling through the if-statement/else-ifs.

***Example:***

```
if (grade >= 90) {

	System.out.println(“You got an A);

} else if (grade >=  80) {

	System.out.println(“You got a B”);

} else if (grade >= 70) {

	System.out.println(“You got a C”);

} else if (grade >= 60) {

	System.out.println(“You got a D”);

} else {

	System.out.println(“You got an F”);

}
```


## Compound Conditionals:

### 3 New Operators:

**&&** → “and”, means both arguments must be true for the statement to evaluate true

**||** → “or”, means at least one argument must be true for the statement to evaluate true

**!** → “not”, negates the following argument, known as a "bang sign"

These operators are used to group conditionals.

`true && true` → true

`true && false` → false

`false && true` → false

`false && false` → false

--

`true || true` → true

`true || false` → true

`false || true` → true

`false || false` → false

`!true` → false

`!false` → true

***Example:***

`(8 == 8) && (6 < 9)` → true

`(12 >= 12) && (5 != 5)` → false

`(9 <= 0) && (3 > 2)` → false

`(8 * 7 == 2) && (9 * 12  < 3)` → false

`(8 == 8) || (6 < 9)` → true

`(12 >= 12) || (5 != 5)` → true

`(9 <= 0) || (3 > 2)` → true

`(8 * 7 == 2) || (9 * 12  < 3)` → false












## Arrays:

A way to store groups of data sequentially.

### 2 ways to declare an array:

***Examples:*** For an integer array named ages of size 6 (holding 6 values):

`int[] ages = new int[6];`  ←sets default values as placeholders.  For integers, this means 0s.

 		-- OR --
   
`int[] ages = {12, 9, 18, 6, 7, 14};`

Basically: `type[] variableName = new type[size];`

		-- OR --
  
	`type[] variableName = {data};`


*Note: Array size cannot be changed later after declaration

### Array Indexing:

To access the data in an array, you tell the computer what position that data is in.

Arrays are zero-indexed, meaning the first position is 0, then the next is 1, etc.

***Examples:*** Using previous ages array: 

12 → Position 0

9 → Position 1

18 → Position 2

6 → Position 3

7 → Position 4

14 → Position 5

So to print out the value 18, I would use:

`System.out.println(ages[2]);`




### Changing Values:

If I wanted the first value of ages to be 20, I would write

`ages[0] = 20;`

So to load an array value by value:

```
int[] newAges = new int[3]

int[0] = 19;

int[1] = 4;

int[2] = 8;
```




### A Look Ahead:

I’m very proud of you for learning so well this summer.  Java was also my first big language, which I learned in my Senior year of high school, and I remember it being super confusing at the start.

I strongly encourage you to continue learning Java, or other coding programs!


I referenced a lot of content to teach you guys from [https://www.learncs.online/lessons], which is a free online version of the freshman-year introductory class in Java I took at UIUC. If you  continue, I recommend creating your own account and playing around with the learn, solve, test, debug, and play tabs.  We got to around the 5th lesson in their sequence, and you can continue forward from there or review those we already covered.




## Future Languages I Suggest to Learn:

The great thing about coding is although the syntax may differ between languages, the core principles are the same.

This means that once you learn a language or two, learning new ones become infinitely easier.  So you're already a step ahead!


***Python:***
* Known as a simple language!
* Has lots of libraries and resources out there
* Great for: Data Science / Analytics, Machine Learning / Artificial Intelligence, Scripting (ex: Web scraping, task automation, testing scripts, system administration), Web Development, Automation, Trading, much more

***Arduino Programming Language:***
* Before I learned Java, I learned to code simple arduinos for projects!
* Super fun and rewarding
* Can make some fun projects from it, by controlling motors, LED lights, etc
* Cool to see physical results of your programming!
* I bought a kit that came with all the needed parts and a book of projects to start, but you can also find projects and resources online and buy your own parts

***Swift:***
* ios (Apple) app development!
* Very cool to learn for fun projects
* You can actually download what you made onto your phone, which is pretty cool to see!!

***HTML / CSS / JavaScript:***
* 3 languages I use for web development
* Focus on learning frontend first, then backend
* HTML → bones, CSS → skin, JavaScript → muscles of the website
* Once you learn how to use these three languages very well, you can move on to popular frameworks like React


## Resources:

I had ChatGPT compile some resources for languages, but you can always Google and research on your own!  YouTube, ChatGPT, and online forums/sites like Stack Overflow will also be your friend for questions and learning.  YouTube courses can be a great starting point.

***1. Python***
   - Free Resources:
     - [Codecademy: Learn Python](https://www.codecademy.com/learn/learn-python-3)
     - [Coursera: Python for Everybody](https://www.coursera.org/specializations/python)
     - [Automate the Boring Stuff with Python](https://automatetheboringstuff.com/) - Free online book
   - Books:
     - "Python Crash Course" by Eric Matthes
     - "Automate the Boring Stuff with Python" by Al Sweigart
   - Interactive Platforms:
     - [SoloLearn](https://www.sololearn.com/Course/Python/)
     - [HackerRank](https://www.hackerrank.com/domains/tutorials/10-days-of-python)
   
***2. JavaScript***
   - Free Resources:
     - [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
     - [Eloquent JavaScript](https://eloquentjavascript.net/) - Free online book
   - Books:
     - "Eloquent JavaScript" by Marijn Haverbeke
     - "You Don't Know JS" series by Kyle Simpson
   - Interactive Platforms:
     - [Codecademy: Learn JavaScript](https://www.codecademy.com/learn/introduction-to-javascript)
     - [FreeCodeCamp: JavaScript Algorithms and Data Structures](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/)

***3. Java***
   - Free Resources:
     - [Codecademy: Learn Java](https://www.codecademy.com/learn/learn-java)
     - [Coursera: Java Programming and Software Engineering Fundamentals](https://www.coursera.org/specializations/java-programming)
   - Books:
     - "Head First Java" by Kathy Sierra and Bert Bates
     - "Effective Java" by Joshua Bloch
   - Interactive Platforms:
     - [SoloLearn](https://www.sololearn.com/Course/Java/)
     - [HackerRank](https://www.hackerrank.com/domains/tutorials/10-days-of-java)

***4. HTML & CSS***
   - Free Resources:
     - [Codecademy: Learn HTML](https://www.codecademy.com/learn/learn-html)
     - [Codecademy: Learn CSS](https://www.codecademy.com/learn/learn-css)
     - [MDN Web Docs: HTML](https://developer.mozilla.org/en-US/docs/Web/HTML)
     - [MDN Web Docs: CSS](https://developer.mozilla.org/en-US/docs/Web/CSS)
   - Books:
     - "HTML and CSS: Design and Build Websites" by Jon Duckett
   - Interactive Platforms:
     - [FreeCodeCamp: Responsive Web Design Certification](https://www.freecodecamp.org/learn/responsive-web-design/)

***5. Swift (for iOS Development)***
   - Free Resources:
     - [Codecademy: Learn Swift](https://www.codecademy.com/learn/learn-swift)
     - [Apple's Swift Documentation](https://developer.apple.com/swift/resources/)
   - Books:
     - "Swift Programming: The Big Nerd Ranch Guide" by Matthew Mathias and John Gallagher
     - "iOS Programming: The Big Nerd Ranch Guide" by Christian Keur and Aaron Hillegass
   - Interactive Platforms:
     - [HackerRank](https://www.hackerrank.com/domains/tutorials/10-days-of-swift)
     - [SoloLearn](https://www.sololearn.com/Course/Swift/)

***General Learning Platforms***
- [Coursera](https://www.coursera.org/): Offers courses from universities and organizations on various programming languages.
- [edX](https://www.edx.org/learn/computer-programming): Provides courses from top institutions on different programming languages.
- [Udemy](https://www.udemy.com/): Features a wide range of paid courses often available at discounted prices.
- [Khan Academy](https://www.khanacademy.org/): Offers introductory courses in computer programming.

