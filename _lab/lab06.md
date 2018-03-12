---
layout: lab
num: lab06
ready: false
desc: "Recursive Functions"
assigned: 2018-03-13 08:00:00.00-7
due: 2018-03-14 23:59:59.00-7
---
<div markdown='1'>

<h2>Goals for this lab</h2>

By the time you have completed this lab, you should be able to:
<ol>
<li>Write simple recursive functions in Python.</li>
</ol>

<h2>Step by Step Instructions</h2>
**Step 0:** Get together with your assigned lab partner.
Select whichever partner was pilot first last time to be navigator first this time. This lab's pilot should log in and create a lab06 directory under your cs8 folder. You will work in this account for the rest of the lab. If your partner is more than 5 minutes late, ask the TA to pair you with someone else for this week.

**Step 1A:** Log in, create a lab06 directory, and copy the start-up file
Decide which one of you will be the first pilot for this lab, and then log in to the pilot's account and create a directory called lab06 inside his/her cs8 folder. You will work in this account for the rest of the lab, but remember to switch often between pilot and navigator roles during the course of the lab.

**IMPORTANT!**
Copy the file <code><a href="http://cs.ucsb.edu/~zmatni/cs8w18/labs/lab06/lab06.py" target="_blank">http://cs.ucsb.edu/~zmatni/cs8w18/labs/lab06/lab06.py</a></code> using the Linux <b>cp</b> command and place it in whatever folder you choose to work on this project (presumably <code>~/cs8/lab06/</code>).

**Step 1B:** Start IDLE. Then, select &quot;File-&gt;Open&quot; and open the lab06.py that you just copied.
Now that you have it open, you can start designing the function(s) that you need for this lab. You MUST have a function called isPalindrome(string). You may need one or more additional functions. **BE VERY CAREFUL ABOUT NAMING THE FUNCTION isPalindrome EXACTLY LIKE I'VE ASKED YOU TO!**

**Step 2A:** isPalindrome(string)

Write a function named isPalindrome(string) that checks if string is a palindrome or not and returns the appropriate Boolean value.
A palindrome is a string that spells backwards EXACTLY like it spells forward, so for example, the string "catac" is a palindrome, and so is "mine enim".
Note that while "madamimadam" is a palindrome, that "madam I'm adam" is NOT because of the space characters and the single quote therein.

Your solution MUST make use of one or more recursive function(s). Your solution MUST NOT include ANY for or while loops.

HINT: Make use of one of the examples we went through in class on Monday.

**Step 2B:** 

Write your lab06.py program to include the function above and any other function(s) you deem necessary. 

**Step 3:** Show off your work and get credit for the lab

<table bgcolor="yellow" border="1" cellpadding="4"><tbody><tr><td>
   Get your TA's attention to inspect your work, and to record your lab completion.
</td></tr></tbody></table>

<blockquote>

**Step 4:** Submit your work to submit.cs

Your final submission is the file called lab06.py, which should have started out with the start-up file I gave you (see top of this document) and now has at LEAST one function called **isPalindrome**.

Note that the start-up file tests your program out with some simple cases. You may want to test your program in additional ways. Note that submit.cs will test *other* test cases on your functions as well.

Navigate to the <b>submit.cs</b> website, select <b>lab06</b>, register your partner, and then upload your `lab06.py` file. EDIT: You will see 80/80 points, if it passes the tests. 

You will earn the other 20 points (to make this lab worth a total of 100 points) as follows:

1) Your TA will manually have to look at your function in lab and see that it works. This is worth 10 points. If you do not finish this part of the lab during regular hours, you will not get this 10 point credit.

2) Your TA will also manually look at your submitted code on submit.cs and verify that you did the correct work AND that you have left enough comments to explain your code. This is worth another 10 points. If you use Python code or techniques that were not covered in class or are not in the textbook, you will lose these 10 points on the lab.

<hr>
<p><font size="1">
Copyright 2018, Ziad Matni, CS Dept, UC Santa Barbara. Permission to copy for non-commercial, non-profit, educational purposes granted, provided appropriate credit is given;  all other rights reserved
</font></p>
