The order of an algorithm describes its complexity. An algorithm's order tells you how changes in the size of a problem affect the approximate time taken for its completion (run time). The order of an algorithm can be described as a function of its size. If an algorithm has order $f(n)$, then increasing the size of the problem from $n$ to $m$ will increase the run time of the algorithm by a factor of approximately $\frac{f(m)}{f(n)}$.

For the [[Sorting algorithms|bubble sort]], most of the steps are to do with making comparisons between pairs of numbers. If a list has $n$ numbers, then the first pass required $(n-1)$ comparisons. Assuming some swaps were made, the second pass requires $(n-2)$ comparisons. In the worst case, this continues until $(n-(n-1))$ comparisons are made on the final pass. This means that the total number of comparisons made will be $(n-1)+(n-2)+(n-3)+\dots+(n-(n-3)+(n-(n-2))+(n-(n-1))$ comparisons in total. This can be written:
$$\Huge \sum_{r=1}^{n}r=\frac{n}{2}(n+1)=\frac{n^{2}+n}{2}$$
Since this contains a quadratic expression, the algorithm is considered to have quadratic order. This means that for a size increase of a problem by factor $k$, the algorithm will take approximatley $k^{2}$ times as long to complete.

Some common orders for algorithms are:
\> Linear, $k$
\> Quadratic, $k^{2}$
\> Cubic, $k^{3}$
\> Exponential, $n^{k}$
