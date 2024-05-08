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



According to the slides, the chance of picking a good pivot with the left most element is $1/2$
    This is because a good pivot would fall in the middle %50

In median of three, we get a pivot by taking the first, middle, and last element
{p1, ..., p2, ..., p3}

In this scenario, the only good pivot is p2
A = {p1, p2, p3}

the algorithm selects the middle element, so the only good pivots have p2 as the middle element
there are 6 permutations of the array A:
{p1, p2, p3}
{p1, p3, p2}
{p3, p1, p3}
{p2, p3, p1}
{p3, p1, p2}
{p3, p2, p1}

2 of these have p2 as the middle element
there is a $2/6 = 1/3$ 
$1/3 < 1/2$
therefore the leftmost element is better