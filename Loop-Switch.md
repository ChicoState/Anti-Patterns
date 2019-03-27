# Loop-Switch Sequence

A Loop-Switch Sequence is a pattern where a switch or set of conditionals is unnecessarily nested in a loop.

## Example

```// parse a key, a value, then three parameters 
String key = null;
String value = null;
List<String> params = new LinkedList<String>();

for (int i = 0; i < 5; i++) {
    switch (i) {
        case 0:
            key = stream.parse();
            break;
        case 1:
            value = stream.parse();
            break;
        default:
            params.add(stream.parse());
            break;
    }
}
```

## Problems

Harmful mostly because it is harder to read/maintain, and it's doing pointless checks which may slow
down the program.

## How to fix it

Take out the steps that you know are going to execute in a certain order out of the loop
and do them before or after. For example, the code above could be refactored into this:
```// parse a key and value
String key = stream.parse();
String value = stream.parse();

// parse 3 parameters
List<String> params = new LinkedList<String>();
for (int i = 0; i < 3; i++) {
    params.add(stream.parse());
}
```



Code examples from [wiki visually](https://wikivisually.com/wiki/Loop-switch_sequence)
