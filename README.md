# Algorithm-to-count-intersecting-chord-pairs-in-O-n-log-n-time
Chord Intersection Algorithm
Overview
This repository contains a O(n log n) algorithm for counting the number of intersecting chord pairs on a circle. Given n chords on a circle, each defined by its endpoints, the algorithm determines how many pairs of chords intersect inside the circle.
Problem Statement
Consider n chords on a circle, each defined by its endpoints. The problem is to determine the number of pairs of chords that intersect inside the circle.
For example:

If the n chords are all diameters that meet at the center, then the correct answer is n(n-1)/2.
We assume that no two chords share an endpoint.

Algorithm
The algorithm uses a clever transformation of the problem into counting inversions in a sequence, which can be done efficiently using a merge sort approach:

Map each endpoint on the circle to its corresponding chord index
Sort all endpoints in clockwise order around the circle
Create a sequence where each position contains the corresponding chord index
Record the position of the first occurrence of each chord index
Create a reduced sequence containing only the positions of first occurrences
Count inversions in this reduced sequence using merge sort

The number of inversions in the reduced sequence equals the number of intersecting chord pairs.
Time Complexity

O(n log n) time complexity where n is the number of chords
O(n) space complexity

