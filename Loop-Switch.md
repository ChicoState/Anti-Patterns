# Loop-Switch Sequence

A Loop-Switch Sequence is a pattern where a switch or set of conditionals is unnecessarily nested in a loop.

## Example:

````{c++}
for (int i = 0; i <= 5; i++)
{
    switch (i)
    {
        case 1:
            DoSomething();
            break;
        case 2:
            DoSomethingElse();
            break;
        case 3:
            DoTheNextThing();
            break;
        case 4:
            DoAnotherThing();
            break;
        case 5:
            DoTheLastThing();
            break;
    }
}
````

## Issues From Use:
The issues that arise from placing a switch inside a for loop reduces readability. But if the sequence of events are known at compile time the code structure then becomes redundant.

## Solution:

The correct version of using this pattern would be inversion of control. If this is used in order to handle a sequence of events not know at compile time. To implement this simply remove the switch and for loop and state the steps done within the switch statement. 
````
DoSomething();
DoSomethingElse();
DoTheNextThing();
DoAnotherThing();
DoTheLastThing();
````



Code examples from [level up code](https://levelupcode.wordpress.com/avoid/loop-switch-sequences/)
