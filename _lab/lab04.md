---
layout: lab
num: lab04
ready: true
desc: "Using Lists in Python"
assigned: 2018-02-27 08:00:00.00-7
due: 2018-02-28 23:59:59.00-7
---
<div markdown='1'>

<h2>Goals for this lab</h2>

By the time you have completed this lab, you should be able to:
<ol>
<li>Use Python lists </li>
</ol>

<h2>Step by Step Instructions</h2>
**Step 0:** Get together with your assigned lab partner.
Select whichever partner was pilot first last time to be navigator first this time. This lab's pilot should log in and create a lab04 directory under your cs8 folder. You will work in this account for the rest of the lab. If your partner is more than 5 minutes late, ask the TA to pair you with someone else for this week.

**Step 1A:** Log in, create a lab04 directory, and copy the start-up file
Decide which one of you will be the first pilot for this lab, and then log in to the pilot's account and create a directory called lab04 inside his/her cs8 folder. You will work in this account for the rest of the lab, but remember to switch often between pilot and navigator roles during the course of the lab.

**IMPORTANT!**
Copy the file <code><a href="http://cs.ucsb.edu/~zmatni/cs8w18/labs/lab04/lab04.py" target="_blank">http://cs.ucsb.edu/~zmatni/cs8w18/labs/lab04/lab04.py</a></code> using the Linux <b>cp</b> command and place it in whatever folder you choose to work on this project (presumably <code>~/cs8/lab04/</code>).

**Step 1B:** Start IDLE. Then, select &quot;File-&gt;Open&quot; and open the lab04.py that you just copied.
Now that you have it open, you can start designing the 5 functions that you need for this lab: printSortedListAscending, printSortedListDescending, checkList, ListAverage, ListMedian. **BE VERY CAREFUL ABOUT NAMING THE FUNCTIONS EXACTLY WHAT I ASK YOU TO NAME THEM!**

**Step 2A:** printSortedListAscending

Write a function named printSortedListAscending to print the sorted elements, in ASCENDING order, of a list with labels showing the sorted order of each element. The function header should like this:

```
def printSortedListAscending(aList):
```

And here is an example test run on Python IDLE:

```
>>> myList = [92.5, 127.1, 9, 104.2, 78.4]
>>> printSortedListAscending(myList)
1 9
2 78.4
3 92.5
4 104.2
5 127.1
```

Test your function from the Python shell window on various types of lists with varying lengths.

**Step 2B:** printSortedListDescending

Write a function named printSortedListDescending to print the sorted elements, in DESCENDING order, of a list with labels showing the sorted order of each element. The function header should like this:

```
def printSortedListDescending(aList):
```

And here is an example test run on Python IDLE:

```
>>> myList = [92.5, 127.1, 9, 104.2, 78.4]
>>> printSortedListDescending(myList)
1 127.1
2 104.2
3 92.5
4 78.4
5 9
```

Test your function from the Python shell window on various types of lists with varying lengths.

**Step 2C:** checkList

Write a function named checkList that takes as parameter a list and RETURNS a Boolean value (i.e. True or False). This return value must equal True (careful: this is a Boolean value, not a string!!) ONLY if every item in the list is an integer or if its a float, otherwise, it should return False. Hint: We worked on a function like this in lecture on Monday, 2/26!

The function header should look like this:

```
def checkList(aList):
```

And here is an example test run on Python IDLE:

```
>>> myList = [92.5, 127.1, 9, 104.2, 78.4]
>>> print(checkList(myList))
True

>>> myOtherList = ['abc', 23, 0.45]
>>> print(checkList(myOtherList))
False
```

**Step 2D:** ListAverage

Write a function named ListAverage that takes as parameter a list, CHECKS to see that it is all integers or floats (using the checklist() function from above), and, if so, RETURNS the average of the entire list contents. If the contents are deemed not be "average"-able (i.e. if at least one item in the list is not an integer), then this function must instead return a string value equal to "Not an integer list".

The function header should look like this:

```
def ListAverage(aList):
```

And here is an example test run on Python IDLE:

```
>>> myList = [5, 5, 4, 4, 5]
>>> ListAverage(myList)
4.6

>>> myOtherList = [5, 5, 4, 'f', 5, 5]
>>> ListAverage(myOtherList)
'Not an integer list'
```

**Step 2E:** ListMedian

Write a function named ListMedian that takes as parameter a list, CHECKS to see that it is all integers or floats (using the checklist() function from above), and, if so, RETURNS the median of the entire list contents. If the contents are have at least one item in the list is not an integer, then this function must instead return a string value equal to "Not an integer list". Hint: If you look at the slides from lecture on Monday, 2/26, you should see an example of this function.

The function header should look like this:

```
def ListMedian(aList):
```

And here is an example test run on Python IDLE:

```
>>> myList = [5, 5, 4, 4, 4]
>>> ListMedian(myList)
4

>>> myOtherList = [5, 5, 4, 'f', 5, 5]
>>> ListMedian(myOtherList)
'Not an integer list'
```

<table bgcolor="yello" border="1" cellpadding="4"><tbody><tr><td>
**Important:** To make it a little easier on you, the test cases on submit.cs will only test lists that are either all numerical (i.e. made of ints and/or floats) or either all strings. The two sample test cases already in lab04.py are illustrative of this.
</td></tr></tbody></table>

**Step 3:** Show off your work and get credit for the lab

<table bgcolor="yellow" border="1" cellpadding="4"><tbody><tr><td>
   Get your TA's attention to inspect your work, and to record your lab completion.
</td></tr></tbody></table>

<blockquote>

**Step 4:** Submit your work to submit.cs

Your final submission is the file called lab04.py, which should have started out with the start-up file I gave you (see top of this document) and now have FIVE functions that you wrote: printSortedListAscending, printSortedListDescending, checkList, ListAverage, ListMedian. **BE VERY CAREFUL ABOUT NAMING THE FUNCTIONS EXACTLY WHAT I ASK YOU TO NAME THEM AND MAKE SURE THE FILE IS CALLED lab04.py AND NOTHING ELSE!!**

Note that the start-up file has a couple of test cases and you should run those to see how well your functions work. But note that submit.cs will test *other* test cases on your functions as well.

Navigate to the <b>submit.cs</b> website, select <b>lab04</b>, register your partner, and then upload your `lab04.py` file. EDIT: You will see 80/80 points, if it passes the tests. 

You will earn the other 20 points (to make this lab worth a total of 100 points) as follows:

1) Your TA will manually have to look at your function in lab and see that it works. This is worth 10 points. If you do not finish this part of the lab during regular hours, you will not get this 10 point credit.

2) Your TA will also manually look at your submitted code on submit.cs and verify that you did the correct work AND that you have left enough comments to explain your code. This is worth another 10 points. If you use Python code or techniques that were not covered in class or are not in the textbook, you will lose these 10 points on the lab.

<hr>
<p><font size="1">
Copyright 2018, Ziad Matni, CS Dept, UC Santa Barbara. Permission to copy for non-commercial, non-profit, educational purposes granted, provided appropriate credit is given;  all other rights reserved
</font></p>
