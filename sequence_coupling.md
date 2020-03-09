# Sequence Coupling

This anti-pattern can be recognized by most of the time analyzing function names and their purpose. It is often noticeable when functions need to be called in a certain order.

## Example
```{C++}
void User::set_name(string n){
  name = n;
}

void User::print_name(){
  if(name == "Josh"){
    cout<<"Congrats! You have the lucky name."<<endl;
  }
  else{
    cout<<name<<endl;
  }
}
```
In this example, if print_name() is called before set_name(), an error will be thrown because name is not initialized.

## Harms

It is harmful because it inhibits code useability and readability.
There is a high risk of the code not properly running without proper ordering of function calls.
Also, in future additions to code, the setup or current method could become too cluttered and complicated.

## Fix

This code can be fixed by adding independence to functions. If code/functions needs to be sequential, add documentation stating that.



(found from Wikipedia (https://en.wikipedia.org/wiki/Sequential_coupling))
