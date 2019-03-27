# Anemic Domain Model
## 1. What is the anti-pattern?

When a class is too simple, it can become an anemic class. This can lead to having other classes that handle the business logic for a class, which, according to [Martin Fowler](https://en.wikipedia.org/wiki/Martin_Fowler_(software_engineer)), is antithetical to the principles of Object Oriented Programming. 

According to Fowler on his [website](https://www.martinfowler.com/bliki/AnemicDomainModel.html), anemic classes are "little more than bags of getters and setters", and can be hard to spot as they often appear to be normal classes.

## 2. What is an example?
Anemic
from [Wikipedia](https://en.wikipedia.org/wiki/Anemic_domain_model)
```
class Box
{
    public int Height { get; set; }
    public int Width { get; set; }
}
```
Non-Anemic
```
class Box
{
    public int Height { get; private set; }
    public int Width { get; private set; }

    public Box(int height, int width)
    {
        if (height <= 0) {
            throw new ArgumentOutOfRangeException(nameof(height));
        }
        if (width <= 0) {
            throw new ArgumentOutOfRangeException(nameof(width));
        }
        Height = height;
        Width = width;
    }

    public int Area()
    {
       return Height * Width;
    }
}
```

## 3. How/why is it harmful?
If we are creating a class without business logic, it goes against the reasons for using the object oriented model in the first place.

## 4. How do we fix it?
By encapsulating all business logic in the class and making sure that classes don't perform the business logic of other classes. We also should take advantage of the core principles of object-oriented design by combining data and processing them together.
