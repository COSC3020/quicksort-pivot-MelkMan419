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
With the median-of-three method, we inspect the first, middle, and last elements, and choose the median value as the pivot.
The pivot will be a good pivot if it falls within the middle n/2 elements when the array is sorted. If the array is randomly ordered, the probability of the first, middle, and last elements being from the middle n/2 elements is 1/2 each.
To have a good pivot using the median-of-three method, at least two out of the three elements need to fall within the middle n/2 elements.
The probability of having two or more elements from the middle n/2 elements among the first, middle, and last elements is given by the complement of the probability of having only one or fewer elements from the middle n/2 elements, which is:
P(two or more good elements)=1−P(one or fewer good elements)
The probability of having one or fewer good elements among the three is:
P(one or fewer good elements)=P(none good)+P(exactly one good)
The probability of none of the elements being good (falling within the middle n/2 elements) is (1/2)×(1/2)×(1/2)=1/8.
The probability of exactly one element being good is(3/1)×(1/2)×(1/2)×(1/2)=3/8 since there are 3 ways to choose one good element out of 3.
Therefore, P(one or fewer good elements)=1/8+3/8=1/2.
Thus, P(two or more good elements)=1−1/2=1/2.

So, both methods, choosing the first element and using the median-of-three method, have the same probability, 1/2, of picking a good pivot.
