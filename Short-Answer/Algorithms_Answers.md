sprint start
Add your answers to the Algorithms exercises here.

Give an analysis of the running time of each snippet of
pseudocode with respect to the input size n of each of the following:

```
a)  a = 0 ----------- O(n)
    while (a < n * n * n): --------- O(1)
      a = a + n * n --------- O(n)

      O(n) * ( O(1) + O(n) ) = O(n)
```
a) The answer is O(n). even though there are alot of n variable, at the end of the calculation the majority will either be n or 1. Elimination and common O's made me decide that all it is asking is for one variable runtime.

```
b)  sum = 0  ------------------ O(n)
    for i in range(n): ----------- O(1)
      i += 1 ----------- O(n + 1)
      for j in range(i + 1, n): ----O(1)
        j += 1 ---------- O(n + 1 )
        for k in range(j + 1, n):  ------O(1)
          k += 1 ------- O( n + 1 )
          for l in range(k + 1, 10 + k): ---------- O(1)
            l += 1 ------ O( n + 1)
            sum += 1 ------O( n + 1)

            sum(n) * ( 1 + n + 1 ) * ( 1 + n + 1) * ( 1 + n + 1) * ( 1 + n ) * sum(n)
            n * n * n * n
            O(n^4)
```
b) Answer is O(n^4), this is because each loop is exactly the same so times itself(4), with the last loop changing the sum, which is still a basic n.

```
c)  def bunnyEars(bunnies): -------- O(n)
      if bunnies == 0: ------------ O(n)
        return 0 --------------- O(1)

      return 2 + bunnyEars(bunnies-1) -------- n + ( n * (n - 1) ) = O(n)

      function(n) * ( n + 1 ) * return(n)
      function(n) = return (n + function(n(n))) 
      function(n) = n + function(n) 
      O(n)
      
```
c) Answer is 0(n). It took me second to think about this one because it is encapsulating itself, meaning everything is being reduced to the same variable. Even though it expands and there are multiple n's, its still within a main code block that is looking for one solid answer reusing its variables.