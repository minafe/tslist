# tslist
Thread safe list

The problem:

Suppose you need a list of element and this list is used by several threads. One thread can add elements to this list but also delete element to this list.
Suppose the first thread is using the first element of the list and the second thread decide to delete this element, what happen then ? SEGMENTETATION FAULT, for sure !!!!
I look into the web for a lib that solve this problem but I could not find anything easy to use and open source, for that reason I decided to write this library.


How does it works

This library does not allow to delete an element if this element is pointed by an iterator. If a thread is using an element with an iterator the other thread can not delete it.


Example

They are in the code.




