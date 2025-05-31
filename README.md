PREPARATION
Go through the slide to revise what we did in class.

EXTRA RESOURCES
The following links will direct you to W3Schools, where you can further expand your knowledge beyond the slides. This resource is intended to complement, rather than replace, the content covered in the slides.

For string, click HERE

For list, click HERE

For tuple, click HERE

For set, click HERE

For dictionary, click HERE

NOTE: You can always reference the links above for easier to navigate reading tutorial.

PS: the essence of this assignment is to practice what you have learnt and also do personal research. Ensure you attempt it as that is how you can hone your programming skill.

Good luck!

IMPORTANT ASSIGNMENT
QUESTION 1
Ask a user to enter a value between 0 and 100 which represent temperature in degree celcius. Convert this value of temperature in degree celcius to fahrenheit. Assign the converted value to a variable called result and print out the value of the result variable.

HINT: The formular for converting temperature value in degree celcius to fehrenheit is:

f = (c×95)+32

where f represent temperature in fehrenheit
where c represent temperature in celcius
For example: if c(user input) = 5, then equivalent value in fehrenheit is: f = (5×95)+32=47

To get input from a user, research about input function. Here are useful links:

Reading link: input function on w3school
Video link: input function on YouTube

[ ]
Temperature_in_Degree_Celsius = float(input("Enter a temperature in Celsius (between 0 and 100): "))
Enter a temperature in Celsius (between 0 and 100): 53

[ ]
Temperature_in_Fahrenheit = (Temperature_in_Degree_Celsius * (9/5)) + 32
Result = Temperature_in_Fahrenheit
print (Result)
127.4
QUESTION 2
Given a list of numbers: lst=[1,6,1,10,7,100,0], print out two new variable (name them whatever you want) that reference the list above in:

Ascending order and
descending order respectively.
Hint: python list has the sort method that can be used sort a list. Run this code, help(list), to read more on how to use the sort method to order a list in ascending and descening.

You can also learn about sort through w3schools


[ ]
lst=[1,6,1,10,7,100,0]
Ascending = sorted(lst)
Descending = sorted(lst, reverse=True)
print ("Ascending Order:", Ascending)
print ("Descending Order:", Descending)
Ascending Order: [0, 1, 1, 6, 7, 10, 100]
Descending Order: [100, 10, 7, 6, 1, 1, 0]
QUESTION 3
Given the formular: V=43∗π∗r3, calculate the volume of a sphere of radius r=5 and the constant π=3.142?

Save the result in a variable called volume_of_cylinder_r5 and print out the value of the variable


[ ]
r=5
pi=3.142
V = (4/3) * pi * r**3
volume_of_cylinder_r5 = V
print (volume_of_cylinder_r5)
523.6666666666666
QUESTION 4
Suppose the cover price of a book is $24.95, but bookstores get a 40% discount. Shipping costs $3 for the first copy and 75 cents for each additional copy. What is the total wholesale cost for 60 copies?


[ ]
Wholesale_Cost = (24.95 * 0.6 * 60) + (3) + (0.75 * 59)
print (Wholesale_Cost)
945.4499999999999
QUESTION 5
Ask a user to enter a word(words) of odd length and assign the user entering to a variable named entry. Print the first, middle and last character from the entry value.

e.g if entry = "James", the printed value will be Jms

Hing: use the floor division to get the index of the middle value (len(entry)//2). Use what you learnt in class regarding index to get the first and last characters. Finally, concatenate the result together.

Check this blog for explanation: Get middle index of a string


[ ]
while True:
    Entry = input("Enter a word of odd length: ")
    if len(Entry) % 2 == 1:
        break
    print("The length of the word must be odd. Try again.")

print(f"You entered: {Entry}")
Enter a word of odd length: Victor
The length of the word must be odd. Try again.
Enter a word of odd length: Shola
You entered: Shola

[ ]
First_Middle_Last_Character = Entry[0] + Entry[len(Entry)//2] + Entry[-1]
print (First_Middle_Last_Character)
Soa
QUESTION 6
Ask a user to enter a name of odd length and assign the user entering to a variable named name.

Print a string made of the middle three characters of a given string.

e.g if name = "JaSonAy", printed result will be Son

Hint: Use the approach above to get the middle index and assign the middle index to a variable. Now slice the string from the index on the left of the middle index upto the right index of the middle index.


[ ]
while True:
  name = input ("Please enter a word of odd length: ")
  if len(name) % 2 == 1:
    break
  print ("The length of the word must be odd. Try again.")

print (f"You entered: {name}")

Please enter a word of odd length: Ashade
The length of the word must be odd. Try again.
Please enter a word of odd length: Ashante
You entered: Ashante

[ ]
Middle_3_Characters = name[len(name)//2-1:len(name)//2+2]
print (Middle_3_Characters)
han
QUESTION 7
Given two strings, word1 and word2, write a program to return a new string made of word1 and word2 first, middle, and last characters.

Initialise the two variables as: word1 = "America" and word2 = "Japan"

Your answer is expected to be 'AJrpan'


[ ]
word1 = "America"
word2 = "Japan"

first_char = word1[0] + word2[0]
middle_char = word1[len(word1)//2] + word2[len(word2)//2]
last_char = word1[-1] + word2[-1]

new_string = first_char + middle_char + last_char

print(new_string)
AJrpan
QUESTION 8
Given a variable and its value as word = "PyNaTive". This word contains a combination of lower and upper case letters.

Write a program to arrange the characters of a string so that all lowercase letters should come first.

Hint: you can iterate through the characters using for loop and checl if each character is upper case or not. You can create an empty string and concatenate those that lowercase character to the empty string first followed by those that are uppercase.


[ ]
word = "PyNaTive"

lowercase_chars = ""
uppercase_chars = ""

for char in word:
    if char.islower():
        lowercase_chars += char
    else:
        uppercase_chars += char

arranged_word = lowercase_chars + uppercase_chars

print(arranged_word)
yaivePNT
QUESTION 9
Count all letters, digits, and special symbols from a given string:

characters = "P@#yn26at^&i5ve".

Hint: remember that every characters in a string is a string object even it is a number. For example, the the first number in the string above is something like this, '2' (string) and not something like this, 2 (integer) without the quotation. str (string) object has a method that can check if a member of a string is a number (e.g '2'). Call help on str to find the string method that will help you with this challenge.

All you need is to 3 different variables and assign zero to them to keep track of the count of numbers, special characters and alphabet. Example:

number_count = 0
alphabet_count = 0
symbol_count = 0
Now iterate throgh the string. if it is a number, increment number_count by 1, else if it is symbol, increment symbol_count by 1 else if it is an alphabet, increment alphabet_count by 1.

There is a python method to check if a number if a character is a number. To check for symbols, create a list of all special characters and check if that character is there.


[ ]
characters = "P@#yn26at^&i5ve"

number_count = 0
alphabet_count = 0
symbol_count = 0

# Define a string of special characters
special_characters = "!@#$%^&*()_+-=[]{}|;:'\",.<>?/`~"

# Iterate through each character in the string
for char in characters:
    if char.isdigit():
        number_count += 1  # Count digits
    elif char.isalpha():
        alphabet_count += 1  # Count alphabet characters
    elif char in special_characters:
        symbol_count += 1  # Count special symbols

# Output the counts
print("Letters:", alphabet_count)
print("Digits:", number_count)
print("Special Characters:", symbol_count)
Letters: 8
Digits: 3
Special Characters: 4
QUESTION 10
Write a program to check if two strings are balanced. For example, two strings are balanced if all the characters in the first string are present in the second string. The character’s position doesn’t matter.

Initialise the two strings as: string1 = "Yn" and string2 = "PYnative"


[ ]
# Initialize the two strings
string1 = "Yn"
string2 = "PYnative"

# Check if all characters in string1 are present in string2
is_balanced = all(char in string2 for char in string1)

# Output the result
print(is_balanced)
True
QUESTION 11
Write a program to find all occurrences of “USA” in a given sentence ignoring the case.

Given: sentence = "Welcome to USA. usa awesome, isn't it?". The result should be 2.

Hint: there is a python method that you can use to get the index of the first character you are searching for. Once you get it, use that index as start to slice string upto the next 3 characters (since USA is 3 letter word).


[ ]
sentence = "Welcome to USA. usa awesome, isn't it?"
word = "usa"

count = sum(sentence[i:i+3].lower() == word for i in range(len(sentence) - 2))
print("Number of occurrences:", count)
Number of occurrences: 2
QUESTION 12
Given a string, write a program to return only the sum and average (in 2 decimal places) of the digits that appear in the string, ignoring all other characters.

Given: str1 = "PYnative29@#8496", the sum of the digit is 38 and the average is 6.33.

Hint:

Initialize a variable called total and assign 0 to it (total=0).
Also initialize count variable and assign 0 to it as well (count=0)
Iterate throguh the string (since it is a sequence of characters).
For each character, check if it is a number (there is a sting method to check if a string is a number).
If it is a number, sum it with the total variable that you initialized in step 1 and also increase the count variable by 1 to show that you are keeping track of the number of integers you have else just bypass and go to the next iteration.
After the iteration, you should have gotten the total sum and the number of integers in the string. To get the average, divide the total variable by count variable

[ ]
# Initialize the given string
str1 = "PYnative29@#8496"

# Initialize variables for sum and count of digits
total = 0
count = 0

# Iterate through the string
for char in str1:
    if char.isdigit():  # Check if the character is a digit
        total += int(char)  # Add the digit to the total sum
        count += 1  # Increase the count of digits

# Calculate the average, ensuring no division by zero
average = total / count if count != 0 else 0

# Format the average to 2 decimal places
average = round(average, 2)

# Output the sum and average
print("Sum:", total)
print("Average:", average)
Sum: 38
Average: 6.33
QUESTION 13
Write a program to print all characters and the number of characters within the string in question 12.

Hint: Just like the precious question, create a count variable and assign 0 to it (count=0). But this time around, the variable will be used to track the count of characters. You will iterate to check if an element of a string in each iteration is a character (any of letter a-z or A-Z). If it is, increment that count variable by 1 and also print the character.v


[ ]
# Initialize the given string
str1 = "PYnative29@#8496"

# Initialize count variable for characters
count = 0

# Iterate through the string
for char in str1:
    if char.isalpha():  # Check if the character is a letter (a-z or A-Z)
        count += 1  # Increment count for each character
        print(f"Character: {char}, Count: {count}")  # Print the character and count

# Output the total count of characters
print(f"Total number of characters: {count}")
Character: P, Count: 1
Character: Y, Count: 2
Character: n, Count: 3
Character: a, Count: 4
Character: t, Count: 5
Character: i, Count: 6
Character: v, Count: 7
Character: e, Count: 8
Total number of characters: 8
QUESTION 14
Reverse and print the output of the string you got in question 13.


[ ]

Start coding or generate with AI.
QUESTION 15
Write a program to print the index of the first character (B) of the last substring “Beauty” in the sentence:

str1 = "Beauty is a data scientist who knows Python. Beauty works at google."

Hint: there is a string method to get the index of the first occurence of a string.


[ ]
# Initialize the given string
str1 = "Beauty is a data scientist who knows Python. Beauty works at google."

# Find the index of the first occurrence of the substring "Beauty"
index = str1.rfind("Beauty")

# Print the index of the first character of the last occurrence of "Beauty"
print(index)
45
QUESTION 16
Write a program to split a given string on hyphens and display each substring. Given: str1 = Beauty-is-a-data-scientist.

Hint: string has a split method. Call help on str.


[ ]

# Initialize the given string
str1 = "Beauty-is-a-data-scientist"

# Split the string on hyphens
substrings = str1.split('-')

# Display each substring
for substring in substrings:
    print(substring)
Beauty
is
a
data
scientist
BONUS QUESTION
FINDING THE MEDIAN INDEX OF A SEQUECE WITH EVEN SIZE IN PYTHON
One thing i didn't mention was that the median index is different from the median value so for median index of a list with odd number as its size, we will have to choose the left or right index of the two middle index

Check the code below for example


[ ]
# Function to find the median index
def find_median_index(sequence):
    # Get the size of the sequence
    size = len(sequence)

    # For odd size list, the median index is the exact middle
    if size % 2 != 0:
        median_index = size // 2  # Integer division gives the middle index
    else:
        # For even size list, you can choose the left or right of the two middle elements
        # Here, I will choose the left one (size // 2 - 1)
        median_index = size // 2 - 1  # Left middle index for even size

    return median_index

# Example usage
sequence_odd = [1, 3, 5, 7, 9]
sequence_even = [1, 3, 5, 7, 9, 11]

# Find median index
print("Median index (odd-sized list):", find_median_index(sequence_odd))  # Output: 2
print("Median index (even-sized list):", find_median_index(sequence_even))  # Output: 2
Median index (odd-sized list): 2
Median index (even-sized list): 2

[ ]
numbers = [1,2,39,4,166,7,8,93,50,12,11,23,45,67,78]
sorted (numbers)
n = len(numbers)
print(n)
numbers2= sum(numbers)
numbers3 = (numbers2 + 1)
# Median Index formular = [(n+1)/2]th
median_index = (n+1)/2
print (median_index)
#Median Index is the eight value
Numbers3 = sorted (numbers)
Numbers3 [7]
15
8.0
23
Since we have two middle values becaue the length of the string is 2, we can say we don't have middle index unless we want to use the value of mid_index above which is 2 or we use a value below it which 1 (i.e 2-1 which is equal to 1 for the second position) as the index value.

READING ASSIGNMENT - PYTHON FUNCTION
Read about python function here.


[ ]
# Function to find the median index
def find_median_index(sequence):
    # Get the size of the sequence
    size = len(sequence)

    # For odd size list, the median index is the exact middle
    if size % 2 != 0:
        median_index = size // 2  # Integer division gives the middle index
    else:
        # For even size list, we have two middle indices
        median_index_left = size // 2 - 1  # Left middle index
        median_index_right = size // 2  # Right middle index
        return median_index_left, median_index_right  # Return both indices for the even case

    return median_index  # Return single median index for odd-sized list

# Example usage
sequence_odd = [1, 3, 5, 7, 9]
sequence_even = [1, 3, 5, 7, 9, 11]

# Find median index
print("Median index (odd-sized list):", find_median_index(sequence_odd))  # Output: 2
print("Median index (even-sized list):", find_median_index(sequence_even))  # Output: (2, 3)
Median index (odd-sized list): 2
Median index (even-sized list): (2, 3)

[ ]

Start coding or generate with AI.
Colab paid products - Cancel contracts here
