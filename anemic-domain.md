# Anemic Domain Model

When a class is too simple, it can become an anemic class. This can lead to having other classes that handle the business logic for a class, which, according to [Martin Fowler](https://en.wikipedia.org/wiki/Martin_Fowler_(software_engineer)), is antithetical to the principles of Object Oriented Programming. 

According to Fowler on his [website](https://www.martinfowler.com/bliki/AnemicDomainModel.html), anemic classes are "little more than bags of getters and setters", and can be hard to spot as they often appear to be normal classes.

## Example 
from [Wikipedia](https://en.wikipedia.org/wiki/Anemic_domain_model)
```
class Box
{
    public int Height { get; set; }
    public int Width { get; set; }
}
```