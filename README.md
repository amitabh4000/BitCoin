# BitCoin

Group Members:

1. Dinesh Kumar Sundararajan (UFID: 61314525)
2. Amitabh Suman (UFID: 25834884)


Files Attached:

The following files can be found inside the project1 folder.

1. project1.scala can be found in /project1/src/main/scala/
2. Application.conf file can be found in /project1/src/main/resources/
3. build.sbt can found in /project1 


Program Logic:

Input is obtained from the user. If the input is given is the number of zeros, then the local workers are called and bit coins are found. If the input given is the IP address of the master, then it serves as a remote worker and communicates with the master and performs the operation.  

The Master Actor mainly creates the worker actors and allocates work. The work unit size given is 1000000. The time for which the program is to be run is given, say 100 seconds. The bit coin computation is performed by the workers till this time is reached and then the bit coins found (based on zeros) , are displayed. In case the IP address is given as the input, remote workers are called, which communicates with the server to obtain work. After computing the bit coins, the data is sent back to the master, which displays the result. The process is stopped once the time limit is reached.


Work Unit Size:

Work Unit Size = 1000000

The reason for choosing this value as the work unit size is that the program takes an optimal time for this size. This value was chosen after a series of trial and error operations. We observed that for lesser values of work unit size, the number of inputs processed gets reduced as a result of the interactions between the worker and the server. Also, when the value is increased beyond this, it creates an overhead for the worker. Hence, the optimal work unit size of 1000000 was chosen.


Largest No. of working machines:

The largest number of working machines (laptops) that were connected is 2. One machine serves as the master and one serves as the remote worker. Also, it can be observed based on the results that 12 worker actors can operate at a time.






