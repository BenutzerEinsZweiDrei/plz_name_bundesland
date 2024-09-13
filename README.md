get bundesland like

```python

import json

# Load the JSON data from a file
with open('plz_ready.json', 'r') as file:
    data = json.load(file)

def get_bundesland(data, plz):
    for entry in data:
        if entry["postcode"] == plz:
            return entry["bundesland"]
    return None  # Return None if no matching postcode is found

# example
plz = "01067"
bl = get_bundesland(data, plz)
print(bl)

```
