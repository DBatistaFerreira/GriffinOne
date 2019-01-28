# GriffinOne

## Q1
The main requirement is not met because the depositor and withdrawer (two seperate threads) are accessing the same memory at the same time. The atomicity problem is the that the two thread operations are overlapping which is thread interference. The bug is that the object is not synchronized, thus when depositing and withdrawing money both threads see different values for the current balance so they write back an incorrect balance when they are done with their operation. 

## Q2
The threads are started sequentially in the AccountManager class with the start() method. They are created sequentially but their execution order is determined by the scheduler, and the threads end when their tasks are done. The consistency is not preserved because they are accessing the same memory, the main problem is not the start or end of the thread but the run time of the thread and how it accesses the main memory. 

## Q5
The synchronized block only locks the code in the block, thus the threads will be synchronized while executing the block statements, but the synchronzied method will lock the entire method so each thread must wait to use that entire method. This leads to the synchronized block running much faster than the synchronized method





