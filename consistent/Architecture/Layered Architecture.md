**What is Layer ?**

1.  Independent Isolated portion of the System which behaves as an external entity in the System. 
2.  Can be a single file, set of modules or set of packages that have single purpose (or) functionality.
3.  Interacts with rest of the system through well defined API (Rest, Messaging, or Abstract Interface).
4.  It will expose it's functionality through abstract API.
5.  Layers will have sub components (High Module and helping Low Level Modules).
 ![[Pasted image 20230225153848.png

How to make sure we have clear Layers :
1.  Well organised code with proper coding paradigms and design patterns.
2.  Layers are independent from each other.
3.  Each Layer responds to the layer above(Closed Layers).
4.  Open Layers allows request to bypass them.

