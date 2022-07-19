# Reverse-letters-in-words-in-string
A String DSA Question from Leetcode - originally as - reverse-words-in-a-string-iii

Basically u need to reverse each word in a string
I solved it using Cpp strings and 2 pointer method

In this approach, We first demarcate a word, and then reverse it.

To demarcate the word, we use 2 pointers i and j; i stays at the start position and and j increments by 1 till j finds a whitespace, then the pointers are send to reverse function. 
In this function we are passing string by reference (i.e. we send the memory address) of the string using & operator. This makes sure that the original string gets modified (thus leading us to an in-place solution)
So, in this called function, we again take new pointers st (start) and et (end), which are swapped and then incremented and decremented by 1 respectively till st<=et. So here the word gets reversed.
We need to take care that et=j-1, this is because the j to the position of whitespace and not the last letter of the word.
Now, we change i to i=j+1, thus pointing to the start of new word (i.e. after the whitespace) and the process continues.

If the string ends, i.e. j becomes = string.length(), then we come out of loop and finally reverse the last word using the same function as above

We need to use & operator to pass string in reverse function. 

This has O(n^2) time complexity yet, it shows faster than  86.08% in leetcode. In has O(1) space complexity
