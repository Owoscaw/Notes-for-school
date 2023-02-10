Standard searching and [[Sorting algorithms|sorting]] algorithm [[Big O notation]] (worst case):
\> Linear search $O(n)$
\> Binary search $O(log\,n)$
\> Searching balanced binary tree $O(log\,n)$
\> Searching unbalanced binary tree $O(n)$
\> Bubble sort $O(n^2)$
\> Merge sort $O(n\,log\,n)$

# Searching:

## Linear search:

The only systematic way of searching in unstructured, unordered data. Each element in a set is examined sequentially, one after the other. On average, it will take $n/2$ examinations to find an element.
\> Worse case $n$
\> Average case $n/2$
\> Best case $1$
```python

#worst case steps: n + 3
#big O(n)
def linearSearch(listOfNames, name):

	#3 assignments out of a loop +3 times
	index = -1
	i = 0
	found = False

	while i < len(listOfNames) and not found:
		if listOfNames[i] == name:

			#2 assignments when we find it
			index = i
			found = True
		else:

			#1 assignment in while loop that runs len(listOfNames) times
			#n times
			i = i + 1
	return index
```

## Binary search:

Binary search is a very efficient way of searching ordered data in a list. The midpoint of the list is examined. If the midpoint is larger than the searching item, the lower half of the list is considered. If the midpoint is smaller than the searching item, the upper half of the list is considered. This is repeated until the index of the searching item is found. Every time the midpoint is examined, half of the data set is removed. This has order $O(log\,n)$.

# Sorting:

## Bubble sort:

Bubble sort is the simplest sorting algorithm, swapping two elements if one is bigger than the other. This has order $O(n^2)$.
```python

def bubbleSort(names):
	n = len(names)
	#n - 2 iterations
	for i in range(0, n - 2):
		#(n - 2) times ()
		for j in range(0, n - i - 2):
			if names[j] > names[j + 1]:
				swapName = names[j]
				names[j] = names[j + 1]
				names[j + 1] = swapName
```