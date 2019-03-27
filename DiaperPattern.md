# Diaper Pattern
#### SmartMirror Group


### How to recognize Diaper Pattern: 
   When you have a Try-Catch for an error, but you have no implementation of what should happen  
   when an error is caught. 

### Example: 
```python
try: 

do_something_that_might_throw_exception()
except Exception:
	pass
```
   As you can see, the exception is not handled, logged, or notifies the user of such exception.

(found from [The Diaper Pattern Stinks](https://mike.pirnat.com/2009/05/09/the-diaper-pattern-stinks/))

### Why Diaper Pattern is considered harmful:
   You would not know what is happening in the background of your program. It might range from memory leaks
   to simple errors and warnings. 

### Solution: 
   At the very least, log the exception, notify the user, or insert code that will handle the issues at 
   run-time.

 


