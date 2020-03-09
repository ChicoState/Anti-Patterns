# Diaper Pattern
#### SmartMirror Group and ParkCore Group


### How to recognize Diaper Pattern:
   When you have a Try-Catch that is meant to handle an error, but you have no
   implementation of what should happen when the error is actually caught. Also
   known as Error Hiding.

### Example:
```python
try:
  do_something_that_might_throw_exception()
except Exception:
	pass
```
   As you can see, the exception is not handled or logged, and the user is in
   no way notified of the error or exception.

(found from [The Diaper Pattern Stinks](https://mike.pirnat.com/2009/05/09/the-diaper-pattern-stinks/))
(found from [Wikipedia](https://en.wikipedia.org/wiki/Error_hiding))

### Why Diaper Pattern is considered harmful:
   If you have specific exceptions that need handling, you should be taking care
   of them. Otherwise, you would not know what is happening in the background of
   your program. It might range from memory leaks to simple errors and warnings.

### Solution:
   At the very least, log the exception, notify the user, or insert code that
   will handle the issues at run-time.
