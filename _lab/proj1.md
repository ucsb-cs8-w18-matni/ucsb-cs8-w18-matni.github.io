---
layout: lab
num: project1
ready: true
desc: "Doing Mathematical Calculations & String Manipulations with Python"
assigned: 2018-02-09 09:30:00.00-7
due: 2018-02-23 23:59:59.00-7
---
<div markdown="1">

<h1>CS 8, Winter 2018: Programming Project 1</h1>
<h2>Due: Friday, 2/23 11:59pm</h2>

<h1>PLEASE READ ALL THE INSTRUCTIONS CAREFULLY!!!</h1>

<strong>Before you begin:</strong>
Read all of Miller/Ranum chapters 1, 2 and 3 and obtain copies of these 5 files:
<ol>
<li>    sphere.py</li>
<li>    screensize.py</li>
<li>    fibonacci.py</li>
<li>    decode.py</li>
<li>    message.txt</li>
</ol>
	
The files are found at <code><a href="http://cs.ucsb.edu/~zmatni/cs8w18/projects/proj1" target="_blank">http://cs.ucsb.edu/~zmatni/cs8w18/projects/proj1/</a></code>. Copy them using the Linux <b>cp</b> command and place them in whatever folder you choose to work on this project (presumably <code>~/cs8/proj1/</code>).
  
You have TWO WEEKS to work on this project and turn it in. It is highly recommended that you do this lab with a partner, although I am making that *optional* in this case.

Edit the comments at the beginnings of these files to include your name (and the name of your partner, 
if you are working with another student) and the date each program is written. 
This is IMPORTANT, and it applies to all future programs too!

<hr>
<!-- PART 1-->
<h2>sphere.py</h2>
(20 points: some calculations) Add the following four functions to sphere.py (three of them are taken from Exercises 2.1, 2.2 and 2.3 on page 81 of the text, and the other is a natural addition):

<ol type="a">
<code>circumference(r)</code> - to return the circumference of a circle with radius<code>r</code>. [<code>2&pi;r</code>]
<code>area(r)</code> - to return the area of a circle with radius <code>r</code>. [<code>&pi;r<sup>2</sup></code>]
<code>surface(r)</code> - to return the surface area of a sphere with radius
<code>r</code>. [<code>4&pi;r<sup>2</sup></code>]
<code>volume(r)</code> - to return the volume of a sphere with radius
<code>r</code>. [<code>4&pi;r<sup>3</sup>/3</code>]
</ol>

Notes:
<ol>
The function headers must <em>exactly match</em> the ones above, or the testing code will not work.
Use <code>math.pi</code> (after importing the math module) for the value of &pi; in all of these calculations.
We suggest you test them one at a time in the Python shell. When they are all done, you can run the module. Here are two sample runs to which you can compare your results:
</ol>

<pre>
-bash-4.2$ <b>python3 sphere.py</b> 
enter radius: <b>2.5</b>
circumference: 15.7
circle area: 19.6
sphere volume: 65.4
sphere surface area: 78.5
-bash-4.2$ <b>python3 sphere.py</b> 
enter radius: <b>10</b>
circumference: 62.8
circle area: 314.2
sphere volume: 4188.8
sphere surface area: 1256.6
</pre>

<hr>
<!-- PART 2-->
<h2>screensize.py</h2>
(20 points: slightly more complicated calculations) Add two functions to screensize.py to calculate the height and width of a display
screen, given the diagonal screen size (D) and the aspect ratio (W:H), using these formulas:

<img src="heighteq.png">..................................
<img src="widtheq.png">

<ol type="a">
<code>height(D, W, H)</code> - where D, W and H are described above.
<code>width(W, H, screenHeight)</code> - where W and H as above, and screenHeight is the result of the height function.
</ol>

When done, your results should match the following sample runs from our solution.
<pre>
-bash-4.2$ <b>python3 screensize.py</b> 
enter D, W, H (separated by commas): <b>51, 4, 3</b>
width = 40.8, height = 30.6
-bash-4.2$ <b>python3 screensize.py</b> 
enter D, W, H (separated by commas): <b>64, 16, 9</b>
width = 55.8, height = 31.4
</pre>
	
<hr>
<!-- PART 3-->
<h2>fibonacci.py</h2>
<b>First switch roles between pilot and navigator if you did not already do that.</b>
(Based on Exercise 2.14 from page 56 of the text). 

(20 points: accumulator pattern) The numbers in the Fibonacci Series are characterized by the fact that 
every number after the first two is the sum of the two preceding ones, so the sequence starts with a 1 and 1 
and continues on. This gives us this series of numbers: 1 1 2 3 5 8 13 21 34 55… etc…
Write a Python program that prints out the first n numbers in the Fibonacci Series. Do not copy a solution from 
an online source. You cannot recursively call the function (that means have the function call itself) and should mostly use <code>if/else</code> and <code>for</code> statements.  
  
Here is the required function header and an appropriate comment - type or copy/paste them into your fibonacci.py file at least one blank line below the end of the factorial function:
<pre>
# fib - returns nth term of Fibonacci sequence:
#     1, 1, 2, 3, 5, 8, ... So fibo(6) = 8
def fibo(n):
</pre>

<code>fibo(n)</code> - where n is the number of terms in the series.
Examples:
If n is equal to 1, then just include the first term in the equation: <code>(1)</code>.
If n is equal to 2, then just include the first and the second term in the equation: <code>(1 1)</code>.
If n is equal to 6, include the first six terms: <code>(1 1 2 3 5 8)</code>

When done, your results should match the following sample runs from our solution.
<pre>
-bash-4.2$ <strong>python3 fiboncci.py</strong> 
enter number of terms: <b>9</b>
1 1 2 3 5 8 13 21 34
-bash-4.2$ <strong>python3 fibonacci.py</strong>
enter number of terms: <b>1</b> 
1
-bash-4.2$ <strong>python3 fibonacci.py</strong>
enter number of terms: <b>5</b>
1 1 2 3 5 
</pre>

Test your function thoroughly to be sure it is correct. Verify that both fibo(1) and fibo(2) return 1, fibo(3) returns 2, and so on. You may assume that n will always be greater than 0, but find out what the function returns for 0 or negative values too, and try to understand why it returns what it does in such cases.

*Hint:* Another way to write this is: fibo(i) = fibo(i-1) + fibo(i-2).  This does not mean that to calculate fibo(i) you should call fib for both of the lower results.  What this really means is that the result of this iteration is dependent on your result of the last iteration and the iteration before that.  Storing those (two) partial results are the key to getting this algorithm correct.

Remember to let both partners think about this before diving in.  Do not skip the design step, in which you work this out on paper before trying to write in Python.

*NEXT STEPS (NOT DONE YET!!):*

The "golden ratio" is often denoted by the lower case Greek letter, phi (&phi;) and appears in natural constructs everywhere from plants and flowers to the way galaxies form. This ratio can be approximated by using the Fibonacci function. In particular, as the value of n increases, the value of the fraction F(n+1)/F(n) gets nearer and nearer to &phi;. 

Here F denotes the Fibonnaci function. In calculus, this relationship is expressed as a limit, as n approaches infinity:

<img src="fiblimit.png">

Of course, it is not necessary to plug &#8734; into the formula to <i>approximate</i> the ratio, let alone (&#8734; + 1)! Your job is: Find the smallest value of n for which the ratio is within 1.0e-10 of this approximate value of &phi;: 1.6180339887.

Devise a strategy using your fib function, and other things you have learned so far in CS 8.

Things you should know:
<ol>
1.0e-10 is an actual floating point constant equal to 0.0000000001.
One should not use == to compare floating point numbers, because very slight differences will cause false results. Instead, the best approach is to calculate the absolute value of the difference between the two numbers, and then verify this difference is less than a very small value (like 1.0e-10).
</ol>

In Python, the absolute value of a number is found with the abs function:
<pre>
>>> abs(-5.5)
5.5
>>> abs(1.05)
1.05
</pre>

<hr>

<!-- PART 4-->
<h2>decode.py</h2>
(20 points: string manipulation)In this last exercise, you are going to read in an external file that contains a 
coded message and de-code it!

Reading the external file is done for you, as with the last exercise. The decoding should be performed with this scheme in mind:

When originally coded, each letter was transposed by adding 5 to its ASCII code, except for all lower case letters 'a',
which were not changed. Therefore you have to figure out a way to reverse this process in order to decode.

The function that you have to write, <code>decode(lines)</code>, takes in a group of strings stored together (as in the last exercise) in an EXTERNAL FILE 
called "message.txt", which contains a coded message that you must decipher. The function then goes through each 
string (line) in this list, then each character in the line, and does the decoding (on a character-by-character basis). 
Finally, it has to print out each line it decodes. See the example below (which does not use the file that you will be using):

<pre>
-bash-4.2$ cat message.txt
Ymjwj,x%a%qnyyqj%gqahp%xuty%ts%ymj%xzs%ytia~3
Ny,x%ymj%xarj%tqi%ymnsl%ax%~jxyjwia~3
-bash-4.2$ 
-bash-4.2$ python3 decode.py
There's a little black spot on the sun today.
It's the same old thing as yesterday.
</pre>

The Linux command "cat message.txt" means "show me what's in the file message.txt". As you see from the example, the 
file contains garbled (coded) text. The Python program, decode.py, if working properly, prints out the decoded text.

<hr>
<h3>How we will grade this project</h3>
You will submit this project as multiple files on submit.cs (see below). However, you will be ADDITIONALLY graded on the following:

a) That you have followed directions carefully (worth 10 points), and

b) That you have left sufficient comments in your code (worth 10 points), and

c) That you did not copy code from the Internet or someone else (we will run anti-plagiarism software on your submissions and if you are caught doing so, you will get a zero on this project and I will have to report you to the CS Department and to the University, as is the strict policy
at UCSB. If you have *any* questions about this, ask me BEFORE you submit your wort UCSB. If you have *any* questions about this, ask me BEFORE you submit your work.

<h3>How to turn this work in</h3>

Your final submission will be all the 5 files (4 of which you will modify). MAKE SURE YOU HAVE NOT EDITED OUT THE TESTER CASES THAT I PUT IN THOSE ORIGINAL FILES (i.e. THE PARTS BELOW THE COMMENTS THAT SAY <b>"# do not change any part of the code below"</b>)

Navigate to the <b>submit.cs</b> website, select <b>proj1</b>, register your partner (if you have one), and then upload your 5 files. You will see 80/80 points, if it passes the tests. 

If you run into problems, be sure to ask questions on Piazza or visit your TA's or your instructor's office hours.

<hr>
<p><font size="1">
Copyright 2018, Ziad Matni, CS Dept, UC Santa Barbara. Permission to copy for non-commercial, non-profit, educational purposes granted, provided appropriate credit is given;  all other rights reserved.
</font></p>


