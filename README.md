Download Link: https://assignmentchef.com/product/solved-cs3700-homework9-source-router-v0-using-the-dijkstras-algorithm
<br>
<strong>Part I </strong> Write a <strong>Java program</strong> to build up the forwarding table at <strong>source router V0</strong> using the Dijkstra’s algorithm.

<ul>

 <li>The routers in the network are labeled as <strong>V0</strong>, <strong>V1</strong>, <strong>V2</strong>, …, etc (for display, such labels are <strong>required</strong> to use, please do NOT use 0, 1,</li>

</ul>

2, 3, … etc. However, it is perfectly okay for you to use indices 0, 1, …, and <em>n</em> – 1 internally in your program.)

<ul>

 <li>Your routing program needs to

  <ol>

   <li>Display a prompt message to ask the user to input the total number of routers, <strong><em>n</em></strong>, in the network. Validate <strong><em>n</em></strong> to make sure that it is greater than or equal to 2.</li>

   <li>Use a topo.txt file that contains costs of all links. Each line in this file provides the cost between a pair of routers as below, where <strong>tab (‘t’)</strong> is used to separate the numbers in each line.</li>

  </ol></li>

</ul>

&lt;# of one router&gt; &lt;# of the other router&gt; &lt;link cost between these two routers&gt;

…                 …                       …            where the first and the second numbers in each row need to be validated to be between 0 and <strong><em>n</em> – <em>1</em></strong>, the third number needs to be validated to be positive.  For example, for the link (V0, V3) whose cost is 10, <strong>only</strong> <strong>ONE of the following two lines needs to be included in the topo.txt file</strong>.

0              3              10           // only <strong>ONE</strong> of this or the next line needs to be included in the topo.txt file

3              0              10           // only <strong>ONE</strong> of this or the above line needs to be included in the topo.txt file

This topo.txt file can locate in the same directory where this program runs such that a path is not needed. Display a message saying that in which row the first invalid number is detected, close the txt file, and KEEP asking for the name of the cost input file until all numbers are checked to be valid.  Record the cost information in the Cost matrix.

<ol start="3">

 <li>Implement the Dijsktra’s algorithm to build up the shortest-path tree rooted at source router V0. As the intermediate results, at the end of <strong>Initialization</strong> and each iteration of the <strong>Loop</strong>, display The set <strong>N’</strong></li>

</ol>

The set <strong>Y’ </strong>

The distance vector <strong>D</strong>, i.e., D(i) for each i between 1 and <strong><em>n –</em> 1</strong>

The predecessor vector <strong>P</strong>, i.e., p(i) for each i between 1 and <strong><em>n – </em>1</strong>

<ol start="4">

 <li>Use the shortest-path tree resulted from the Dijsktra’s algorithm to build up the forwarding table for router V0. Display the forwarding table in the following format:</li>

</ol>

Destination                           Link

V1                                          (V0, …)

V2                                          (V0, …)

…

Vn-1                                      (V0, …)

<strong>Part II : Test your programs on the Virtual Server cs3700a.msudenver.edu </strong>




<strong>Warning</strong>: to complete this part, especially when you work at home, you must first (1) <strong>connect to GlobalProtect </strong>using your NetID account (please read “<strong>how to connect to GlobalProtect …</strong>” at <a href="https://msudenver.edu/vpn/">https://msudenver.edu/vpn/</a><a href="https://msudenver.edu/vpn/">)</a>; then (2) <strong>connect to the virtual servers cs3700a </strong>using <strong><em>sftp</em></strong> and <strong><em>ssh</em></strong> command on MAC/Linux or <strong><em>PUTTY</em></strong> and <strong><em>PSFTP</em></strong> on Windows.

<table width="720">

 <tbody>

  <tr>

   <td colspan="2" width="720">ITS only supports GlobalProtect on MAC and Windows machines.  If your home computer has a different OS, it is your responsibility to figure out how to connect to cs3700a for programming assignments and submit your work by the cutoff deadline.  Such issues cannot</td>

  </tr>

  <tr>

   <td width="246">be used as an excuse to request any extension.</td>

   <td width="474"><strong> </strong></td>

  </tr>

 </tbody>

</table>




<ol>

 <li>MAKE a directory “<strong>HW9</strong>” under your home directory on <strong>cs3700a</strong>.msdenver.edu</li>

 <li>UPLOAD and COMPILE <strong><em>your program</em></strong> under “<strong>HW9</strong>” on <strong>cs3700a</strong>.msdenver.edu</li>

 <li>TEST <strong><em>your program</em></strong> running on <strong>cs3700a</strong>.msudenver.edu</li>

 <li>SAVE a file named <strong><em>txt</em></strong> under “<strong>HW9</strong>” on <strong>cs3700a</strong>.msudenver.edu, which captures the outputs of your program when you test it. You can use the following command to redirect the standard output (stdout) and the standard error (stderr) to a <strong>file</strong> on UNIX, Linux, or Mac, and view the contents of the file</li>

</ol>

<strong>java prog_name_args | tee testResultsClient.txt //copy stdout to the .txt file  //if you want, you may also use “script” command instead of the “tee” command </strong>

<strong>     //to write both stdin and stdout into testResultsClient.txt while testing your </strong>

<strong>      //client program on cs3700a.  For how to use “script”, see  </strong>

<strong> //</strong> <a href="https://www.geeksforgeeks.org/script-command-in-linux-with-examples/"><strong>https://www.geeksforgeeks.org/script</strong></a><a href="https://www.geeksforgeeks.org/script-command-in-linux-with-examples/"><strong>–</strong></a><a href="https://www.geeksforgeeks.org/script-command-in-linux-with-examples/"><strong>command</strong></a><a href="https://www.geeksforgeeks.org/script-command-in-linux-with-examples/"><strong>–</strong></a><a href="https://www.geeksforgeeks.org/script-command-in-linux-with-examples/"><strong>in</strong></a><a href="https://www.geeksforgeeks.org/script-command-in-linux-with-examples/"><strong>–</strong></a><a href="https://www.geeksforgeeks.org/script-command-in-linux-with-examples/"><strong>linux</strong></a><a href="https://www.geeksforgeeks.org/script-command-in-linux-with-examples/"><strong>–</strong></a><a href="https://www.geeksforgeeks.org/script-command-in-linux-with-examples/"><strong>with</strong></a><a href="https://www.geeksforgeeks.org/script-command-in-linux-with-examples/"><strong>–</strong></a><a href="https://www.geeksforgeeks.org/script-command-in-linux-with-examples/"><strong>examples/</strong></a> <strong> //or Google “script command in Linux” if the above link is broken. </strong>

<strong>cat file-name     //display the file’s contents.  </strong>

<strong> </strong>

<strong> </strong>