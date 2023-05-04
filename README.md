Download Link: https://assignmentchef.com/product/solved-cs633-assignment-1-a-program-to-send-d-bytes-from-one-node-to-another
<br>



1.1: Write a program to send D bytes from one node to another node using

MPI_Send/Recv. Each send/recv should be done for 100 times. The experiment should be repeated 5 times on a pair of nodes (select nodes from your bucket only, see below). D = {128, 1024, 65536, 1048576, 4194304} in bytes. Use 1 process per node. Plot the effective bandwidth for each data size (one plot). MBps (y-axis) and MB (x-axis).

<em>Pseudocode:</em>

<em>For d in D {    Repeat 100 times </em>

<em>     send and recv </em>

<em>} </em>

<em> </em>

(40 marks)




1.2: Write a program to send D bytes from (P-1) senders to 1 receiver (choose rank 0 as the receiver rank). Compare blocking and non-blocking sends and receives. D = {1024, 65536, 1048576} in bytes. Total #processes P = {8, 16, 32}, use 4 processes per node, i.e. #nodes = {2, 4, 8}. Sends/recvs should be repeated for 100 times. Repeat runs for each data point 5 times. Plot the effective bandwidth for each D for blocking and nonblocking for all process counts in the same graph (6 plots). MBps (y-axis) and MB (xaxis).

<em> </em>

<em>Pseudocode:</em>

<em>For all process counts  </em>

<em>  For d in D {</em>

<em>     Repeat 100 times </em>

<em>        Isend/send and Irecv/recv </em>

<em>  }</em>

(40 marks)

<u>General execution instructions</u>




Node buckets: use the following node conventions.

<ul>

 <li>CSE login names starting with A – B: 27.19.1 – 13</li>

 <li>CSE login names starting with C – L: 27.19.14 – 26</li>

 <li>CSE login names starting with M – R: 172.27.19.27 – 39 (barring node 36)</li>

 <li>CSE login names starting with S – Z: 27.19.40 – 54</li>

</ul>

Suggestion: Its preferable to have a script which generates machinefile/hostfile on-thefly based on the node status so that your jobs never fail.

<u>General submission instructions</u>




Each submission subfolder (named 1.1, 1.2) should necessarily contain the source code (‘src.c’), ‘Makefile’, ‘readme’, job script (‘run.py’ or ‘run.sh’), plot script and plots. You should measure the total time taken by your main algorithm. The job script should run all the configurations, i.e. I should be able to run the job script to execute your code (all configurations). The job script must generate data* files, which must be input to your plot script. Optionally, you may automate plot generation. Your plot should be named

‘plot.jpg’. The readme should contain your observations regarding performance/speedup and any issues that you might have faced. You may have other auxiliary files, if required.


