---
layout: lab
num: lab02
ready: false
desc: "Lab02 - Accumulator Functions and More Turtle Graphics"
assigned: 2018-02-06 08:00:00.00-7
due: 2018-02-07 23:59:59.00-7
---

<div markdown='1'>

<h1>Lab02: Factorial Function & More Turtle Graphics</h1>
<hr>
<h2>Goals for this lab</h2>

By the time you have completed this lab, you should be able to:
<ol>
<li>Write functions that use what the textbook calls the "Accumulator Pattern"</li>
<li>Know more about the manipulation of Python objects, as demonstrated with the use of the Turtle graphics module.</li>
</ol>


<h2>Step by Step Instructions</h2>
**Step 0:** Get together with your assigned lab partner. THIS LAB IS A REQUIRED PAIR PROGRAMMING ASSIGNMENT. LAB PARTNERS **MUST** BE IN THE SAME LAB. NO EXCEPTIONS.

**Step 1:** Log in, and create a lab02 directory
Decide which one of you will be the first pilot for this lab, and then log in to the pilot's account and create a directory called lab02 inside his/her cs8 folder. You will work in this account for the rest of the lab, but remember to switch often between pilot and navigator roles during the course of the lab.

**Step 2:** Bring up IDLE as usual, and open a new window for function definitions
Start IDLE. Then, select &quot;File-&gt;New Window&quot; and add a comment at the top of this new file like the following (with the proper substitutions of course): 

<pre>
# lab02.py
# Your names, today's date
</pre>

Then, save it under the name lab02.py inside your lab02 directory.

<h3>Step 3: Practice writing a function to accumulate products</h3>

You will write a function called factorial that computes the product of the first N numbers, where N is a parameter. For example, factorial(4) is calculated as 1 * 2 * 3 * 4, so the function should return the value 24. We will assume N is greater than 0. I did a similar exercise in lecture.

Be sure to understand the purpose and meaning of each of the following instructions before you execute them.

<ol type="a">

<li>Skip a blank line (in your lab02.py file), and then type a brief comment for a factorial function such as the following:
  <pre>
  # factorial - returns n factorial 
  # assumes n is greater than or equal to 0
  </pre>
</li>

<li>On the very next line, type the function header as follows:
  <pre>def factorial(n):</pre>
</li>

<li>Now write the rest of this function. It has to return the factorial value of n. Make sure that the function checks on the fact that n is a positive, non-zero number.
</li>
</ol>

Save and run the module. Then test the function a few times (in the Python shell window) by comparing its results to ones that you calculate manually.  Here are 2 example runs of our solution:
<pre>
>>> <b>factorial(3)</b>
6
>>> <b>factorial(5)</b>
120
</pre>

<h3>Step 4. Getting Started with pat, the (<u>p</u>erfectly <u>a</u>dorable) <u>t</u>urtle</h3>
<p>First make sure that you can show turtle graphics. Try this command at the Python shell prompt
   (&gt;&gt;&gt;):</p>
<pre>&gt;&gt;&gt; import turtle<br>&gt;&gt;&gt; </pre>
<p>If what you get back is just another Python prompt (not a bunch of error messages) then you are good to go.</p>
<p>Then type (still in the Python shell window) the following command:</p>
<pre>&gt;&gt;&gt; pat = turtle.Turtle(&quot;turtle&quot;)</pre>
<p>That last command will open another new window - probably titled "Python Turtle Graphics" -
   and eventually this window will display your drawings. But ignore it for now. In fact, you
   will need to recreate it later.</p>
<p>Back in the new file window (lab02.py file), type the drawRectangle function
   that we did together in class and add a comment in front of it, as in the example below:</p>
  <pre class="codes"># function to draw a rectangle
# parameters: name of a turtle, and the width and height to draw
# draws: a rectangle at the position of the turtle
  def drawRectangle(turtleObject, width, height):
# This is where your code goes...</pre>
<p>Once you have typed in the function, save the file, and use the Run=&gt;Run Module
   command to &quot;compile&quot; your Python code. You might get an error message
   when you do this the first time - read the message, and figure out what to fix in
   your function definition. Keep fixing, saving and running the module until it
   works without error messages. Then look in the Python Shell window
   - you should see something like this:</p>
<pre>&gt;&gt;&gt; ================================ RESTART ================================<br>&gt;&gt;&gt;   
</pre>
<p>Congratulations! You just compiled and loaded into memory a useful function that we
   can use to make drawings.</p>
<p>Unfortunately though, IDLE just destroyed a portion of the work you did earlier:
   pat the turtle is gone from memory (the Python shell was restarted). Not such a big
   loss this time - just two commands to repeat, but annoying nonetheless. Thankfully IDLE
   does provide a way to repeat prior commands. Try that way now: click (with the mouse)
   on the "import turtle" line (inside the Python Shell window) and then hit the enter
   key - notice the command appears at the &gt;&gt;&gt; prompt - hit enter one more time
   to, well, enter it. Repeat the "pat = ..." command too.</p>
<p>Now, to test your function, try calling it with various values for width and height:</p>
<pre>&gt;&gt;&gt; drawRectangle(pat, 20, 50)
&gt;&gt;&gt; drawRectangle(pat, 100, 75)</pre>
<p>You can also try moving pat between the rectangles, picking up the pen first&mdash;for
   example this will move pat over a bit before drawing the next rectangle.</p>
<pre>&gt;&gt;&gt; pat.up()
&gt;&gt;&gt; pat.forward(100)
&gt;&gt;&gt; pat.down()
&gt;&gt;&gt; drawRectangle(pat, 60, 80)</pre>

<p>After playing with pat and the drawRectangle function for awhile, move on to Step 5.</p>

<h3>Step 5: Write a function to draw a house</h3>
<p><b>First switch roles between pilot and navigator if you did not already do that.</b></p>
<p>Add a function named <b>drawHouse()</b> to the lab02.py file according to the following specifications:</p>
   <ol>
   <li>Add a couple of blank lines after the end of your drawRectangle function definition.</li>
   <li>The new function header must name two parameters in this new function: a turtle, and a width.</li>
   <li>Precede the header with an appropriate comment like you did for drawRectangle.</li>
   <li>The function body should use the turtle parameter to draw a house - make the
     height of the house proportional to its width. <i>Use the
     drawRectangle function</i> to make part of the house - <em>abstraction is good!</em></li>
   </ol>
   It should work correctly if used as follows:
<pre>&gt;&gt;&gt; drawHouse(pat, 100)    # a really big house
&gt;&gt;&gt; drawHouse(pat, 10)     # a tiny house (just 10 pixels wide)</pre>
<table border="0"><tr>
  <td width="50%">Here is an example:<img align="center" src="house.png" alt="House" width="200"></td>
  <td align="left">Note: your house does not have to look exactly like this&mdash;i.e. the proportions of the
      width/height and the steepness of the roof can be different. As long as it &quot;looks like
      a house&quot;, that's good enough for this lab.</td>
</tr></table>

<blockquote>
<h3>Step 6: Draw a block of houses</h3>
<ul>
<li>Make a function to draw a block (row) of houses.
    Precede the function definition with an appropriate comment, like always!
    Write the function header to take three
    parameters: a turtle, the width of one house, and the number of houses to draw:
    <pre>def drawBlock(turtle, width, number):</pre>
    <p>The function should draw as many houses as the parameter named number specifies,
    and each house should have the specified width. Separate the houses by moving the
    turtle without drawing any lines - pick up the pen, move, and then put it down again 
    (how do you do that? Look at the hints in Step 4). 
    You should separate the houses by 1/2 house width. Here is an example
    (12 houses, each width 25 in the original drawing):</p>
    <p><img src="12houses.png" alt="row of houses"></p></li>
</ul>
</blockquote>

<h3>Step 7: Show off your work and get credit for the lab</h3>
<table bgcolor="yellow" border="1" cellpadding="4"><tbody><tr><td>
   Get your TA's attention to inspect your work, and to record your lab completion.
</td></tr></tbody></table>

ZIAD

<h3>Step 8: Submit your work to submit.cs</h3>
Your final submission, the file called lab02.py, should now have 4 functions defined therein: one for the factorial function and the other 3 for the Turtle graphics functions, drawRectangle, drawHouse, and drawBlock.

Navigate to that page, and upload your `lab02.py` file.
EDIT: You will see 100/100 points, if it passes the tests. 

Or, if you are working on the ECI/CSIL/lab linux systems, you can also *OPTIONALLY* submit at the command line with this command, provided you are in the correct folder/diretory:

```
~submit/submit -p XXXX lab02.py
```

The first time you use this method, it will ask for your email address: use your full umail address (e.g. cgaucho@umail.ucsb.edu). For password, use the password that you enter for the submit.cs system. You may save these credentials if you don’t want to have to type them in every time.

<hr>
<p><font size="1">
Copyright 2018, Ziad Matni, CS Dept, UC Santa Barbara. Adapted (heavily) from work by Phill Conrad and others. Permission to copy for non-commercial, non-profit, educational purposes granted, provided appropriate credit is given;  all other rights reserved
</font></p>


