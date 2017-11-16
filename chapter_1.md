### Algorithm Overview
- **algorithm** - a well defined computational procedure that takes some value or a set of values as input and produces some value or set of values as an output.
  - an algorithm is **_correct_** if, for every input instance it halts with the correct output.
  - typically algorithms are chosen to be efficient, which usually refers to speed - AKA, how long it takes an algorithm to produce a result.
  - an algorithm is **_NP-complete_** if no _efficient_ solution is known, but nobody has ever proven that an efficient solution does not exist.
    - EX: Traveling Salesman Problem

- **data structure** - a way to store and organize data in order to facilitate access and modifications.

- **parallelism** - When multiple cores on a computer are used to perform more computations per second, increasing speed and functionality.

-------
### Efficiency

- there are two major limiting factors for computing algorithms - _speed_ and _memory_.

    ##### Sort Types
    - **insertion sort** - time ~ cn<sup>2</sup>,

    > where  `c = is a constant` and ` n = number of items`

    - **merge sort** - time ~ cn * log<sub>2</sub>n

  Insertion sort typically has a smaller value of c than merge sort, so typically it runs faster than merge sort.

  However, after the value of n becomes large enough, merge sort _surpasses_ insertion sort in speed, as lg<sub>2</sub>n is a much smaller factor than n.

  Thus no matter how much smaller the constant in insertion sort is, there will always be a point at which merge sort becomes the faster sort method.
