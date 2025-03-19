# Algorithm to count intersecting chord pairs in O(nlogn) time
Chord Intersection Algorithm
Overview
This repository contains a O(n log n) algorithm for counting the number of intersecting chord pairs on a circle. Given n chords on a circle, each defined by its endpoints, the algorithm determines how many pairs of chords intersect inside the circle.

# Problem Statement
Consider n chords on a circle, each defined by its endpoints. The problem is to determine the number of pairs of chords that intersect inside the circle.
## For example:

If the n chords are all diameters that meet at the center, then the correct answer is n(n-1)/2.
We assume that no two chords share an endpoint.

# Algorithm
The algorithm uses a clever transformation of the problem into counting inversions in a sequence, which can be done efficiently using a merge sort approach:

<p> 1. Map each endpoint on the circle to its corresponding chord index </p>
<p> 2. Sort all endpoints in clockwise order around the circle </p>
<p> 3. Create a sequence where each position contains the corresponding chord index </p>
<p> 4. Record the position of the first occurrence of each chord index </p>
<p> 5. Create a reduced sequence containing only the positions of first occurrences </p>
<p> 6. Count inversions in this reduced sequence using merge sort </p>

The number of inversions in the reduced sequence equals the number of intersecting chord pairs.

# Time Complexity

<p> O(n log n) time complexity where n is the number of chords
<p> O(n) space complexity

# Usage
To use this algorithm in your project:
<p> 1. Clone this repository </p>
<p> 2. Import the: "count_chord_intersections" function </p>

