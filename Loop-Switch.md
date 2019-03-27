# Loop-Switch Sequence
--
A Loop-Switch Sequence is a pattern where a switch or set of conditionals is unnecessarily nested in a loop.

## Example

// parse a key, a value, then three parameters 
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
  
## Problems


## How to fix it



Code examples from [wiki visually](https://wikivisually.com/wiki/Loop-switch_sequence)
