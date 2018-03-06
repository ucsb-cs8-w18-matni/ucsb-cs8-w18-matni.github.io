---
layout: lab
num: lab05
ready: true
desc: "Using File I/O in Python"
assigned: 2018-03-06 08:00:00.00-7
due: 2018-03-07 23:59:59.00-7
---
<div markdown='1'>

<h2>Goals for this lab</h2>

By the time you have completed this lab, you should be able to:
<ol>
<li>Know how to read/write external file (i.e. use file I/O) with Python code.</li>
</ol>

<h2>Step by Step Instructions</h2>
**Step 0:** Get together with your assigned lab partner.
Select whichever partner was pilot first last time to be navigator first this time. This lab's pilot should log in and create a lab05 directory under your cs8 folder. You will work in this account for the rest of the lab. If your partner is more than 5 minutes late, ask the TA to pair you with someone else for this week.

**Step 1A:** Log in, create a lab05 directory, and copy the start-up file
Decide which one of you will be the first pilot for this lab, and then log in to the pilot's account and create a directory called lab05 inside his/her cs8 folder. You will work in this account for the rest of the lab, but remember to switch often between pilot and navigator roles during the course of the lab.

**IMPORTANT!**
Copy the file <code><a href="http://cs.ucsb.edu/~zmatni/cs8w18/labs/lab05/lab05.py" target="_blank">http://cs.ucsb.edu/~zmatni/cs8w18/labs/lab05/lab05.py</a></code> using the Linux <b>cp</b> command and place it in whatever folder you choose to work on this project (presumably <code>~/cs8/lab05/</code>).
 Also, copy the file <code><a href="http://cs.ucsb.edu/~zmatni/cs8w18/labs/lab05/myInput.txt" target="_blank">http://cs.ucsb.edu/~zmatni/cs8w18/labs/lab05/myInput.txt</a></code>. This is an example text file that one of your functions will be "reading".

**Step 1B:** Start IDLE. Then, select &quot;File-&gt;Open&quot; and open the lab05.py that you just copied.
Now that you have it open, you can start designing the 2 functions that you need for this lab: FileRead and FileWrite. **BE VERY CAREFUL ABOUT NAMING THE FUNCTIONS EXACTLY WHAT I ASK YOU TO NAME THEM!**

**Step 2A:** FileRead

Write a function named FileRead (no arguments) to read a file (it gets the name by asking the user, i.e. using the input() function). It will read all the lines in the file **as a list of strings** and count of how many lines are in it. Finally, it will return the aforementioned list of strings. The function header should like this:

```
def FileRead():
```

And here is an example test run on Python IDLE (careful! the myInput.txt file MUST BE placed in the correct directory called <code>/cs/student/<your username here>/cs8/lab05/<code>. Ask your TA for help if the following does not work because of wrong file placement):

```
>>> Lines = FileRead()
Enter filename: /cs/student/joeshmoe/cs8/lab05/myInput.txt
There are 16 lines in the file myInput.txt

```

The variable <code>Lines</code> will be used in Step 2B below.

**Step 2B:** FileWrite

Write a function named FileWrite that will write all the lines read from the previous function, EXCEPT any lines that begin with the letter "I" - that is, upper-case "I", into file called "myout.txt" (it's always called that). This function takes in a list of strings as an input (the variable allLines). After writing the file properly, it prints out a simple message: "myout.txt written" and nothing else.

```
def FileWrite(allLines):
```

And here is an example test run on Python IDLE:

```
>>> FileWrite(allLines)
myout.txt written
```

**Step 2C:** Putting it all together

Write your lab05.py program to include the 2 functions above. The start-up file that I've provided for you will run the two functions back to back. When you test run your entire program (and you see the "myout.txt written" message), look at <code>myout.txt</code>. Does it look like the file <code>myInput.txt</code>, but without lines that had started with the letter "I"? If so, and all the other lines were kept intact, you have succeeded!

**Step 3:** Show off your work and get credit for the lab

<table bgcolor="yellow" border="1" cellpadding="4"><tbody><tr><td>
   Get your TA's attention to inspect your work, and to record your lab completion.
</td></tr></tbody></table>

<blockquote>

**Step 4:** Submit your work to submit.cs

Your final submission is the file called lab05.py, which should have started out with the start-up file I gave you (see top of this document) and now have TWO functions that you wrote: FileRead and FileWrite. **BE VERY CAREFUL ABOUT NAMING THE FUNCTIONS EXACTLY WHAT I ASK YOU TO NAME THEM AND MAKE SURE THE FILE IS CALLED lab05.py AND NOTHING ELSE!!**

Note that the start-up file tests this out on the text file I've given you (myInput.txt). You may want to test your program on other text files (go crazy!). Note that submit.cs will test *other* test cases on your functions as well.

Navigate to the <b>submit.cs</b> website, select <b>lab05</b>, register your partner, and then upload your `lab05.py` file. EDIT: You will see 80/80 points, if it passes the tests. 

You will earn the other 20 points (to make this lab worth a total of 100 points) as follows:

1) Your TA will manually have to look at your function in lab and see that it works. This is worth 10 points. If you do not finish this part of the lab during regular hours, you will not get this 10 point credit.

2) Your TA will also manually look at your submitted code on submit.cs and verify that you did the correct work AND that you have left enough comments to explain your code. This is worth another 10 points. If you use Python code or techniques that were not covered in class or are not in the textbook, you will lose these 10 points on the lab.

<hr>
<p><font size="1">
Copyright 2018, Ziad Matni, CS Dept, UC Santa Barbara. Permission to copy for non-commercial, non-profit, educational purposes granted, provided appropriate credit is given;  all other rights reserved
</font></p>
