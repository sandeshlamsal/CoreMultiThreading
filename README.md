# CoreMultiThreading

thread is a process in execution.  eg:- a client using a bank account (Account Object) in a time. if by any process if we can manage
to use multiple clients using same bank ac)ame resorce) it is multi-threading

when multiple threads (clients) access the same account. eg: joint account using xyx account simultaneously(same time/sec) it will make
data inconsistency issue. to block the threads to use the same class(account) or methods(withdraw) ony by one customer, we can make the account 
class or its method to syncnronized keyword to make it synchronized.

disadvantage of synchronization is it increases waiting time of threads
and creates performance issues.


Every object has internally uses lock/wait conept to make it looks like synchronize.

if we use synchronized then lock is used.

lock,unlock is done by jvm for threads. 

but if u use synchronized it will make forceful lock to running object and it starts it exection. once the exection is done
it will release the lock. it is done by jvm.

if synchronozation is not defined in method then it can use the resource directly.

Note: while a thread executing syn method on given object the other threads not allowed to execute any syn methods symolltaneuosly on same object. but remininting threds are allowed to execute not syn method simultaneously.

eg: class x{                            //if u1 using m1, will lock object x
sync m1() //will wait                   //if u2 try using m2, then wait
sync m2() //will wait                   //if u3 comes for m3, not being sync can use directly.
m3()//wont wait
}

Lock is done on Object, not on method.

Every object has Syn and non-Syn Area. Syn are is for writing operations so only one thread can access it, but for non-sync, any no of
threads can use it.while writing program Syn area whould be always thread safer, where state of object is changing.

