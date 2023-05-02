Download Link: https://assignmentchef.com/product/solved-comp2710-project2-while-and-do-while-statements
<br>
<ul>

 <li>To learn “while” and “do-while” statements</li>

 <li>To learn how to define functions</li>

 <li>To write a test driver</li>

 <li>To learn how to use assert()</li>

 <li>To use random numbers</li>

</ul>




<strong><em><u>Description:</u> </em></strong>

In the land of Puzzlevania, Aaron, Bob, and Charlie had an argument over which one of them was the greatest puzzle-solver of all time.  To end the argument once and for all, they agreed on a duel to the death (this makes sense?). Aaron was a poor shooter and only hit this target with a probability of 1/3. Bob was a bit better and hit his target with a probability of 1/2. Charlie was an expert marksman and never missed. A hit means a kill and the person hit drops out of the duel.

To compensate for the inequities in their marksmanship skills, the three decided that they would fire in turns, starting with Aaron, followed by Bob, and then by Charlie. The cycle would repeat until there was one man standing. That man would be remembered for all time as the Greatest Puzzle-Solver of All Time.

<strong>Strategy 1:</strong>  An obvious and reasonable strategy is for each man to shoot at the most accurate shooter still alive, on the grounds that this shooter is the deadliest and has the best chance of hitting back.

Write a program to simulate the duel using this strategy. Your program should use random numbers and the probabilities given in the problem to determine whether a shooter hits his target. You will likely want to create multiple functions to complete the problem. My solution had only one function to simulate the duels and it passed in the odds and the three guys as pass-by-reference parameters.  Once you can simulate a duel, add a loop to your program that simulates 10,000 duels. Count the number of times that each contestant wins and print the probability of winning for each contestant (e.g., for Aaron your might output “Aaron won 3612/10000 duels or 36.12%).




<strong>Strategy 2:</strong> An alternative strategy for Aaron is to intentionally miss on his first shot, while the rest of duel is as same as that in <strong>Strategy 1</strong>. Write a function to simulate Strategy 2. Your program will determine which strategy is better for Aaron.







<strong>Note: </strong>You must provide the following user interface. Probabilities might be slightly different for different runs due to the random number, but strategy 2 should be always better than strategy 1. You do not need to display text in red. Please replace “Li” with your name.

<table width="591">

 <tbody>

  <tr>

   <td width="591">*** Welcome to Li’s Duel Simulator ***Unit Testing 1: Function – at_least_two_alive()                  Case 1: Aaron alive, Bob alive, Charlie alive                  Case passed …Case 2: Aaron dead, Bob alive, Charlie alive                  Case passed …Case 3: Aaron alive, Bob dead, Charlie alive                  Case passed …Case 4: Aaron alive, Bob alive, Charlie dead                  Case passed …Case 5: Aaron dead, Bob dead, Charlie alive                  Case passed …Case 6: Aaron dead, Bob alive, Charlie dead                  Case passed …Case 7: Aaron alive, Bob dead, Charlie dead                  Case passed …Case 8: Aaron dead, Bob dead, Charlie dead                  Case passed …Press any key to continue… Unit Testing 2: Function Aaron_shoots1(Bob_alive, Charlie_alive)Case 1: Bob alive, Charlie aliveAaron is shooting at CharlieCase 2: Bob dead, Charlie aliveAaron is shooting at CharlieCase 3: Bob alive, Charlie dead                       Aaron is shooting at BobPress any key to continue… Unit Testing 3: Function Bob_shoots(Aaron_alive, Charlie_alive)Case 1: Aaron alive, Charlie aliveBob is shooting at CharlieCase 2: Aaron dead, Charlie aliveBob is shooting at CharlieCase 3: Aaron alive, Charlie dead                                  Bob is shooting at AaronPress any key to continue… Unit Testing 4: Function Charlie_shoots(Aaron_alive, Bob_alive)Case 1: Aaron alive, Bob aliveCharlie is shooting at BobCase 2: Aaron dead, Bob aliveCharlie is shooting at BobCase 3: Aaron alive, Bob deadCharlie is shooting at Aaron</td>

  </tr>

  <tr>

   <td width="591">Press any key to continue… Unit Testing 5: Function Aaron_shoots2(Bob_alive, Charlie_alive)Case 1: Bob alive, Charlie aliveAaron intentionally misses his first shot                      Both Bob and Charlie are alive.Case 2: Bob dead, Charlie aliveAaron is shooting at CharlieCase 3: Bob alive, Charlie dead                       Aaron is shooting at BobPress any key to continue… Ready to test strategy 1 (run 10000 times): Press any key to continue… Aaron won 3593/10000 duels or 35.9%Bob won 4169/10000 duels or 41.69%Charlie won 2238/10000 duels or 22.38% Ready to test strategy 2 (run 10000 times): Press any key to continue… Aaron won 4131/10000 duels or 41.31%Bob won 2594/10000 duels or 25.94%Charlie won 3275/10000 duels or 32.75% Strategy 2 is better than strategy 1.</td>

  </tr>

 </tbody>

</table>

<strong> </strong>

<strong><em><u>Requirements:</u> </em></strong>




<ol>

 <li>You must follow the above user interface to implement your program.</li>

</ol>




<ol start="2">

 <li>You must implement the following functions:</li>

</ol>




<ul>

 <li>bool <strong>at_least_two_alive</strong>(bool A_alive, bool B_alive, C_alive)</li>

</ul>

/* Input: A_alive indicates whether Aaron is alive */

/*        B_alive indicates whether Bob is alive */

/*        C_alive indicates whether Charlie is alive */

/* Return: true if at least two are alive */

/*         otherwise return false */




<ul>

 <li>void <strong>Aaron_shoots1</strong>(bool&amp; B_alive, bool&amp; C_alive)</li>

</ul>

/* Strategy 1: Use call by reference

<ul>

 <li>Input: B_alive indicates whether Bob alive or dead</li>

 <li>C_alive indicates whether Charlie is alive or dead</li>

 <li>Return: Change B_alive into false if Bob is killed.</li>

 <li>Change C_alive into false if Charlie is killed.</li>

</ul>

*/







<ul>

 <li>void <strong>Bob_shoots</strong>(bool&amp; A_alive, bool&amp; C_alive)</li>

</ul>

/* Call by reference

<ul>

 <li>Input: A_alive indicates if Aaron is alive or dead</li>

 <li>C_alive indicates whether Charlie is alive or dead</li>

 <li>Return: Change A_alive into false if Aaron is killed.</li>

 <li>Change C_alive into false if Charlie is killed.</li>

</ul>

*/




<ul>

 <li>void <strong>Charlie_shoots</strong>(bool&amp; A_alive, bool&amp; B_alive)</li>

</ul>

/* Call by reference

<ul>

 <li>Input: A_alive indicates if Aaron is alive or dead *        B_alive indicates whether Bob is alive or dead</li>

 <li>Return: Change A_alive into false if Aaron is killed.</li>

 <li>Change B_alive into false if Bob is killed.</li>

</ul>

*/




<ul>

 <li>void <strong>Aaron_shoots2</strong>(bool&amp; B_alive, bool&amp; C_alive)</li>

</ul>

/* Strategy 2: Use call by reference

<ul>

 <li>Input: B_alive indicates whether Bob alive or dead</li>

 <li>C_alive indicates whether Charlie is alive or dead</li>

 <li>Return: Change B_alive into false if Bob is killed.</li>

 <li>Change C_alive into false if Charlie is killed. */</li>

</ul>




<ol start="2">

 <li>You must implement five unit-test drivers (five functions) to test the above five functions (see the example output on pages 2 and 3).</li>

</ol>




<ol start="3">

 <li>You must use <strong>assert</strong> in your test driver.</li>

</ol>




<ol start="4">

 <li>You must define at least three constants in your implementation. For example, the total number of runs (i.e., 10,000) can be defined as a constant.</li>

</ol>




<strong><em><u>Hints:</u> </em></strong>

<ol>

 <li>How to implement “Press any Enter to continue…”</li>

</ol>




cout &lt;&lt; “Press Enter to continue…”;

cin.ignore().get(); //Pause Command for Linux Terminal




<strong>Note:</strong> you can implement the above two lines as a function to be repeatedly called by other functions in your program.




<ol start="2">

 <li>You may need to use the following libraries.</li>

</ol>

# include &lt;iostream&gt;

# include &lt;stdlib.h&gt;

# include &lt;assert.h&gt;

# include &lt;ctime&gt;




<ol start="3">

 <li>Initialize your random number generator as below:      srand(time(0));</li>

</ol>




<ol start="4">

 <li>A sample code of generating a random number is given below:</li>

</ol>




/* Assume that the probabilty of hit a target is 25 percent */ int shoot_target_result;




shoot_target_result = rand()%100;




if (shoot_target_result &lt; 25) {      cout&lt;&lt;“Hit the target
”;




/* add more code here */

}




<ol start="5">

 <li>Please follow the following sample test driver to implement the test driver.</li>

</ol>




void test_at_least_two_alive(void) {

cout &lt;&lt; “Unit Testing 1: Function – at_least_two_alive()
”;




cout &lt;&lt; “Case 1: Aaron alive, Bob alive, Charlie alive
”;        assert(true == at_least_two_alive(true, true, true));

cout &lt;&lt; “Case passed …
”;

cout &lt;&lt; “Case 2: Aaron dead, Bob alive, Charlie alive
”;  assert(true == at_least_two_alive(false, true, true));

cout &lt;&lt; “Case passed …
”;

cout &lt;&lt; “Case 3: Aaron alive, Bob dead, Charlie alive
”;  assert(true == at_least_two_alive(true, false, true));

cout &lt;&lt; “Case passed …
”;




/* add test cases 4-6 below */

…

}

<ol start="6">

 <li>If your strategy 1 is better than your strategy 2, then please check your source code. In this case, it is likely that you have incorrectly implemented strategy 2. Please ensure that strategy 2 is better than strategy 1.</li>

</ol>




<ol start="7">

 <li>The framework of the source code is given below:</li>

</ol>




<table width="578">

 <tbody>

  <tr>

   <td width="578"># include &lt;iostream&gt;# include &lt;stdlib.h&gt;# include &lt;assert.h&gt; # include &lt;ctime&gt; using namespace std; //prototypesbool at_least_two_alive(bool A_alive, bool B_alive, bool C_alive);/* Input: A_alive indicates whether Aaron is alive *//*        B_alive indicates whether Bob is alive *//*        C_alive indicates whether Charlie is alive */</td>

  </tr>

  <tr>

   <td width="578"> /* Return: true if at least two are alive *//*         otherwise return false */ /**  Add other function prototypes below*/void test_at_least_two_alive(void);/* This is a test driver for at_least_two_alive() */ /**  Add more prototypes for other test drivers below*/int main(){/**  This is the main function*  …*/} /* Implementation of at_least_two_alive() */bool at_least_two_alive(bool A_alive, bool B_alive, bool C_alive) {/* add the implementation below */} /* Implementation of the test driver for at_least_two_alive() */ void test_at_least_two_alive(void) {cout &lt;&lt; “Unit Testing 1: Function – at_least_two_alive()
”; cout &lt;&lt; “Case 1: Aaron alive, Bob alive, Charlie alive
”;     assert(true == at_least_two_alive(true, true, true));     cout &lt;&lt; “Case passed …
”; cout &lt;&lt; “Case 2: Aaron dead, Bob alive, Charlie alive
”;     assert(true == at_least_two_alive(false, true, true));     cout &lt;&lt; “Case passed …
”; /* add test cases 4-6 below */ } </td>

  </tr>

 </tbody>

</table>










<strong><em><u>Programming Environment:</u> </em></strong>

Write a program in C++.  Compile and run it using AU server (no matter what kind of text editor you use, please make sure your code could run on AU server, the only test bed we accept is the AU server).