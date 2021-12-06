# `argparse`

- Standard Python library used for parsing the command line arguments.
- `Parsing` : Process of taking data in one format and transforming it to another format.
- `Arguments` : `Input` values which we pass (parsed) in order to perform some operation.

```python
# Install the library
pip install argparse

# Import the library
import argparse

# Create a parser object which stores all the information
parser = argparse.ArgumentParser(description='Greet the user', epilog='Thank you for programming')

# Adding arguments
# Optional arguments : '-name', '--name'
# Positional arguments do not starts with '-' or '--'
# help : description about the argument
parser.add_argument('-n', '--name', type=str, metavar='', required=True, help='Enter the user name')

# Parse the argument
args = parser.parse_args()

# Print the user input argument
print(f'Good Morning {args.name}')

Output :
python greet.py --name Kirankumar | python greet.py -n Kirankumar

Good Morning Kirankumar
```
