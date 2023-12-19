# command-line-arguments-to-count-word
## AIM:
To write a python program for getting the word count from the contents of a file using command line arguments.
## EQUIPEMENT'S REQUIRED: 
PC
Anaconda - Python 3.7
## ALGORITHM: 
### Step 1:
Accept a filename as a command-line argument.
### Step 2: 
If the number of command-line arguments is not equal to 2 then Display an error message indicating proper usage. Exit the program with a status code of 1.
### Step 3: 
Open the file with the specified filename in read mode.
### Step 4:  
Read the entire content of the file.
### Step 5: 
Use the split() method to break the content into a list of words and Calculate the total number of words in the file by finding the length of the list of words.
### Step 6: 
Create a dictionary to store the frequency of each unique word using a set and a dictionary comprehension.Print the total word count in the file and Print the word frequency dictionary.

## PROGRAM:
```python
Developed by: M B ANU VARSHINI
RegisterNumber: 23008712 

import sys
if len(sys.argv) != 2:
    print("Usage: python script.py code.txt")
    sys.exit(1)
filename = sys.argv[1]
with open(filename, 'r') as file:
    words = file.read().split()
    total_words = len(words)
    word_counts = {word: words.count(word) for word in set(words)}
print("Word count in file:", total_words)
print("Word frequency in file:", word_counts)
```
### OUTPUT:



## RESULT:
Thus the program is written to find the word count from the contents of a file using command line arguments.
