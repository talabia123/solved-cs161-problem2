Download Link: https://assignmentchef.com/product/solved-cs161-problem2
<br>



<ol>

 <li><strong> </strong>In your pre-lecture Exercise for Lecture 3, you saw two different proofs that the solution to the recurrence relation <em>T</em>(<em>n</em>) = 2 · <em>T</em>(<em>n/</em>2) + <em>n </em>with <em>T</em>(1) = 1, was exactly <em>T</em>(<em>n</em>) = <em>n</em>(1 + log(<em>n</em>)), when <em>n </em>was a power of two.

  <ul>

   <li>What is the exact solution to <em>T</em>(<em>n</em>) = 2 · <em>T</em>(<em>n/</em>2) + <em>n </em>with <em>T</em>(1) = 2, when <em>n </em>is a power of 2?</li>

   <li>What is the exact solution to <em>T</em>(<em>n</em>) = 2 · <em>T</em>(<em>n/</em>2) + 2<em>n </em>with <em>T</em>(1) = 1, when <em>n </em>is a power of 2?</li>

  </ul></li>

</ol>

<strong>[We are expecting:               Your answer, with a convincing argument (it does not need to be a formal proof). Notice that we want the exact answer, so don’t give a </strong><em>O</em>() <strong>statement. ]</strong>

<ol start="2">

 <li>Consider the recurrence relation <em>T</em>(<em>n</em>) = <em>T</em>(<em>n </em>− 1) + <em>n </em>with <em>T</em>(1) = 1. Your friend claims that <em>T</em>(<em>n</em>) = <em>O</em>(<em>n</em>), and offers the following justification:</li>

</ol>

Let’s use the Master Theorem with, and <em>d </em>= 1. This applies since

Then we have <em>a &lt; b<sup>d</sup></em>, so the Master Theorem says that <em>T</em>(<em>n</em>) = <em>O</em>(<em>n<sup>d</sup></em>) = <em>O</em>(<em>n</em>)<em>.</em>

What’s wrong with your friend’s argument, and what is the correct answer?

<strong>[HINT: It is totally fine to apply the Master Theorem when </strong><em>b </em><strong>is a fraction; that’s not the problem.]</strong>

<strong>[We are expecting: A clear identification of the faulty logic above; your solution to this recurrence (you may use asymptotic notation</strong><a href="#_ftn1" name="_ftnref1"><sup>[1]</sup></a><strong>) and a short but convincing justification.]</strong>

<ol start="3">

 <li><strong>(3 pt.) </strong>Use any of the methods we’ve seen in class so far to solve the following recurrence relations.<a href="#_ftn2" name="_ftnref2"><sup>[2]</sup></a>

  <ul>

   <li><em>T</em>(<em>n</em>) = <em>T</em>(<em>n/</em>3) + <em>n</em><sup>2</sup><em>, </em>for <em>n &gt; </em>3, and <em>T</em>(<em>n</em>) = 1 for <em>n </em>≤ 3.</li>

   <li><em>T</em>(<em>n</em>) = 2<em>T</em>(<em>n/</em>2) + 10 · <em>n </em>+ 4, for <em>n &gt; </em>2, and <em>T</em>(<em>n</em>) = 1 for <em>n </em>≤ 2.</li>

   <li><em>T</em>(<em>n</em>) = <em>T</em>(<em>n/</em>2) + <em>T</em>(<em>n/</em>4) + <em>n </em>for <em>n &gt; </em>4, and <em>T</em>(<em>n</em>) = 1 for <em>n </em>≤ 4.</li>

  </ul></li>

</ol>

<strong>[We are expecting: The answer (you may use asymptotic notation) and a justification. You do not need to give a formal proof, but your justification should be convincing to the grader.]</strong>

<h1>Problems</h1>

You may talk with your fellow CS161-ers about the problems. However:

<ul>

 <li>Try the problems on your own <em>before </em></li>

 <li>Write up your answers yourself, in your own words. You should never share your typed-up solutions with your collaborators.</li>

 <li>If you collaborated, list the names of the students you collaborated with at the beginning of each problem.</li>

</ul>

<ol>

 <li><strong> </strong>Consider the function <em>T</em>(<em>n</em>) defined recursively by</li>

</ol>

Fill in the blank: <em>T</em>(<em>n</em>) = Θ(                   ). <strong>[HINT: It may be helpful that</strong>

<strong>[We are expecting: Your answer and a convincing justification. You do not need to write a formal proof; and you may assume that </strong><em>n </em><strong>is a power of </strong>2 <strong>if it helps.]</strong>

<ol start="2">

 <li><strong> </strong>Consider the function <em>T</em>(<em>n</em>) defined by</li>

</ol>

Using an argument <strong>by induction </strong>(not using the Master Method), prove that <em>T</em>(<em>n</em>) = Ω(<em>n</em>log(<em>n</em>)).

<strong>[We are expecting: A formal proof by induction. Make sure you explicitly state your inductive hypothesis, base case, inductive step, and conclusion. ]</strong>

<ol start="3">

 <li><strong>(8 pt.) </strong>Plucky the Pedantic Penguin sometimes does consulting work on the side.<a href="#_ftn3" name="_ftnref3"><sup>[3]</sup></a> There are <em>n </em>companies who are interested in Plucky’s work. Plucky can work for at most one company during a given day. Each company has a range of times when they are interested in Plucky’s work, and an amount they are willing to pay: between <em>a<sub>i </sub></em>and <em>b<sub>i </sub></em>(including <em>a<sub>i </sub></em>and not including <em>b<sub>i</sub></em>), Company <em>i </em>is willing to pay Plucky <em>f<sub>i </sub></em> Here, <em>a<sub>i</sub>,b<sub>i</sub>,f<sub>i </sub></em>are all positive integers and <em>a<sub>i </sub></em>≤ <em>b<sub>i</sub></em>. Each day, Plucky chooses to work for the highest bidder. If there is no company interested in Plucky’s work on a day, Plucky gets zero fish that day.</li>

</ol>

Plucky gets the bids (<em>a<sub>i</sub>,b<sub>i</sub>,f<sub>i</sub></em>) as inputs, and wants to make a plot of how many fish he will receive each day. To understand the format he wants the output in, see the example below.

In this problem you’ll design an algorithm for Plucky. Your algorithm should take as input a list of <em>n </em>bids (<em>a<sub>i</sub>,b<sub>i</sub>,f<sub>i</sub></em>), one for each company <em>i </em>∈ {0<em>,…,n </em>− 1}, and return a list fishPlot of (<em>t<sub>i</sub>,f<sub>i</sub></em>) pairs as described in the example above.

<ul>

 <li><strong> </strong>Describe a simple <em>O</em>(<em>n</em><sup>2</sup>)-time algorithm for Plucky.</li>

</ul>

<strong>[We are expecting: Pseudocode, and a short English description explaining the main idea of the algorithm. No justification of the correctness or running time is required.]</strong>

<ul>

 <li>Design a divide-and-conquer algorithm that takes time <em>O</em>(<em>n</em>log(<em>n</em>)).</li>

</ul>

<strong>[We are expecting: Pseudocode, and a short English description explaining the main idea of the algorithm. We are also expecting an informal justification of correctness and of the running time.]</strong>

<a href="#_ftnref1" name="_ftn1">[1]</a> Unless specified otherwise, in every problem set, when we ask for an answer in asymptotic notation, we are asking either for a Θ(·) result, or else the tightest <em>O</em>(·) result you can come up with.

<a href="#_ftnref2" name="_ftn2">[2]</a> You may either treat fractions like <em>n/</em>2 as b<em>n/</em>2c, d<em>n/</em>2e, or just as real numbers (not integers), whichever you prefer.

<a href="#_ftnref3" name="_ftn3">[3]</a> He points out indexing errors for bay area start-ups.