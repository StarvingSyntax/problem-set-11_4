# Problem Set 11.4 - Recursion

## Directions
Respond to short response questions in clear, concise sentences directly within this file. Use markdown to ensure that your answers are formatted correctly.

### Short Response Questions
**1. What is recursion?**
  Recursion is the concept of a function calling upon itself in their function body. This is expecially useful if you're function relies on a lot of looping to get your expected output.

**2. What type of problems are best solved using recursion?**

**3. What are the benefits of writing functions recursively? What are the drawbacks?**

  Utilizing recursive functions versus simple iteration comes with it's positives and negatives. If the base case and recursive case are not properly set, the function can result in an infinite loop. With the fibonacci sequence, for example, iterating through the sequence would allow us to have a linear time complexity in contrast to recursively finding an answer which gives us a runtime of of log of n. As for space, the amount of memory used during the execution of fib(5) vesus fib(105) is the same. It's constant or O(1). Though, using recursive logic makes the space required proportional to the maximum amount of recurssions made by the function until it hits it's base case.
  
  , because , that is the maximum number of elements that can be present in the implicit function call stack.



### Coding Exercises
Answer the following questions in `exercises.py`. Run unit test with the `pytest` command. Ensure all tests are passing before submitting this problem set.

1. **_Reverse a String:_** This interview question requires you to reverse a string using recursion. Make sure to think of the base case here and make sure you use recursion to accomplish this! Do not slice (e.g. string[::-1]) or use iteration, there must be a recursive call for the function.

2. **_Fibonnaci Sequence:_** Implement a Fibonnaci Sequence in three different ways - Recursively, Dynamically (Using Memoization to store results), and Iteratively. Remember the fibonacci sequence: `0,1,1,2,3,5,8,13,21,...`

3. **_Integer to String:_** Write a recursive function that takes two parameters - an integer input, `n`, and an integer base, `m` - and returns a string represenation of the number in Base `m`.



---

from functoosl import lru_cache

def factorial(num: int) -> int:
    #Multiply that number and every number previously
    fact = 1
    
    for i in range(num, 0):
        fact *= 1
        
    return fact

# print(factorial(5) == 120)
# print(factorial(4) == 24)
# print(factorial(6) == 720)


def recursive_factorial(num: int) -> int:
    
    #base case
    if num == 1:
        return 1
    else:
        return num * recursive_factorial(num - 1)
