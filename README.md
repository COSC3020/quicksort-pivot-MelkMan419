[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/IF3rQO50)
# Quicksort Pivots

in the lectures I only briefly mentioned strategies for determining a good pivot
for quicksort. The implementation on the slides simply picks the leftmost
element in the part of the array that we consider as a pivot. I also mentioned a
few other ways of picking a good pivot, e.g. randomly.

Median-of-three is also a good way of picking a pivot -- inspect the first,
middle, and last elements of the part of the array under consideration and
choose the median value. Using the probabilities for picking a pivot in a
particular part of the array (in the same way as we did on slide 34), argue
whether this method is more or less (or equally) likely to pick a good pivot
compared to simply choosing the first element. Assume that all permutations are
equally likely, i.e. the input array is ordered randomly.

Your answer must derive probabilities for choosing a good pivot and
quantitatively reason with them.

Add your answer to this markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

Choosing the first element as the pivot:
If we choose the first element as the pivot, it will be a good pivot only if it falls within the middle n/2 elements when the array is sorted.
With probability 1/2, the first element will be from the middle n/2 elements.
Therefore, the probability of choosing a good pivot by selecting the first element is 1/2.

Using the median-of-three method:
We select the median value among the first, middle, and last elements as the pivot. To have a good pivot using the median-of-three method, at least two out of the three elements need to fall within the middle n/2 elements. The probability that the first element is from the middle n/2 elements is 1/2. If the first element is from the middle n/2 elements, the probability that the last element is also from the middle n/2 elements is 1/2. If the first element is from the middle n/2 elements and the last element is also from the middlen/2 elements, then the middle element must also be from the middle n/2 elements for the pivot to be good. So the proabability is actually (1/2)(1/2)=1/4

So comparing the probabilities, we can see that the median-of-three method has a lower probability of selecting a good pivot (1/4) compared to choosing the first element with a probability of (1/2). 
