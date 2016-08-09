# CoreMultiThreading

thread is a process in execution.  eg:- a client using a bank account (Account Object) in a time. if by any process if we can manage
to use multiple clients using same bank ac)ame resorce) it is multi-threading

when multiple threads (clients) access the same account. eg: joint account using xyx account simultaneously(same time/sec) it will make
data inconsistency issue. to block the threads to use the same class(account) or methods(withdraw) ony by one customer, we can make the account 
class or its method to syncnronized keyword to make it synchronized.

disadvantage of synchronization is it increases waiting time of threads
and creates performance issues.
