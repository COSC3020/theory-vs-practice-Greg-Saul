[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/FgMJElkj)
# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.
  

- Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.


- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.

Add your answers to this markdown file.

1a) The biggest issue with asymptotic analysis is that any constant factors are ignored. we could have a complexity of 1000000(n) and all that would be looked at is $O(n)$ for example. this becomes an issue when another algorithms true analysis is just n for O(n).

1b) The hardware that is being used can change the runtime because different computers have different amounts of ram or cores. This is a factor that the asymptotic analysis can't account for because the algorithm will be the same.

1c)  Different methods of compares that are used can make a big difference be a factor that asymptotic analysis doesn't account for. For example in 2030 we learned that while == and string.compare() in c++ have the same output, string.compare() produces a much faster process. If there were two functions, and one used == and the other used the .compare(), they would have the same analysis but likely have different true runtimes.

2a) we know that the time complexity for a binary search tree is $log_2 (n)$ with n being the number of nodes. that being said, we can use a simple proportion to find the time. $log_2 (1000) = 9.97$ and $log_2 (10000) = 13.29$ this implies that we can set up a proportion $9.97/5 = 13.29/x$ => $(13.29 * 5)/ 9.97 = 6.66$ this shows that 10,000 elements of the same datatype would take 6.66 seconds.

3a) The hardware that is used has the potential to make a big difference in the time that it takes to run. Maybe the 1000 element data set was run on a modern computer and the 10000 element data set was run on a computer made in 1995. This would almost certainly slow down the time that it takes to search.

3b) the data type also could have an effect on the runtime. if the set of 1000 was trying to find numbers and just had to compare numbers and the set of 10000 had strings, then the set of 10000 would take significantly longer because string compares are more complicated and take more time than number compares.

3c) If the computer had other programs running in the background then the time could be slowed down a lot. A computer that has 100% of its resources would run the algorithm faster than if I was playing fortnite and trying to run the algorithm at the same time.




#### Help used
Zach Renz gave a hint by pointing out that not all datasets have the same data type and not all computers run at the same speed

used https://github.com/COSC3020/theory-vs-practice-AaronATM to help me with 1c
