(found from [Wikipedia](https://en.wikipedia.org/wiki/Busy_waiting))

How to recognize your anti-pattern:
You can identify busy waiting by monitoring efficiency. If the program underutilizes its time it is most likely busy-waiting, busy-looping or spinning.
This is a lowlevel issue that primarily effects operating systems and is an issue that accumulates.

An example of the anti-pattern:
If the program is waiting for input (either exterior or internal) and stalling or if it is purposely stalling as a time delay technique.

Why the anti-pattern is considered harmful:
It is an expensive approach because it wastes computational time. The time used stalling could be used to compute other things.

What is a recommended antidote to the anti-pattern:
Write better software that either avoids busy waiting or shares the resources so other work can be done concurrently.
Busy waiting can be mitigated by using a variety of system calls that will block the process on an event, such as lock acquisition, timer changes, I/O availability or signals.
Small improvements can be made by using sleep or delay functions as well.

# Example by code:

This is a perfect example of bad code that stalls a program an severly prohibits run time. Here is what is considered a Bad Sleep. We are incrementing a counter until we reach a big number to stall the program.

```c++
int counter = 0;
while(counter <= INT_MAX){
    counter++;
}
```
