# Top-Python-Interview-Questions-and-Concepts
Top Python Interview Questions and Concepts asked in Amazon, Google, Microsoft and Other Top Companies
Python is one of the most popular programming languages in the world, with a wide range of applications in various fields such as web development, data analysis, artificial intelligence, and more. As a result, many companies around the world have adopted Python as their primary programming language, making it an essential skill for any software developer. In this blog post, we will discuss some of the top Python interview questions and concepts that you should be familiar with when applying for a job in this field.


1-Write a program to reverse a string in Python.

This question evaluates the candidate’s understanding of string manipulation in Python. Companies such as Amazon, Google, and Microsoft have asked this question in their interviews.

def reverse_string(str_):  # Function to reverse a string 
  return str_[::-1]        # Using string slicing with step -1 to reverse the string

str_ = "program to reverse a string in Python"   # Input string
print(reverse_string(str_))   # Calling the reverse_string function and printing the result
def reverse_string(str_):
  str_1=""                           # Initialize an empty string to store the reversed string
  for i in str_.split():             # Split the input string at whitespace characters to get a list of words
    str_1+=i[::-1]+str(" ")         # Reverse the characters in each word using string slicing, and append it to the reversed string along with a space character
  return str_1                       # Return the reversed string
str_="program to reverse a string in Python"
print(reverse_string(str_))
2-Write a program to find the largest and smallest elements in a list in Python.

This question evaluates the candidate’s understanding of list manipulation in Python. Companies such as Facebook, Apple, and LinkedIn have asked this question in their interviews.

l = [1212, 34, 2, 4, 45, 76, 2, -23, 129]    # Given list of numbers

def largest_element(l):
    """
    A function to find the largest and smallest elements in a list.

    Parameters:
        - l (list): The list of numbers to find the largest and smallest from

    Returns:
        - max (int): The largest element in the list
        - min (int): The smallest element in the list
    """

    max = l[0]    # Assume the first element as the maximum
    min = l[0]    # Assume the first element as the minimum

    for i in l:
        if i > max:
            max = i    # Update max if a larger element is found
        elif i < min:
            min = i    # Update min if a smaller element is found

    return max, min    # Return the largest and smallest elements as a tuple

print(largest_element(l))    # Call the function and print the result
l = [1212, 34, 2, 4, 45, 76, 2, -23, 129]    # Given list of numbers

def largest_element(l):
    """
    A function to find the largest and smallest elements in a list.

    Parameters:
        - l (list): The list of numbers to find the largest and smallest from

    Returns:
        - max (int): The largest element in the list
        - min (int): The smallest element in the list
    """

    sorted_l = sorted(l)    # Sort the list in ascending order
    min = sorted_l[0]    # Get the first element from the sorted list (smallest element)
    max = sorted_l[-1]    # Get the last element from the sorted list (largest element)

    return max, min    # Return the largest and smallest elements as a tuple

print(largest_element(l))    # Call the function and print the result
3- Write a program to find the second largest number in a list in Python.

This question evaluates the candidate’s understanding of list manipulation and sorting algorithms in Python. Companies such as IBM, Oracle, and Samsung have asked this question in their interviews.

l = [1212, 34, 2, 4, 45, 76, 2, -23, 129]    # Given list of numbers

def second_largest(l):
    """
    A function to find the second largest number in a list.

    Parameters:
        - l (list): The list of numbers to find the second largest from

    Returns:
        - second_largest_number (int): The second largest number in the list
    """

    sorted_l = sorted(l)    # Sort the list in ascending order
    second_largest_number = sorted_l[-2]    # Get the second-to-last element from the sorted list

    return second_largest_number    # Return the second largest number

print(second_largest(l))    # Call the function and print the result
4- Write a program to check whether a given number is prime or not in Python.

This question evaluates the candidate’s understanding of loops, conditionals, and mathematical concepts in Python. Companies such as Uber, Airbnb, and Twitter have asked this question in their interviews.

def prime_number(n):
    """
    A function to check if a given number (n) is a prime number.

    Parameters:
        - n (int): The number to be checked for prime

    Returns:
        - None: The function prints the result directly
    """

    flag = True    # Initialize a flag variable to True

    if n <= 1:    # If the number is less than or equal to 1, print an error message
        print("Kindly provide a valid number greater than 1")
    else:
        for i in range(2, (n // 2) + 1):    # Iterate from 2 to half of the given number
            if n % i == 0:    # If the number is divisible by any number in the range, set the flag to False and break
                flag = False
                break
            else:
                flag = True    # If the number is not divisible by any number in the range, set the flag to True

    if flag:
        print(f"{n} is a prime number")    # If the flag is True, the number is prime
    else:
        print(f"{n} is not a prime number")    # If the flag is False, the number is not prime

n = int(input("Enter a number to check if it's a prime number: "))    # Take input from the user
prime_number(n)    # Call the prime_number function to check if the input number is prime or not
5- Write a program to implement a binary search algorithm in Python.

This question evaluates the candidate’s understanding of algorithms and data structures in Python. Companies such as Google, Microsoft, and Intel have asked this question in their interviews.

def binary_search(arr, n):
    """
    A binary search algorithm to find the position (index) of a target element (n)
    within a sorted list (arr).

    Parameters:
        - arr (list): Sorted list of elements to search
        - n (int): Target element to search for

    Returns:
        - int: Index of the target element in the list, or -1 if not found
    """

    left = 0                 # Initialize the left pointer to the beginning of the list
    right = len(arr) - 1     # Initialize the right pointer to the end of the list

    while left <= right:    # Continue the loop as long as left pointer is less than or equal to right pointer
        mid = (left + right) // 2    # Calculate the middle index of the current range

        if arr[mid] == n:    # If the middle element is equal to the target value, return the index
            return mid
        elif arr[mid] < n:   # If the middle element is less than the target value, update the left pointer
            left = mid + 1
        else:                 # If the middle element is greater than the target value, update the right pointer
            right = mid - 1

    return -1    # Return -1 if target element is not found

arr = [23, 54, 7, 2, -7, 32, 87, 17]    # Input list of elements
arr = sorted(arr)    # Sort the input list (binary search requires a sorted list)
n = 7                # Target element to search for

index = binary_search(arr, n)    # Call the binary_search function to find the index of the target element

if index != -1:    # If the target element is found, print the index
    print(f"The element {n} was found at index {index}")
else:
    print(f"The element {n} is not in the sorted list {arr}")    # If the target element is not found, print a message
6- Write a program to implement a bubble sort algorithm in Python.

This question evaluates the candidate’s understanding of sorting algorithms in Python. Companies such as Amazon, Facebook, and Oracle have asked this question in their interviews.

arr = [23, 54, 7, 2, -7, 32, 87, 17]  # Given list of numbers

def bubble_sort(arr):
  for i in range(len(arr)-1):  # Iterate through the list from the beginning to the second-to-last element
    for j in range(i+1,len(arr)):  # Iterate through the list from the element next to i to the last element
      if arr[i] > arr[j]:  # Compare the current element with the next element
        arr[i], arr[j] = arr[j], arr[i]  # Swap the elements if they are in the wrong order

  return arr  # Return the sorted list

print(f"Sorted array in Ascending order is {bubble_sort(arr)}")  # Print the sorted array in ascending order
7- Write a program to calculate the factorial of a given number in Python.

This question evaluates the candidate’s understanding of loops and mathematical concepts in Python. Companies such as IBM, Apple, and LinkedIn have asked this question in their interviews.

def factorial(n):        # Define a function to calculate the factorial of a number
  if n<1:                 # Check if the input number is less than 1
    return print("enter a number above 1")   # If yes, print an error message
  else:
    fact=1                # Otherwise, initialize a variable 'fact' with 1 to store the factorial
    for i in range(1,n+1):   # Loop through the numbers from 1 to n (inclusive)
      fact*=i            # Multiply the current number with 'fact' to calculate the factorial
    return fact          # Return the calculated factorial
n=5                  # Set the value of n to -1 for testing
print(f"the factorial of {n} is {factorial(n)}")   # Call the factorial function with n as argument and print the result
8- Write a program to check whether a given string is a palindrome or not in Python.

This question evaluates the candidate’s understanding of string manipulation and conditionals in Python. Companies such as Google, Facebook, and Uber have asked this question in their interviews.

def palindrome(string_):
  flag=True                         # Initialize a flag variable to True
  for i in range(len(string_)//2):  # Loop through the characters of the string up to half of its length
    
    if string_[i]!=string_[-(i+1)]: # Compare the characters at the corresponding positions from the beginning and the end
      flag=False                    # If characters are not equal, set flag to False and break out of the loop
      break
  if flag:                          # If flag is still True after the loop, it means the input string is a palindrome
    print(f"{string_} is a palindrome")
  else:
    print(f"{string_} is not a palindrome") # If flag is False, it means the input string is not a palindrome

s="madaa"
palindrome(s)  # Call the palindrome function with the input string "madam"
9- Write a Python program that accepts a sequence of words as input and prints the unique words in sorted form.

This question evaluates the candidate’s understanding of string manipulation, data structures, and sorting algorithms in Python. Companies such as Microsoft, Amazon, and Oracle have asked this question in their interviews.

def sorted_words_list(string_):
  # Convert the input string to a list of words using the split() method
  word_list = string_.split()
  word_list=set(word_list)  #For unique words
  
  # Sort the list of words in alphabetical order
  word_list_sorted = sorted(word_list)
  
  # Return the sorted list of words
  return word_list_sorted

# Prompt the user to enter  sequence of words
string_of_words = input("Enter sequence of words: ")

# Call the sorted_words_list() function with the input string and print the result
print(sorted_words_list(string_of_words))
10- Write a Python function to insert a string in the middle of a string. Input: [[]] Python Output: [[Python]]

This question evaluates the candidate’s understanding of string manipulation and function definition in Python. Companies such as Airbnb, Google, and Uber have asked this question in their interviews.

def srting_shape_word(string_shape, word):
  # Slices the first two characters of the string shape, concatenates it with the given word, and adds the last two characters of the string shape
  output_string = string_shape[:2] + str(word) + string_shape[-2:]
  
  # Returns the output string
  return output_string

string_shape="[[]]"
word="Python"
srting_shape_word(string_shape,word)
11- Write a Python program to count the number of characters (character frequency) in a string.

This question evaluates the candidate’s understanding of string manipulation, loops, and dictionaries in Python. Companies such as Microsoft, Google, and Facebook have asked this question in their interviews.

def count_element(str_):
  # Create an empty dictionary to store the frequency of characters
  dic={}
  # Loop through each character in the string
  for i in str_:
    # Get the keys of the dictionary
    keys=dic.keys()
    # If the character already exists in the dictionary, increment its frequency
    if i in keys:
      dic[i]+=1
    # If the character does not exist in the dictionary, add it with a frequency of 1
    else:
      dic[i]=1
  # Return the dictionary containing the frequency of characters
  return dic

str_="pyhton progarm to count the"
print(f"Frequency of words in given string = {count_element(str_)}")
12- Write Python code to check the Armstrong number.

This question evaluates the candidate’s understanding of loops, conditionals, and mathematical concepts in Python. Companies such as IBM, Intel, and Samsung have asked this question in their interviews.

def check_Armstrong(n):
    # Store the original number in a variable called num
    num = n
    # Initialize a variable called sum to 0
    sum = 0
    # While n is not equal to 0
    while n != 0:
        # Extract the last digit of n
        a = n % 10
        # Add the cube of the digit to sum
        sum += a**3
        # Remove the last digit from n
        n -= a
        n = n // 10
    # If num is equal to sum, then it is an Armstrong number
    if num == sum:
        return "Armstrong Number"
    else:
        return "Not Armstrong Number"

n=12

check_Armstrong(n)
13- Write a function rotate(ar[], d, n) in Python that rotates arr[] of size n by d elements.

This question evaluates the candidate’s understanding of arrays and loops in Python. Companies such as Amazon, Microsoft, and Google have asked this question in their interviews.

def rotate(arr, d, n):
    # create a new array to store the rotated elements
    rotated = [0] * n
    
    # copy the d elements at the end of the array to the beginning of the rotated array
    for i in range(d):
        rotated[i] = arr[n - d + i]
        
    # copy the remaining elements to the rotated array
    for i in range(n - d):
        rotated[i + d] = arr[i]
        
    # return the rotated array
    return rotated
arr = [1, 2, 3, 4, 5, 6, 7]
d = 3
n = len(arr)
rotated = rotate(arr, d, n)
print(rotated)
14- Write a Python program to find all pairs of unique elements in a list whose sum is equal to a given target value.

This question evaluates the candidate’s understanding of list manipulation and control flow structures in Python. Companies such as Amazon, Microsoft, and Google have asked this question in their interviews. The question evaluates the candidate’s ability to use loops to iterate over a list and find pairs of elements whose sum is equal to a given target value.

# define a function target_sum that takes a list and a target value as input
def target_sum(lst, target):
    # create an empty list to store the pairs whose sum is equal to the target
    target_sum_list = []
    
    # loop through all possible pairs of elements in the list
    for i in range(len(lst)-1):
        for j in range(i+1, len(lst)):
            # check if the sum of the pair is equal to the target value
            # and if the pair is not already in the list of pairs
            if lst[i]+lst[j]==target and (lst[i],lst[j]) not in target_sum_list and (lst[j],lst[i]) not in target_sum_list:
                # add the pair to the list of pairs
                target_sum_list.append((lst[i],lst[j]))
    
    # return the list of pairs whose sum is equal to the target
    return target_sum_list

# create a list and a target value
lst = [2, 4, 3, 5, 7, 8, 9, 2,5,0,7]
target = 7

# call the target_sum function with the list and target as input
# and print the result
print(target_sum(lst, target))
15- Write a Python program to check if two strings are anagrams of each other.

This question evaluates the candidate’s ability to manipulate strings and use control flow structures in Python. Companies such as Amazon, Facebook, and Google have asked this question in their interviews. The question evaluates the candidate’s understanding of string manipulation and the use of dictionaries in Python. Candidates should know how to check if two strings are anagrams of each other by comparing the frequency of characters in each string.

def are_anagrams(str1, str2):
    # Convert the strings to lowercase and remove whitespace
    str1 = str1.lower().replace(" ", "")
    str2 = str2.lower().replace(" ", "")
    
    # Check if the lengths of the strings are equal
    if len(str1) != len(str2):
        return False
    
    # Convert the strings to lists and sort them
    str1_list = sorted(list(str1))
    str2_list = sorted(list(str2))
    
    # Compare the sorted lists
    if str1_list == str2_list:
        return True
    else:
        return False


str1="Listen to me "
str2="silent me o t"
anagram(str1,str2)
Conclusion:
In conclusion, these are some of the top Python interview questions and concepts that candidates should be familiar with. These questions cover a range of topics, including string manipulation, list manipulation, sorting algorithms, and arithmetic operations. Candidates can prepare for these questions by practising coding exercises and studying Python concepts in-depth.

It’s also worth noting that different companies may place more emphasis on certain topics than others, so candidates should tailor their preparation to the specific companies they are applying to. Overall, mastering these concepts will help candidates stand out in the competitive job market and succeed in Python-related job interviews.

Check out my other Blogs

ML Use Cases in Banking, Finance & Insurance: Advancements and Examples

Introducing OpenAI’s ChatGPT

Revolutionizing E-Learning with Machine Learning: Popular Models and Use Cases

Choosing the Right Algorithm in Machine Learning

Analysis of the “Google Merchandise Store” website using Google Analytics and making dashboards on Google Data Studio

Using Machine Learning for Sentiment Analysis and Price Prediction in the Cryptocurrency Industry

Forecasting Techniques for Stationary and Non-stationary Time-Series

Ifyou found this content helpful, please give it a like as your support motivates us to create more valuable content for you. You can also connect with me, Deepak Dobal, on LinkedIn. Thank you for your support!
