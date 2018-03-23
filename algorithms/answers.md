# Exercise 1

1.   
    a = 0;  

    while (a < n * n * n)  

    a = a + n * n;   


_answer:_  

BigO notation is O(n), linear time. n^2 steps are taken to reach n^3.

2.  
    // input array is of length n   
    
    i = array.length - 1;  

    while (array[i] > x && i >= 0)  

    i = i/2;   


_answer:_   

BigO notation is O(logn) because each iteration cuts i by half.   


3.  
    sum = 0;  

    for (i = 0; i < Math.sqrt(n) / 2; i++)  

    for ( j = i; j < 8 + i; j++)  

    for (k = j; k < 8 + j; k++)  

    sum++;  


_answer:_   

BigO notation is O(sqrt(n)) the algorithm requires O(n^(1/2)) evaluations where the size of input is n. 

4.  
    sum = 0;  

    for (i = 1; i < n; i *= 2)  

    for (j = 0; j < n; j++)  

    sum++;   


_answer:_   

BigO notation is O(nlogn) because the inner loop in linear and the outer loop doubles in value with each step.

5.  
    sum = 0;  

    for (i = 0; i < n; i++)  

       for (j = i + 1; j < n; j++)  

         for (k = j + 1; k < n; k++)  

           for (l = k + 1; l < 10 + k; l++)  

             sum++;   


_answer:_   

BigO notation is O(n^3) due to the three nested linear loops with (l = k +1; l < 10 + k; l++) being constant. 

6.  
    bunnyEars = function (bunnies) { // here bunnies === n  
     if (bunnies === 0) return 0;  

    return 2 + bunnyEars(bunnies-1);  

    }  


_answer:_   

BigO notation is O(n).  Despite being a recursive call, this algorithm is linear time because the value of n increases by 1 and then decreases by 1 once the condition is met.

7.  
    search = function (array, arraySize, target) { // here arraySize === n if (arraySize > 0) {  

         if (array[arraySize-1] === target) return true;  

         else return search(array, arraySize-1, target);  

       }  

      return false;  

     }   


_answer:_  

BigO notation is O(n) for reasons similar to number 7.  

# Exercise 2  


1. Given an array a of n numbers, design a linear running time algorithm to find the maximum value of a[j] - a[i], where j ≥ i.  

_answer:_  

2. Suppose that you have an n-story building and plenty of eggs. Suppose also that an egg is broken if it is thrown off floor f or higher, and unbroken otherwise. Devise a strategy to determine the value of f such that the number of dropped eggs is minimized.  

_answer:_  

# Exercise 3

##Below is the the pseudo-code for the Quicksort algorithm:

    function quicksort(array)
    if length(array) <= 1
       return array  
       select and remove a pivot element pivot from array  
       create empty lists less and greater  
       for each x in array  
       if x <= pivot then append x to less  
       else append x to greater  
       return concatenate(quicksort(less), list(pivot), quicksort(greater))    

   1. Suppose we implement quicksort so that the pivot is always chosen to be the first element of the array. What is the running time of this algorithm on an input array that is already sorted? Why?  
   _answer:_  

   2. Suppose we implement quicksort so that the pivot is always magically chosen to be the median element of the array. What is the running time of this algorithm? Why?  

   _answer:_  





