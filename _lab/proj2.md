---
layout: lab
num: project2
ready: false
desc: "Strings, Lists, Dictionaries, and File I/O"
assigned: 2018-03-02 09:30:00.00-7
due: 2018-03-16 23:59:59.00-7
---
<div markdown="1">

<h1>CS 8, Winter 2018: Programming Project 2</h1>
<h2>Due: Friday, 3/16 11:59 PM</h2>
<h2>Absolutely no late submissions allowed</h2>

NOTE: This project is due on the very last day of the Winter quarter, Friday, 3/16. As such you cannot submit it any later than that (that is, I will not accept ANY late submissions).

HINT: Don't wait until the last minute to do this! 

<h2>It is optional, but very highly recommended, to work with a partner on this project.</h2>
<h1>PLEASE READ ALL THE INSTRUCTIONS CAREFULLY!!!</h1>

<strong>Before you begin:</strong>
Obtain copies of these 8 files (the first 2 are the start-up Python code files that you will edit and submit at the end):
<ol>
<li>    CountChars.py</li>
<li>    findWord.py</li>

<li>    theRaven.txt</li>
<li>    longer.txt </li>
<li>    short.txt </li>
<li>    longersample.txt</li>  
<li>    shortsample.txt </li> 
<li>    webpagesample.txt</li>
</ol>
	
The files are found at <code><a href="http://cs.ucsb.edu/~zmatni/cs8w18/projects/proj2" target="_blank">http://cs.ucsb.edu/~zmatni/cs8w18/projects/proj2/</a></code>, and save them in whatever folder you choose to work on this project (presumably <code>~/cs8/proj2/</code>).
  
Edit the comments at the beginnings of these files to include your name (and the name of your partner, if you are working with another student) and the date each program is written. 

<hr>
<!-- PART 1-->
<h2>findWord.py</h2>
  	
(40 points: string manipulation) This program calls a function (findIt) that manipulates strings. The function is
run over and over again until the user enters specific outputs to quit.  
<code>findIt(lines, word)</code> takes in a group of strings stored together (that is, lines in a <b>list</b>) 
in an EXTERNAL FILE called "theRaven.txt", which contains the entire poem, "The Raven", by Edgar Allan Poe. 
It then goes through each string (line) in this list and searches for the sub-string "word". 
If it finds "word", it prints the entire line, preceded by the line number (these start at 0). See example below.

The line number is the position of the line in the list. So for example, if the list has 125 lines in it and the one indexed number 103 is "found" by the function and is "Quoth the Raven "Nevermore"", then the function would output:
<pre>
103             Quoth the Raven "Nevermore." 
</pre>

The reading of the external file is done for you in the main findWord.py program.
    
HINTS: When a list contains multiple values, you can access each individual one with a for-loop, 
for example, given a list called <code>people = ["joe", "mary", "bob", "chincilla"]</code>, you would do this: 
<pre>
>>> for one in people:
	   print(one)
joe
mary
bob
chinchilla
</pre>

This will print out each name in the list individually, each on a new line.
If you modify the last line as <code>print(one, end= " ")</code> (note the space character between 
the quotation marks), you will print each item next to the following one on one line with a 
space character between each one. 
<pre>
>>> for one in people:
       print(one, end=" ")
joe mary bob chinchilla >>>
</pre>

If you modify it further as <code>print(one, end= "")</code> (note the ABSENCE of a space characer between 
the quotes), you will print each item immediately next to the other with no space character between them.

When done, your results should match the following 2 example sample runs from our solution.

<div markdown="1">
```
$ python3 findWord.py 
Enter word to find (or RETURN to quit): more
Here are all the lines that contain the word more
5             Only this and nothing more.” 
12             Nameless here for evermore. 
19             This it is and nothing more.” 
26             Darkness there and nothing more. 
33             Merely this and nothing more. 
40             ’Tis the wind and nothing more!” 
47             Perched, and sat, and nothing more. 
54             Quoth the Raven “Nevermore.” 
61             With such name as “Nevermore.” 
66     Till I scarcely more than muttered “Other friends have flown before— 
68             Then the bird said “Nevermore.” 
75             Of ‘Never—nevermore’.” 
82             Meant in croaking “Nevermore.” 
86     This and more I sat divining, with my head at ease reclining 
89             She shall press, ah, nevermore! 
96             Quoth the Raven “Nevermore.” 
103             Quoth the Raven “Nevermore.” 
110             Quoth the Raven “Nevermore.” 
117             Quoth the Raven “Nevermore.” 
124             Shall be lifted—nevermore!
```
```
$ python3 findWord.py
Enter word to find (or RETURN to quit): Raven
Here are all the lines that contain the word Raven
43 In there stepped a stately Raven of the saintly days of yore; 
52 Ghastly grim and ancient Raven wandering from the Nightly shore— 
54             Quoth the Raven “Nevermore.” 
63     But the Raven, sitting lonely on the placid bust, spoke only 
77     But the Raven still beguiling all my fancy into smiling, 
96             Quoth the Raven “Nevermore.” 
103             Quoth the Raven “Nevermore.” 
110             Quoth the Raven “Nevermore.” 
117             Quoth the Raven “Nevermore.” 
119     And the Raven, never flitting, still is sitting, still is sitting 
```
</div>

<!-- PART 2-->
<h2>CountChars.py</h2>
(40 points: reading from file or URL, formatting strings, data structures)

Begin a new file named <strong>CountChars.py</strong> by typing a comment at the top with your name (and the name of your lab partner if you work together), and the current date.

You will notice the instructions are a bit shorter this time. You are given a problem to solve, <em>but you must figure out how to solve it yourself</em>. Keep in mind what you have learned about top-down programming by stepwise refinement: break the problem into meaningful parts; then solve each part separately. And have fun!

The problem is to write a Python3 program that reads a text file or web page named by the user, and prints a neat table showing the counts of all of the different characters it reads. You must also meet the following explicit specifications:

Since we insist that your output will exactly match the results of our solution (see the 3 examples below), copy the following string and dictionary constants and paste them to the beginning of countchars.py (after your header comment of course). These are already entered for you in the start-up file called <b>CountChars.py</b>.

```py
# strings that must be used for output:
prompt = "Enter filename: "
titles = "char       count\n----       -----"
itemfmt = "{0:5s}{1:10d}"
totalfmt = "total{0:10d}"
whiteSpace = {' ':'space', '\t':'tab', '\n':'nline', '\r':'crtn'}
```

Make it so that when you run the module in IDLE, it should immediately instruct the user to enter the filename, and then it should print the table of counts in the Python shell window. Alternatively, a user can run the program directly from the command prompt without ever starting Python or IDLE, by typing the following:

```
-bash-4.2$ python3 CountChars.py
```

Execution must proceed as follows:

<ol markdown="1">
<li>Use the built-in function input to get the filename from the user. Pass the string named prompt to this function.</li>

<li>If the filename does not begin with "http" then assume it is a local file, and open it for reading with the built-in open function. Otherwise import and use the urllib.request.urlopen function to open the web page for reading. The program has to be able to do this automatically. Go back to the slides from class for when we talked about this topic.</li>

<li>Read all of the text in the file or web page, and count each different character in it. Ignore the case of characters (e.g., count both 'A' and 'a' as 'a').</li>

<li>Print the string named <strong>titles</strong>. Then print the table of characters and their counts in ASCII order, and print the total character count at the bottom. Hint: There are 128 characters in the ASCII code, starting from 0 and ending at 127.</li>

<li>Use the string named <strong>itemfmt</strong> to print each interior row of the table in the proper format. For example, if c is a character, and ccount is its count (which should be recorded in the dictionary you created), then print that row of the table as follows:</li>

<div markdown="1">
```py
print( itemfmt.format(c, ccount) )
```
</div>

<li>If the character being printed is one of the white space characters in the dictionary named <strong>whitespace</strong>, then print its description instead of the character itself. For example:</li>

<div markdown="1">
```py
print( itemfmt.format(whiteSpace[c], ccount) )
```
</div>

<li>Use the string named <strong>totalfmt</strong> to properly print the total character count. If this count is named <strong>total</strong>, for example:</li>

<div markdown="1">
```py
print( totalfmt.format(total) )
```
</div>

<li>Fully test your program. Here are sample input files and web pages, and the associated results from our solution. Make sure that your results <em><strong>exactly match these results</strong></em>. Also realize that the graders will probably test other inputs too.</li>

</ol>

<table>
<tr><td><strong>File/Page</strong></td><td><strong>Program Run</strong></td></tr>
<tr><td><a href="http://www.cs.ucsb.edu/~zmatni/cs8w18/projects/proj2/short.txt">short.txt</a></td>
<td><a href="http://www.cs.ucsb.edu/~zmatni/cs8w18/projects/proj2/shortsample.txt">short.txt run</a></td></tr>
<tr><td><a href="http://www.cs.ucsb.edu/~zmatni/cs8w18/projects/proj2/longer.txt">longer.txt</a></td><td>
<a href="http://www.cs.ucsb.edu/~zmatni/cs8w18/projects/proj2/longersample.txt">longer.txt run</a></td></tr>
<tr><td><a href="http://www.cs.ucsb.edu/~zmatni/cs8w18/projects/proj2/index_example.html">http://cs.ucsb.edu/~zmatni/cs8w18/projects/proj2/index_example.html</a></td><td>
<a href="http://www.cs.ucsb.edu/~zmatni/cs8w18/projects/proj2/webpagesample.txt">CS8 Home Page run</a></td></tr>
</table>

These files can also be located at:
<a href="http://www.cs.ucsb.edu/~zmatni/cs8w18/projects/proj2/">http://www.cs.ucsb.edu/~zmatni/cs8w18/projects/proj2/</a>.

<hr>
<h3>How we will grade this project</h3>
You will submit this project as TWO files on submit.cs (see below). However, you will be ADDITIONALLY graded on the following:

a) That you have followed directions carefully (worth 10 points), and

b) That you have left sufficient comments in your code (worth 10 points), and

c) That you did not copy code from the Internet or someone else (we will run anti-plagiarism software on your submissions and if you are caught doing so, you will get a zero on this project and I will have to report you to the CS Department and to the University, as is the strict policy
at UCSB. If you have *any* questions about this, ask me BEFORE you submit your wort UCSB. If you have *any* questions about this, ask me BEFORE you submit your work.

<h3>How to turn this work in</h3>

Your final submission will be the 2 Python code files: **findWord.py** and **CountChars.py**. MAKE SURE YOU HAVE NOT EDITED OUT THE TESTER CASES THAT I PUT IN THOSE ORIGINAL FILES</b>.

Navigate to the <b>submit.cs</b> website, select <b>project2</b>, register your partner (if you have one), and then upload your 2 files. You will see 80/80 points, if it passes the tests. 

If you run into problems, be sure to ask questions on Piazza or visit your TA's or your instructor's office hours.

<hr>
<p><font size="1">
Copyright 2018, Ziad Matni, CS Dept, UC Santa Barbara. Permission to copy for non-commercial, non-profit, educational purposes granted, provided appropriate credit is given;  all other rights reserved.
</font></p>

