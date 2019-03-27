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

Harmful because it is harder to read, and it's doing pointless checks which slows
down the process.

## How to fix it

Take out the steps that you know are going to execute in a certain order out of the loop
and do them before or after.

Code examples from [wiki visually](https://wikivisually.com/wiki/Loop-switch_sequence)
