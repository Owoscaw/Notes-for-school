In an algorithm, the number of assignments defines how effecient an algorithm is. For example:
```python
n = 1000

#1001 assignments
sum = 0
for i in range(n):
	sum += i

#1 assignment
sum = n * (n + 1)/2
```
Big O notation describes the pattern that an algorithm will follow as the data set it is performed on increases in size, i.e. the [[Order of an algorithm|order of an algorithm]]. This is based on the amount of assignments, not operations. For example, the first algorithm above has $O(n)$, meanwhile the bottom has $O(1)$. The top algorithm increases the amount of assignments in accordance to $n$, meanwhile the bottom function is independant of $n$.

In big $O$ notation, only the dominant term (highest order) is written inside the bracket. For example, a function, $f(n) = 3n + 1$ will not be written as $O(3n + 1)$, instead it will be written as $O(n)$.

Big $O$ measures the time complexity of an algorithm, it is only an approximation as only the dominant term is conseidered.

![[big O comparison.png|500]]

## $O(1)$:
Functions with a constant order will execute with the same amount of assignments all the time, no matter the input size.

## $O(n)$:
Functions of order $n$ increase linearly in accordance to $n$. As $n$ increases, the number of assignments will increase linearly. A very common example of $O(n)$ is a single for loop, controlled by $n$:
```python
for i in range(1, n):
	print(i)
```

## $O(n^2)$:
Functions of order $n^2$ increase in accordance to $n^2$, this increases at $n$ times the speed of a $O(n)$ function. A very common example of a $O(n^2)$ algorithm is two nested for loops:
```python
for i in range(1, n):
	for j in range(1, n);
		print(i + j)
```

## $O(log\,n)$:
In big $O$ notation, only $log_2$ is considered, no other bases are needed. Divide and conquer algorithms work by halving the size of a problem at each pass. Time complexity increases very slowly as the size of $n$ increases.  

## $O(2^n)$:



# Analysing an algorithm:
```python
total = 0

#student assigned n times -> n
for student in range(1, n):

	#mark assigned 3 times per loop -> 3n
	for mark in range(1, 3):

		#total assigned 3n times -> 3n
		total = total + results[student][mark]

#student assigned n times -> n
for student in range(1, n):

	#average assigned once per loop -> n
	average[student] = (mark[1] + mark[2] + mark[3])/3

#total of all is 9n
```
In the above code, there are $n$ assignments of the student iterating variable. Per loop, Mark is assigned 3 times, and total is assigned once. This means there are 7 assignments per loop for the first for loop in the above code, i.e. $7n$.

In the bottom for loop, there are $n$ assignments of the student iterating variable. Per loop, average is assigned once, i.e. $n$ times in total. This means that the total amount of assignments in the entire algorithm is $9n$, making it $O(n)$.


# Permutation:

A permutation of $n$ items is the number of ways the items can be arranged. There are two main types of permutation, repetition allowed, and no repetition allowed. This is seen in the [[Binomial theorem|binomial theorem]].

There are $k^n$ possible ways of choosing $n$ items from a list of $k$ items, allowing repetition:
$$\Large [0-k],[0-k],...,[0-k]\,\,\,n\,\,times$$
$$\Large k\times k\times k\times ...\times k\,\,\,n\,\,times$$
$$\Large k^n$$
There are $n!$ ways of choosing a sequence of $n$ items:
$$\Large [0-n],[0-(n-1)],[0-(n-1)],...,[0-1]$$
$$\Large n\times (n-1)\times(n-2)\times ...\times 1$$
$$\Large n!$$