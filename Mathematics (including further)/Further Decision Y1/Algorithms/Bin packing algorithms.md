Bin packing is its own class of problems. The easiest is to imagine stacking boxes of a fixed width $a$ and length $b$ with a varying height into bins of width $a$ and length $b$ using the minimum amount of bins. Similar problems exist for many scenarios in everyday life. There are three bin packing algorithms used, first-fit, first-fit-decreasing, and full-bin. It is often useful to find a lower bound first by dividing the size of the bins by the total size of all the boxes:
$$\Huge lower\,\,bound =\frac{bin\,\,size}{\sum box\,\,sizes}$$
The first-fit algorithm works by considering items in the order they are given:
\> Take the items in the order they are given
\> Place each item in the first availible bin starting from bin 1 every time

The first-fit-decreasing algorithmis identical to the first-fit algorithm but requires the items to be sorted in descending order first:
\> Sort items into descending order, using [[Bubble sort]] or [[Quick sort]].
\> Apply the first-fit algorithm

The full-bin algorithm required the inspection of each bin to select items that will combine to fill bins:
\> Use observation to find combinations of items that will fill a bin, pack these first
\> Any remaining items are packed using the first-fit algorithm
