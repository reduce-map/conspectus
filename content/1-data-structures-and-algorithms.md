# Algorithmics: Fundamentals

- [Data Structures and Algorithms in JavaScript, big respect to trekhleb](https://github.com/trekhleb/javascript-algorithms)
  - [Data Structures](https://github.com/trekhleb/javascript-algorithms?tab=readme-ov-file#data-structures)
  - [Algorithms](https://github.com/trekhleb/javascript-algorithms?tab=readme-ov-file#algorithms)
- [TheAlgorithms](https://github.com/TheAlgorithms)
  - [TheAlgorithms/Python](https://github.com/TheAlgorithms/Python)
  - [TheAlgorithms/TypeScript](https://github.com/TheAlgorithms/TypeScript)

## Time Complexity
- **O(1)**: Constant Time - The algorithm executes in fixed time, regardless of the input data size.
  - *Example*: Accessing an array element by index.
  - *Explanation*: Since an array allows direct access to its elements, accessing any element by index always takes the same amount of time.

- **O(log n)**: Logarithmic Time - Execution time increases logarithmically with the increase in input data size.
  - *Example*: Binary search.
  - *Explanation*: In binary search, the size of the problem is halved with each step, so the total number of steps depends on the logarithm of the input size.

- **O(n)**: Linear Time - Execution time increases linearly with the increase in input data size.
  - *Example*: Traversing an array.
  - *Explanation*: Each element of the array is checked once, so the execution time is directly proportional to the number of elements.

- **O(n log n)**: Linearithmic Time - Execution time increases linear-logarithmically as the size of the input data grows.
  - *Examples*: Merge sort, quicksort.
  - *Explanation*: These algorithms combine linear traversals with logarithmic reductions of the problem using divide and conquer.

- **O(n^2)**: Quadratic Time - Execution time increases proportionally to the square of the input data size.
  - *Example*: Bubble sort.
  - *Explanation*: Each element is compared with every other element, hence the number of comparisons is quadratic relative to the number of elements.

- **O(n^3)**: Cubic Time - Execution time increases proportionally to the cube of the input data size.
  - *Example*: Floyd's algorithm for finding all shortest paths.
  - *Explanation*: The algorithm checks all possible pairs of vertices, and for each pair, it performs a check through all other vertices.

- **O(n^k)**: Polynomial Time - Execution time increases as a polynomial of degree \(k\) of the input data size.
  - *Example*: Algorithms for processing graphs.
  - *Explanation*: Depending on the complexity of the graph and operations, the time may vary, but overall increases polynomially.

- **O(2^n)**: Exponential Time - Execution time increases exponentially with the increase in input data size.
  - *Example*: Algorithms for solving problems by brute force.
  - *Explanation*: The number of possible configurations increases exponentially, requiring the enumeration of a large number of variants.

- **O(n!)**: Factorial Time - Execution time increases proportionally to the factorial of the input data size.
  - *Example*: Complete enumeration of permutations.
  - *Explanation*: The number of all possible permutations of \(n\) elements is \(n!\), so algorithms that require enumeration of all permutations operate in factorial time.
