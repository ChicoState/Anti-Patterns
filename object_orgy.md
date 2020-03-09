# Software Engineering Anti-Patterns. Smart Clock is doing Object Orgy

* How to recognize your anti-pattern
  * This anti-pattern is an insufficent object encaputlation and internals of the object are exposed, allowing unstrestricted access to the data member variables.
    The way we can see this in code is that the internals of the object are exposed via getters and setters, passing the internal data as arguments to functions in other classes.



* Antidote
  * Some object orgies will require a recoding of the the way the object interacts with the whole system; however, the most straight
    forward solution is encapsulation, bundling the data with methods that operate on it within the object(i.e. getters and setters).

* Why the anti-pattern is considered harmful
  * Object orgy may be considered a harmful anti-pattern due to loss of benefits of containing data within a class which is caused by not giving the correct permissions of access for certain members within the class. Allowing for data to be accessed 
    and possibly updated by multiple members due to no construct given for read-only access. All of which are possible by coding
    to an immature design or when a program is driven by laziness or rushed development.

* Example
  * An Example Of The Anti-Pattern:
    by declaring a friend function within class

'''
class Temperature
{
  int cel;
  pubilc:
  Temperature(){
  cel = 0;
  }
  friend int temp(Temperature)
}
```
    this could cause problems, and could weaken the encapsulation

 (found from [Wikipedia](https://en.wikipedia.org/wiki/Object_orgy))
 
 (found from [Wikibooks](https://en.wikibooks.org/wiki/Introduction_to_Software_Engineering/Architecture/Anti-Patterns))
 
 (found from [CodesDope](https://www.codesdope.com/cpp-friend-class-and-function/))
 
