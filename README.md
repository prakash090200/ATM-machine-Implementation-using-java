# ATM-machine-Implementation-using-java

 Its about how the ATM machine works when it need to manage multiple withdraw task at the same time . If the user have an account in the database then they can put  a request of withdraw amount else they need to create their account in that database First.
 Suppose 1000-2000 people all over India want to withdraw some amount from their  account which has huge amount but not enough for all those 1000-2000 people currently accessing the server . So, Here comes the concept of Thread (single  and multiple) in java.
 Its obvious that the processor will not going to handle each user seperately because this may leads to wastage of time i.e the 1000th user accessing the server at the same time have to wait in the queue till 999th user complete his/her transaction.Thats why thread concept is implemented in the code where all 1000th user request will be arranged in a circular queue and all request will be processed bit by bit whenever it get its turn in circular queue this way all request will be handled at the same time .But still there is a problem that if all the user are accessing the atm at the same time then the amount may be vanished before the 1000th user request is completely processed. here comes the concept of multi-thread  i.e **if 2 or more threads(multi-thread) try to access the common resource(atm)  at the same time then their is a chance of data corruption**.
So, their is a need to  synchronized  multiple thread in such a way that unless a thread complete its transaction completely other thread don't get the chance to access the server .Thisway we can save the database from getting corrupt and save the time also.Java provides locking, which ensures mutually exclusive access to the shared resource and prevents data race.
*synchronized- in a series manner , 
asynchronized means - parallelly handling*.

---
## Concept Used:

 * Object Oriented Programming in java.
 * Threads in java
 * Data Structure
     * Double Linked list
 * Exception handling
 * Interface in java
 ---
 ## Screenshots
 ![multi-thread](https://user-images.githubusercontent.com/59432256/80273749-93e9c480-86f2-11ea-9b61-a1352b30f4be.png)

 This a non- synchronized multi-thread implementation where 3 user inputs are given if the user login credentials matches with the database they were allowed to forward transaction request to the server else invalid user.
 for each user a thread is created and attached to his code . 
 
 
 
 <img width="943" alt="synchronized multi-thread" src="https://user-images.githubusercontent.com/59432256/80273558-bbd82880-86f0-11ea-94fe-73e9cb49f848.PNG">




