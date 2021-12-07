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

### `Optional` Arguments

```python
import argparse

# Create a parser object which stores all the information
parser = argparse.ArgumentParser(description='Multiply two integers', epilog='Thank you for programming')

# metavar='Name' (A name for the argument in help message)
# Adding arguments
parser.add_argument('-x', '--x', type=int, metavar='X', required=True, help='Enter the first number')
parser.add_argument('-y', '--y', type=int, metavar='Y', required=True, help='Enter the second number')

# Parse the argument
args = parser.parse_args()

# Print the user input argument
product = args.x * args.y
print(f'Product : {product}')

Output :
python optional.py --x 4 --y 5 | python optional.py -x 4 -y 5
Product : 20
```

### `Positional` Arguments

```python
import argparse

# Create a parser object which stores all the information
parser = argparse.ArgumentParser(description='Multiply two integers', epilog='Thank you for programming')

# Adding arguments
# required is an invalid argument for positional
# default does not work with positional arguments (passing arguments is compulsory)
parser.add_argument('x', type=int, metavar='X', help='Enter the first number')
parser.add_argument('y', type=int, metavar='Y', help='Enter the second number')

# Parse the argument
args = parser.parse_args()

# Print the user input argument
product = args.x * args.y
print(f'Product : {product}')

Output :
python positional.py 4 5 
Product : 20
```
