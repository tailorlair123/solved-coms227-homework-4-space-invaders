Download Link: https://assignmentchef.com/product/solved-coms227-homework-4-space-invaders
<br>
<span style="font-size: 2.61792em; letter-spacing: -1px; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen-Sans, Ubuntu, Cantarell, 'Helvetica Neue', sans-serif;">Overview</span>

The primary goal of this assignment is to give you experience with inheritance hierarchies. The SpaceInvaders game engine developed for this assignment has an abstract SpaceShip base class, from where are derived InvaderShip (also abstract), ShooterShip, MultiShooterShip, BomberShip, TsarBombaShip, and DefenderShip (the player). Additionally, from a Projectile class is derived a Bomb.

<h1>Specification</h1>

The specification for this assignment includes this pdf and the javadocs, as well as any official clarifications posted on Piazza.

Where’s the main() method??

<span style="text-decoration: line-through;">There isn’t one! Like most Java classes, this isn’t a complete program </span>It’s in ui/Game.java. We’ve also shipped within the template a working (compiled) version of the game, so you can see how it should work. Run java bin/ui/Game to test it out.

There will also be a SpecChecker (not ready yet) that will perform a lot of functional tests, but when you are developing and debugging your code at first you’ll always want to have some simple test cases of your own as in the main method above.

Note that neither the SpecChecker nor the provided test program nor the combination of the pair provide complete, comprehensive test coverage of your implementation. You will have to write your own tests.

What must you write?

The methods that you must write or modify are all described in the javadocs. If it’s not described in the javadocs, you may assume it works are leave it alone. We list the method signatures here:

<ul>

 <li>Tableau: This class manages the game world.

  <ul>

   <li>private boolean checkForEnemyHit(DefenderProjectile d)</li>

   <li>private SpaceShip getRightMostEnemy()</li>

   <li>private SpaceShip getLeftMostEnemy()</li>

   <li>private SpaceShip getLowestEnemy()</li>

   <li>public void moveEnemyFleet()</li>

  </ul></li>

 <li>SpaceShip: The base class of all of the different types of ships

  <ul>

   <li>public void translate(double deltaX, double deltaY)</li>

   <li>public void setPosition(double newX, double newY)</li>

  </ul></li>

 <li>ShooterShip: Invader ship which fires single projectiles

  <ul>

   <li>public ShooterShip(Position p, int armor)</li>

   <li>public Projectile[] fire()</li>

  </ul></li>

 <li>MultiShooterShip: Invader ship which fires a spread of projectiles

  <ul>

   <li>public MultiShooterShip(Position p, int armor)</li>

   <li>public Projectile[] fire()</li>

  </ul></li>

 <li>BomberShip: Invader ship which drops small bombs

  <ul>

   <li>public BomberShip(Position p, int armor)</li>

   <li>public Projectile[] fire()</li>

  </ul></li>

 <li>TsarBombaShip: Invader ship which drops big bombs – public TsarBombaShip(Position p, int armor) – You do not need to overload fire() for this class. Why not?</li>

</ul>

<h1>Suggestions for getting started</h1>

Most of the constructors are one-liners, and your code won’t build until you write them, so do that first. The fire() methods are also pretty simple; the DefenderShipfire() method is complete, so you may look there if you’re stumped. Some of the methods in Tableau are a bit more involved, so save these for last.

<h1>The SpecChecker</h1>

You will (eventually) find the SpecChecker online; see the Piazza Homework post for the link. Import and run the SpecChecker just as usual. It will run a number of functional tests and then bring up a dialog offering to create a zip file to submit. Remember that error messages will appear in the console output. There are many test cases so there may be an overwhelming number of error messages. <em>Always start reading the errors at the top and make incremental corrections in the code to fix them</em>. When you are happy with your results, click “Yes” at the dialog to create the zip file. See the document “SpecChecker HOWTO”, which can be found in the Piazza pinned messages

<h1>More about grading</h1>

This is a “regular” assignment so we are going to read your code. Your score will be based partly (about a third) on the SpecChecker’s functional tests and partly on the grader’s assessment of the quality of your code. This means you can get partial credit even if you have errors, and it also means that even if you pass all the SpecChecker tests you can still lose points. Are you doing things in a simple and direct way that makes sense? Are you defining redundant instance variables? Some specific criteria that are important for this assignment are:

<ul>

 <li>Use instance variables only for the “permanent” state of the object, use local variables for temporary calculations within methods.</li>

</ul>

– You will lose points for having lots of unnecessary instance variables – All instance variables should be private.

<ul>

 <li>Accessor methods should not modify instance variables.</li>

</ul>

See the “Style and documentation” section below for additional guidelines.

<h1>Style and documentation</h1>

Roughly 15% of the points will be for documentation and code style. Here are some general requirements and guidelines:

<ul>

 <li>Each class, method, constructor and instance variable, whether public or private, must have a meaningful and complete Javadoc comment. Class javadoc must include the @author tag, and method javadoc must include @param and @return tags as appropriate.

  <ul>

   <li>Try to state what each method does in your own words, but there is no rule against copying and pasting the descriptions from this document or from the posted javadoc.</li>

   <li>Run the javadoc tool and see what your documentation looks like! You do not have to turn in the generated html, but at least it provides some satisfaction &#x1f642;</li>

  </ul></li>

 <li>All variable names must be meaningful (i.e., named for the value they store).</li>

 <li>Your code should not be producing console output. You may add println statements when debugging, but you need to remove them before submitting the code.</li>

 <li>Internal (//-style) comments are normally used inside of method bodies to explain how something works, while the Javadoc comments explain what a method does. (A good rule of thumb is: if you had to think for a few minutes to figure out how something works, you should probably include a comment explaining how it works.)

  <ul>

   <li>Internal comments always precede the code they describe and are indented to the same level. In a simple homework like this one, as long as your code is straightforward and you use meaningful variable names, your code will probably not need many internal comments.</li>

  </ul></li>

 <li>Use a consistent style for indentation and formatting.

  <ul>

   <li>Note that you can set up Eclipse with the formatting style you prefer and then use Ctrl-Shift-F to format your code. To play with the formatting preferences, go to Window→Preferences→Java→Code Style→Formatter and click the New button to create your own profile for formatting.</li>

  </ul></li>

</ul>

<h1>If you have questions</h1>

For questions, please see the Piazza Q &amp; A pages and click on the folder assignment4. If you don’t find your question answered, then create a new post with your question. Try to state the question or topic clearly in the title of your post, and attach the tag assignment4. <em>But remember, do not post any source code for the classes that are to be turned in</em>. It is fine to post source code for general Java examples that are not being turned in. (In the Piazza editor, use the button labeled “pre” to have Java code formatted the way you typed it.)

If you have a question that absolutely cannot be asked without showing part of your source code, make the post “private” so that only the instructors and TAs can see it. Be sure you have stated a specific question; vague requests of the form “read all my code and tell me what’s wrong with it” will generally be ignored.

Of course, the instructors and TAs are always available to help you. See the Office Hours section of the syllabus to find a time that is convenient for you. We do our best to answer every question carefully, short of actually writing your code for you, but it would be unfair for the staff to fully review your assignment in detail before it is turned in.

Any posts from the instructors on Piazza that are labeled “Official Clarification” are considered to be part of the spec, and you may lose points if you ignore them. Such posts will always be placed in the Announcements section of the course page in addition to the Q &amp; A page. (We promise that no official clarifications will be posted within 24 hours of the due date.)

<h1>What to turn in</h1>

Please submit, on Canvas, the zip file that is created by the SpecChecker. The file, SUBMIT THIS hw4.zip, will be located in the directory you selected when you ran the SpecChecker. It should contain one directory, hw4, which in turn contains your source tree. Please LOOK at the file you upload and make sure it is the right one!

Submit the zip file to Canvas using the Assignment 4 submission link and verify that your submission was successful. If you are not sure how to do this, see the document “Assignment Submission HOWTO” which can be found in the Piazza pinned messages.

We recommend that you submit the zip file as created by the SpecChecker. If necessary for some reason, you can create a zip file yourself. The zip file must contain the directory hw4, which in turn should contain your source tree. You can accomplish this by zipping up the src directory of your project. The file must be a zip file, so be sure you are using the Windows or Mac zip utility, and NOT a third-party installation of WinRAR, 7-zip, or Winzip