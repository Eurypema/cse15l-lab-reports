# Part 1

### Student:

I've written a Java program to calculate factorials, but it's giving me negative values for inputs greater than 20. 
![image](https://github.com/Eurypema/cse15l-lab-reports/assets/103284133/ce5e0476-3aff-4079-9c5a-20c8472f994c)
![image](https://github.com/Eurypema/cse15l-lab-reports/assets/103284133/c2e5c0c5-c723-4116-a4d9-868e767e2a0f)

### TA:
It seems like you're running into integer overflow. The int type has a maximum value of 2^31-1. For factorials, this limit is easily exceeded. Can you try using a long type instead of int in your factorial method and see if that fixes the issue for larger numbers?

### Student:

I changed the data type to long, and now it works correctly for 20! But for even larger numbers, it still gives wrong answers, like 200! = 0. Is there a limit to long as well?

![image](https://github.com/Eurypema/cse15l-lab-reports/assets/103284133/8a40b5a1-dd00-4d2f-a100-eede1265c4cc)

### TA:

Yes, long also has a limit, which is 2^63-1. For factorials of large numbers, this limit can be reached quickly. To handle even larger numbers, you should use BigInteger in Java, which can handle arbitrarily large integers. 

### Student:

I changed the data type to BigInteger, and it now allows for really large factorials. But the large number of trailing zeroes makes me wonder if I am still running into integer overflow.

![image](https://github.com/Eurypema/cse15l-lab-reports/assets/103284133/3d58ac22-a0bc-4bc8-9ce7-1d86817eb1bd)

### TA

This is actually expected behavior for factorial calculations, as factorials of large numbers often include many trailing zeroes. These zeroes result from the multiplication of the number 10, which is a product of 2 and 5. As factorials involve multiplying a series of consecutive integers, there are many opportunities for pairs of 2s and 5s to combine and form 10s.

# Part 2:

In the second half of this quarter, my lab experience opened my eyes to the power and flexibility of Bash scripting. Before these sessions, I had regularly encountered .sh files but never fully understood their significance or their potential in automating tasks. The hands-on practice with writing and executing Bash scripts has not only demystified this aspect of programming for me but also equipped me with a valuable tool. I now appreciate the nuances of command-line interfaces and have a newfound ability to manipulate files and directories and automate repetitive tasks with a few lines of code. This practical skill set is something I anticipate will greatly enhance my efficiency in future software development projects.
