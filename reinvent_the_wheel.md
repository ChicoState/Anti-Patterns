# Reinvent the Wheel

### This is an example of reinventing the wheel

```cpp
void add(int a, int b, int &product) {
    product = 0;
    for(int i = 0; i < abs(a); i++) {
        if(a < 0) {
            product--;
        } else if(a > 0) {
            product++;
        }  
    }
    for(int i = 0; i < abs(b); i++) {
        if(b < 0) {
            product--;
        } else if(b > 0) {
            product++;
        }   
    }
}

add(a, b, c);
```

### This is a reinvention of the basic

```cpp
product = a + b;
```

We didn’t need to go through all that trouble, and to make things worse it’s much more inefficient.

Writing code from scratch in a production environment is a waste of time, since code that performs a variety of useful functions already exists for you to use. Unless you are a researcher trying to invent more efficient implementations, chances are that someone else has already written something better than what you are envisioning.


To avoid copyright infringement and code plagiarism, developers may implement an existing algorithm or other portion of code. Some developers, as a result of limitation through architecture may need to implement something differently and in such a way that is less efficient than commonly used and readily available implementations.
