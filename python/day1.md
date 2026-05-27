# DAY 1
Important python basics.

## 1.String 
### String reverse:
Reverses the string.
```python
name = "cybersecurity"
name[::-1]
```
### Check substring:
Substring is a string inside a string.
```python
name = "cybersecurity"
"cyber" in name
```
### Last element:
Element at the end of the string, you can also use this in other functions too.  
Ex, List,set,array,...
```python
name = "cybersecurity"
name[-1]
```

## 2.List
List is a collection of data.
### Append:
Add to the list.
```python
ports = [631,53,22,20]
ports.append(21)
```
### Remove:
Delete from the list.
```python
ports = [631,53,22,20]
ports.remove(20)
```

## 3.Dictionary
Dictionary is set of key, value pairs.
### Empty dictionary:
```python
services = {}
```
### Add to dictionary:
```python
services[21] = "FTP"
```
21 is a key and "FTP" is value.
keys are unique.

### Traverse dictionary:
```python
for key,value in services.items():
  print(key,value)
```
services.items() returns key, value pairs.

### Keys:
```python
services.keys()
```
This returns keys in services dictionary.

### Values:
```python
services.values()
```
This returns values in services dictionary.

### Value of specific key:
```python
services.get(21)
```
This returns value at key 21 in services dictionary.

## 4.Files
### Read:
Read from the file.
```python
with open("notes.txt","r") as f:
  print(f.read())
```
### Write:
Write to the file, removing any content the file had before.
```python
with open("notes.txt","w") as f:
  f.write("hello")
```
### Append:
Write to the file, keeping the contents of the file.
```python
with open("notes.txt","a") as f:
  f.write("\nhi")
```
## 5. Functions
Reusable block again and again.
### Simple Function:
```python
def greet(name):
    print("Hello", name)
```

### Return:
```python
def square(num):
    return num * num
```
## 6.Exception handling
If an error occurs it can be handled by try and except blocks, try catches the error and executes except block, if no error except block is unused.
### try-except:
```python
try:
  age = int(input("Enter your age: "))
except:
  print("Enter proper age")
```
