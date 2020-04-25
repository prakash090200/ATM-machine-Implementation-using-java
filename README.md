# ATM-machine-Implementation-using-java :octocat: 

 Its about how the ATM machine works when it need to manage multiple withdraw task at the same time . If the user have an account in the database then they can put  a request of withdraw amount else they need to create their account in that database First.
 Suppose 1000-2000 people all over India want to withdraw some amount from their  account which has huge amount but not enough for all those 1000-2000 people currently accessing the server . So, Here comes the concept of Thread (single  and multiple) in java.
 Its obvious that the processor will not going to handle each user seperately because this may leads to wastage of time i.e the 1000th user accessing the server at the same time have to wait in the queue till 999th user complete his/her transaction.Thats why thread concept is implemented in the code where all 1000th user request will be arranged in a circular queue and all request will be processed bit by bit whenever it get its turn in circular queue this way all request will be handled at the same time .But still there is a problem that if all the user are accessing the atm at the same time then the amount may be vanished before the 1000th user request is completely processed. here comes the concept of multi-thread  i.e **if 2 or more threads(multi-thread) try to access the common resource(atm)  at the same time then their is a chance of data corruption**.
So, their is a need to  synchronized  multiple thread in such a way that unless a thread complete its transaction completely other thread don't get the chance to access the server .Thisway we can save the database from getting corrupt and save the time also.Java provides locking, which ensures mutually exclusive access to the shared resource and prevents data race.
*synchronized- in a series manner , 
asynchronized means - parallelly handling*.

---
## Concept Used:

 * Object Oriented Programming in java.<br/>
 * Threads in java <br/>
 * Data Structure <br/>
      * Double Linked list <br/>
 * Exception handling <br/>
 * Interface in java <br/>

 ---
 ## Screenshots :movie_camera: :film_strip:
 
 ### asynchronized multi-thread :camera:
<img width="944" alt="asynchronized multi-thread" src="https://user-images.githubusercontent.com/59432256/80273990-cbf20700-86f4-11ea-9955-4e31b8085810.PNG">


This is asynchronized multi-thread implementation where 3 user inputs are given if the user login credentials matches with the database they were allowed to forward transaction request to the server else invalid user.
 For each user a thread is created and attached to the code , now when they try to withdraw amount from atm ( atm has only Rs 5000 left)
 both request will be processed together at the same time in a circular queue both the threads making use of same resource as a result the data got corrupted.
 
 ### synchronized multi-thread :camera:
 <img width="943" alt="synchronized multi-thread" src="https://user-images.githubusercontent.com/59432256/80273558-bbd82880-86f0-11ea-94fe-73e9cb49f848.PNG">
 
 Here we made it synchronized now 1st thread was processed completely then next thread is processed , this way data is secured.
 
# Working 

* First create the thread object for thread class <br/>
* join the thread with the source code either by - <br/>
      *  Implementing the interface Runnable( import java.lang.Runnable). <br/>
      *  Extending the Thread Class Itself(import java.lang.thread). <br/>
* Start each thread corresponding to each customer. <br/>
* For synchronized multi- thread use- <br/>

---
     Synchronized(resource object name){ 
             public void run(){ 
             // code 
             } 
          }
---       
* All database is maintained and structures using Double linked list which is the child class of list ( inturn is a child class of collection interaface)
# Contact

:computer: https://www.linkedin.com/in/prakash-kumar-384409177/

:telephone_receiver: 6379215481

<center><a href="https://imgflip.com/gif/3l3m92"><img src="https://i.imgflip.com/3l3m92.gif" title="made at imgflip.com"/></a></center>

Hover on picture  :v: 

