---
layout: lab
num: lab00
ready: true
desc: "Lab00 - A Gentle Introduction"
assigned: 2018-01-23 09:00:00.00-7
due: 2018-01-24 23:59:59.00-7
---
<h2>Introduction</h2>

<p>Your first lab for this week is an introduction to programming on CSIL and in the Computer Science lab. You will write your first Python program that will print a specific text out on your computer display.</p>

 <h2>Goals for this lab</h2>
 <p>By the time you have completed this lab, you should be able to </p>
 <ul>
   <li>use the computers in Phelps 3525 (and other labs like CSIL) to do basic things</li>
   <li>perform basic management of directories and files</li>
   <li>know how to submit assignments using the &quot;submit.cs&quot; program.</li>
</ul>
<p><b>THE DEADLINE TO SUBMIT THIS LAB IS WEDNESDAY, 1/24 BY 11:59 PM</b>. Details on how to submit are further down in this document.</p>

 <p>Additionally, most of you will have a lab partner to share lab and
 some other duties during the rest of the quarter.</p>
 
 <p>This assignment is designed to make sure you are comfortable working in the 
computing environment and know how to submit your work. It is mostly about
mechanics, not concepts. As a result, this assignment is not particularly intellectually
challenging. We hope that will not be the case in future labs!</p>

 <h2>Step by Step Instructions</h2>

 <h3>Step 0: Select a lab partner</h3>
 <p>Refer to your responses to question 1 of Hw0: "What of the following things have you done before?"</p>
 <ul>
    <li><p>If you circled just "a" and/or "b" then we consider you a relative beginner, and we think that you
    should select a partner who is also a beginner like yourself.</p></li>
    
    <li><p>If you circled "c" and/or "d" then we think you should either work by yourself for this lab OR you can select a partner who is a bit more experienced, like we consider you to be.</p></li>
    
    <li><p>This lab REQUIRES you to partner up if you are a relative beginner, but does NOT require you to partner with someone if you are slightly more experienced. Other labs will REQUIRE EVERYONE to partner up, so please be aware of that. In such parner-required labs, no more than one student each lab is allowed to work without a partner, and only then if
    there is not an even number of students in the lab.</p></li>
 </ul>
 <p>Does your experience match the person with whom you are currently paired? Do you both want to
    work with each other? If the answer is no to either of those questions, then look around to find
    a different partner now.</p>
 <p>We expect a few minutes of (hopefully not chaotic) mingling while you match up, but please try
    to do it quickly. You can refer to responses to question 2, "What type of computer/system(s) do
    you have?" if that matters to you. Research also shows that lab partners are best matched by
    gender, but we leave that decision to you too.</p>
 <p>If you select a partner today, we expect you to keep that partner to work with in future labs. Please inform us if
    you make any changes later.</p>
 <p>Before proceeding to Step 1, fill in your partner's name and CoE username (if available) in response to question 4 of Hw0.'</p>

 <h3>Step 1: Verify your College of Engineering Account(s)
  <span class="smallerFont">[SHOULD BE DONE ALREADY!]</span></h3>
 <p>For Hw0 you were instructed to create (or confirm the existence of) a &quot;College of
 Engineering&quot; computer account. One of you must already be signed on (or you would not be
 reading this page right now), but we need to make sure that both of you can do that. So log out
 and let your partner log in now.</p>
 <p>If either of you have arrived at your lab session without ever logging:</p>
 <ul>
   <li>Stay logged into whichever account you are using now. If none, then a TA can log onto a
       different computer, and provide a web 
       
       owser for you to use to fill out
       the form necessary to create the account. Go to the following link to do so:
       <br><a href="https://accounts.engr.ucsb.edu/create/">https://accounts.engr.ucsb.edu/create</a>
   </li>
   <li>Once you create the account, it may take several minutes before the account is active.</li>
   <li>After waiting 5-10 minutes, try logging in.</li>
  </ul>

<h4>Notes:</h4>
 <ul>
   <li>Phelps 3525 is only available during your weekly scheduled discussion section - it
   is not open for your use at other times.</li>
   <li>At other times during the week, you can work in CSIL, the &quot;Computer Science
   Instructional Lab&quot;.
   <br><strong>Finding CSIL:</strong> CSIL is located in Harold Frank Hall (HFH).
    You enter from an outside door. To locate CSIL, find the &quot;main front entrance&quot;
    to Harold Frank Hall, on the side of the building that faces the ocean. Stand <em>outside</em>
    the double glass doors, with your <em>back</em> to the building, <em>facing the ocean</em>.
    The entrance to CSIL is now on your <em>left</em>.</li>
 </ul>
 <p>If you are making up this lab assignment outside your regularly scheduled lab time (because
    you added the course late for example), then you should go to CSIL to do it.
 </p>

<table bgcolor="lightcyan" border="1" cellpadding="4"><tbody><tr><td>
   <strong>Steps 2 through 7 below must be done once for each lab partner.</strong>
   <br>First complete these steps for whichever partner is currently logged on. After Step 7,
   you must go back and redo the steps using the other partner's account.
</td></tr></tbody></table>

<h3>Step 2: Bring up a terminal window</h3>
 <p>On the Linux systems, like the ones used in the CS Labs, there a lot of things we can do with pointing and clicking
 with the mouse, just like on Windows or Mac. But there are also many things we can only do with the command line, or can do more easily with the command line.</p>

 <p>So, one of the first steps will often be to bring up a &quot;Terminal Window&quot;, which is the Linux &quot;command line&quot;.</p>

 <p>Here's how:</p>
 <ul>
   <li>Find the Applications Menu at the top left of the screen.</li>
   <li>Select System Tools, then Terminal Window</li>
   <li>A Terminal Window should pop up.</li>
  </ul>

<h3>Step 3: Create some directories</h3>
<p>At the command prompt, we are going to type several commands to create folders
(called &quot;directories&quot;) on Linux in which you can store your programs. The
commands are shown in the box below&mdash;but first, a little explanation.</p>

<p>Each of the <strong>cd</strong> commands shown below is a command to &quot;change
directory&quot;&mdash;that is to move into a different folder on the hard drive. </p>

<ul>
<li>When you type <strong>cd</strong> by itself, it takes you to your
'home directory'.</li>
<li>cd followed by a directory name (e.g. <strong>cd cs8</strong>) moves you into
a directory under the current one</li>
</ul>

<p>Each of the <strong>mkdir</strong> commands &quot;makes a new directory&quot; (i.e. a new folder). </p>

<ul>
<li>For example,<strong> mkdir cs8</strong> creates a new directory called cs8,
inside the current directory.</li>
</ul>

<p>Each of the pwd commands &quot;prints the working directory&quot;, i.e. it tells you where you are on the hard drive.</p> 

<ul>
<li>Your home directory is something like <strong>/cs/student/jsmith</strong>
or <strong>/engr/student/mdiaz</strong></li>
<li>Under that, you might have a directory cs8&mdash;that would show up as
<strong>/cs/student/jsmith/cs8</strong>, or <strong>/engr/student/mdiaz/cs8</strong></li>
</ul>

<p>At the command prompt, type each of these commands. What you type is shown in bold.
You should get back exactly the output shown, (except that the part in italics may be different&mdash;each user will have something different show up there.)</p>

<pre>-bash-4.2$ <strong>cd</strong>
-bash-4.2$ <strong>pwd</strong>
/<em>cs</em>/<em>student</em>/<em>yourusername</em>
-bash-4.2$ <strong>mkdir cs8</strong>
-bash-4.2$ <strong>cd cs8</strong>
-bash-4.2$ <strong>pwd</strong>
/<em>cs</em>/<em>student</em>/<em>yourusername</em>/cs8
-bash-4.2$ <strong>mkdir lab00</strong>
-bash-4.2$ <strong>cd lab00</strong>
-bash-4.2$ <strong>pwd</strong>
/<em>cs</em>/<em>student</em>/<em>yourusername</em>/cs8/lab00
-bash-4.2$ <strong>cd</strong>
-bash-4.2$ <strong>pwd</strong>
/<em>cs</em>/<em>student</em>/<em>yourusername</em></pre>

<h4>Checking if it worked</h4>

<p>To see if it worked, you can use the file manager on the desktop. Drag any windows
that might be covering up the &quot;Home&quot; icon
on your desktop&mdash;it should be near the upper left hand corner of the screen.
When you double click on this icon, it will bring up your home directory. You should
see inside a folder called cs8. If you double click on that, you should see inside
of it, a folder called lab00.</p>

<p>Note that you could also use mouse clicks and menu options to create these folders,
instead of the command line. If you have trouble with the command line, then for today,
it is ok to do it that way. </p>

<p>Eventually, though, we want you to learn some of the Unix commands 
also&mdash;the reasons it is important to know both will become more clear 
as you move deeper into the study of programming and Computer Science.</p>

<h3>Step 4: Bring up the program called IDLE</h3>

<p>The preliminaries are done&mdash;now we are ready to start saving files
for Python!</p>

<p>IDLE is a piece of software that you use to interact with the Python programming
language. As we are using Python version 3 in this class, we also use IDLE version 3.
Type the following at the command prompt:</p>

<pre>-bash-4.2$ <strong>idle3</strong></pre>

<p>The window that appears should have the Python Command prompt (&gt;&gt;&gt;)
in it.</p>

<ul>
<li>This is sometimes called the &quot;Python Command Prompt&quot; window.</li>
<li>This is also called the &quot;Python Shell&quot; window.</li>
</ul>

<p>When you have the IDLE window up, you are ready for the next step.</p>

<h3>Step 5: Save a file in IDLE</h3>

<p>In IDLE, select &quot;File=&gt;New Window&quot; to open a new &quot;untitled&quot;
window for Python code.</p>

<p>When it comes up, click and drag the window by its title bar over to the right
of your Python Shell window.</p>

<p>Then, open a web browser to the link below. </p>

<ul>
<li>Hint: You may be able to use right-click (control-click on Mac), to open this link
in a new window.</li>
</ul>

<p><a href="http://www.cs.ucsb.edu/~zmatni/cs8w18/labs/lab00/hello.py">http://www.cs.ucsb.edu/~zmatni/cs8w18/labs/lab00/hello.py</a></p>

<p>Go ahead and read it and see if you can guess what it might do. Then "select all" of the text, "copy" it and "paste" it into the new &quot;untitled&quot; window.</p>

<ul>
<li>Note: if the usual keystrokes for copy and paste are not working, try the menu options under &quot;Edit&quot; for copy and paste.</li>
</ul>

<p>At the top of the file, type "Copied by: " followed by your name and, if another student is working with you today, the other student's name on the same line as yours.  Make sure you type "Copied by:" exactly as shown, including capitalization.</p>

<p>You'll have to save the file. Save the file with the name hello.py inside the cs8/lab00 folder you created in the previous step. Files with names ending in .py are typically understood to be Python programs.</p>

<h3>Step 6. Run your Python program</h3>

<p>In your IDLE window where you copied the hello.py text, pull down the menu tab that says "Run" and select "Run Module".</p>
<p>What happens?</p>

<h3>Step 7. Submit your assignment using the submit.cs program</h3>

<p>Once you are satisfied that your program is correct, then it is time to submit it.</p>

<p><strong>Please remember that in this class you must submit the program(s) to obtain any credit for the assignment; just completing the programs is not enough.</strong></p>

<p>For this example, let us assume that you only had to submit 1 program (hello.py). This applies to ANY Python program you submit via this system:</p>
<hr>

<p>In this course we will use the <a href="https://submit.cs.ucsb.edu/" target="_blank">submit.cs.ucsb.edu</a> system. You can make a submission from either the command line on any CS machine, or from a Web browser.</p>

<p>If you do not have a submit.cs account, you will first need to create one. This can be done at 
<a href="https://submit.cs.ucsb.edu/form/user" target="_blank">https://submit.cs.ucsb.edu/form/user</a>.</p>

<p>Once you have an account created, login at <a href="https://submit.cs.ucsb.edu/session" target="_blank">https://submit.cs.ucsb.edu/session</a>.</p>

<p>Next, you need to join the CS8 course. Look for the "Join Class" link at the top of the page. It is in the top bar. The class, in this system, is called: <b>CS8_w18_matni</b>. Once you see the list of all courses, click on the <b>"Join CS8_w18_matni"</b> button.</p>

<p><b>BE AWARE THAT THERE IS ANOTHER SECTION OF CS8 GOING ON THIS QUARTER AND THEY TOO ARE USING SUBMIT.CS. DO NOT SUBMIT YOUR WORK IN THE OTHER CLASS SECTION ACCOUT. MAKE SURE THAT YOU ARE SUBMITTING TO <font color="red"> CS8_w18_matni.</font></b></p>

<p>You should then see CS8 appear on your homepage when logging in to the submit.cs system. Click on the course now.</p>

<p>Now find "lab00" and click on the "Make Submission" button. It looks like this:</p>
<img src="make-submission-button.png" width="154" alt="Make Submission Button" />

<p>This is the Web interface for submitting your code for the assignment. You can now upload your source file directly on this page. The browser will open a dialog box and you will need to navigate to the directory containing your <b>hello.py</b> file and select it.</p>
 
<p>Once your file is uploaded, click "Submit 1 File":</p>
<img src="submit-file-button.png" width="129" alt="Submit 1 File Button" />

<p>Once you submit, you should see a page detailing your submission. The system will automatically grade your program and will show you the results on this page after about a 1 minute delay.</p>

<h3>Step 8: Check Submission Results</h3>

<p>After the 1 minute delay, the submit system will show your score and give you feedback on your submission. <em>Refresh the webpage after a minute to see this information.</em> This usually takes one of three forms:</p>

<p>A correct submission with a score of 100 (in the special case of Lab00, the score should be 50, since the Hw00 is worth 50 points too). This means that your program passed all the tests for this assignment. Once you get to this point, you are finished with the assignment and will receive full credit. This case will look like this (except the number under "Value" will say 50, not 100):</p>
<img src="correct-submission.png" width="233" alt="Correct Submission." />

<p>An incorrect submission with a score of 0 to 49. This means that your program failed 1 or more of the tests. For this assignment, the system will show both the expected output and the output your program generated side-by-side so that you can see what went wrong. You will need to fix your program, and then do Step 7 again to re-submit. This case will look like or similar to this (maybe slightly different wording):</p>
<img src="incorrect-submission.png" width="706" alt="Incorrect Submission." />

<p>Or a submission for which compilation failed. This means that your program caused compilation errors when the system tried to compile it. You will need to interpret the compiler output and fix the errors. The system will show you the compilation command that failed along with the full error message. This case will look like this (again, with maybe slightly different wording):</p>
<img src="compilation-failure.png" width="499" alt="Compilation Failure." />

<p>Ask your T.A. if you do not understand this crucial step.</p>

<p>You may submit your program <b>multiple times</b> before the deadline. You should really only submit after local compilation (i.e. when you run your program to check out that it works first) does not produce any errors and runs as expected - that is the most efficient and preferred way to do things. The score of the last submission uploaded before the deadline will be used as your assignment grade.</p>

<p>Once your submission receives a score of 100/100, you are done with this assignment. Congratulations on completing your first Python programs!</p>

<h3>Step 9. Log Out</h3>
<p>Actually, this is the final step of <em>every lab</em>, but we probably won't remind you again after this one.
In fact, you should do this every time you walk away from a lab computer, either in Phelps 3525 or CSIL.</p>

<p>Here's how:</p>
 <ul>
   <li>Find the System Menu at the top of the screen.</li>
   <li>Select Log Out</li>
  </ul>
 
<table bgcolor="lightcyan" border="1" cellpadding="4"><tbody><tr><td>
<strong>Second partner should now log in and redo Steps 2 through 7.</strong>
<br>The first partner should not leave though: help your partner out. Things should go much more quickly and smoothly the second time through.
</td></tr></tbody></table>

<hr>

<h2>Evaluation and Grading</h2>
<em>Each</em> student must accomplish the following to earn full credit for this lab:
 <ul>
   <li>Turn in a complete and accurate Hw0 - your TA should have collected it earlier.</li>
   <li>hello.py is complete, with "# Copied by:" and your name, and is saved in ~/cs8/lab00/.</li>
   <li>hello.py is turned in from your user account using submit.cs.
   <!--<br><b>Deadline for after-lab submission: Wednesday, 1/23, at 11:59 PM.</b>
      <br><i>Note that to be eligible for late turn-in with credit, you MUST have attended your entire lab period.</i>--></li>
 </ul>

 <p>You should try to complete this assignment by the end of the lab section.
  This first lab, however, will be accepted late without penalty from students who register for the class late, or anyone who needs extra help.</p>

<hr>
<blockquote>
<h3>After both partners finish the lab work above</h3>
<p>Normally this section of the labs will have optional challenges for you to work on after
completing the mandatory tasks. That is, if you finish the required work early, then we
want you to do additional work until the lab officially ends.</p>

<p>Are you one of the first pairs to finish? Then look around for classmates who might be
struggling, and ask them if you can help. After all of your classmates are either done or being
competently helped by someone else, then you may ask the TA to be excused. That is, today
you may leave early, but only after you are sure that nobody needs your help.</p>
</blockquote>

<hr>

<h3>If your account does not work:</h3>

<p>If you try to create a College of Engineering account, and it does not work, then send email to support@cs.ucsb.edu. In your email, </p>
<ul>
  <li>cc your instructor and your TA on the email.</li>
  <li>Indicate that you are enrolled in CS8 with Prof. Matni (remember that this quarter has two separate sections of CS8 taught by different professors).</li>
  <li> Tell approximately what day you enrolled in the class on GOLD and when you completed (or attempted) the form at
     <a href="https://accounts.engr.ucsb.edu/create/">https://accounts.engr.ucsb.edu/create/</a> </li>
  </ul>

<p>Note: DO NOT include your password in your email to support. In fact, NEVER send your
  password through email, and NEVER tell anyone else your password, not even the support
  staff. Real support staff will NEVER ASK YOU FOR YOUR PASSWORD&mdash;not over email,
  and not in person. They will not need it to help you. </p>

 <p>If someone is asking for your password over email, it is a scam called a &quot;phishing attack&quot;&mdash;don't be fooled by these dastardly villains!'</p>

<hr>
<p><font size="1">Copyright 2018, Ziad Matni, CS Dept, UC Santa Barbara. Based in part on work by Phillip Conrad. Permission to copy for non-commercial, non-profit, educational purposes granted, provided appropriate credit is given;  all other rights reserved.</font></p>
