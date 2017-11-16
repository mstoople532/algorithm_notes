### Insertion Sort
- *Insertion Sort* is known for being an efficient algorithm for sorting small numbers of elements, ie. a hand of cards.
- Goal: Take an array of `n` numbers and sort them so that a<sub>1</sub> < a<sub>2</sub> < ... < a<sub>n</sub>
  - the numbers in the array are also known as _**keys**_.
- *Insertion Sort* works by removing one element at a time from the preexisting array. Once removed, the element is compared to the other elements in the  array to determine its position.
- The array is sorted _**in place**_ - the elements are rearranged within the array, with at a most a constant number of them stored outside the array at any given time.
- Thus the same array contains the sorted output sequence when the procedure is completed.
- **loop invariant** - the portion of the array that has already been sorted and thus does not *change* in order.
  - Three things to demonstrate about a loop invariant
    1. **Initialization** - It is true prior to the first iteration of the loop.
    2. **Maintenance** - If it is true before an iteration of the loop, it remains true before the next iteration.
    3. **Termination** - When the loop terminates, the invariant provides a property that demonstrates the algorithm is correct.
  - Thus when the first two properties hold, the invariant is true prior to every iteration of the loop.
  - Typically to demonstrate *correctness* you use the loop invariant along with the condition that caused the loop to terminate.
- Within the the example of *Insertion Sort*, the loop terminates because the number of loops is larger than the number of elements of the array. Since the array includes all of the elements in the original array, sorted, you can conclude the algorithm is correct.
------
### Analyzing Algorithms
- Algorithms are typically analyzed to predict the resources the algorithm requires.
  - Resources such as memory, bandwith, or computer hardware are often concerns, but usually one measures computational time.
- Assume a **_RAM (Random Accesss Machine)_** model of computation unless otherwise specified for examples.
  - In a RAM model, instructions are executed one after another with no concurrent operations.
  - The RAM model contains instructions commonly found on real computers: arithmetic (ie. add, subtract, multiply, divide, remainder, floor, ceiling), data movement (ie. load, store, copy), and control (ie. conditional and unconditional branch, subroutine call, and return).
- The time taken by an algorithm generally grows with the size of the input, but the exact meaning of 'runtime' and 'size of input' can vary.
  - The best measure of **_input size_** can change depending on the problem. While in many cases input size is best measured as the number of elements in the input, in other problems it is more sensible to use the total number of bits needed to represent the input (or other options).
  - The **_runtime_** of an algorithm on an input is the number of primitive operations executed.
- In the example of *Insertion Sort*, the running time of the algorithm is the sum of the run times for each statement executed, multiplied by how many times it needs to execute (loops)
- Even for inputs of a given size, runtime may depend on *which* input of that size is given. In *Insertion Sort*, runtime is minimized when the array is already sorted, as fewer steps need to execute (fewer comparisons to other elements in the array need to be made).
- **worst-case running time** - the longest running time for *any* input of size n.
  - The worst-case runtime of an algorithm provides an upper bound, thus providing a guarantee that the algorithm will never take any longer.
  - For some algorithms, the worst case occurs fairly often. EX: when searching a database for a particular piece of information, the worst case will occur when the information is not present.
  - Often the "average case" is roughly as bad as the worst case.
- Randomized algorithms can be used to make random choices, thus allowing probabilistic analysis and yielding an *expected* running time.
- It is the **_rate of growth_** that constitutes the most important measure of running time. In *Insertion Sort*, the factor n<sup>2</sup> is more important than the factors preceding it, and the worst-case running time is `theta` * n<sup>2</sup>
- One algorithm is generally considered to be more efficient than another if its worst-case running time has a lower order of growth. However, because of constant factors/ lower order terms, an algorithm with a running time possessing a higher order of growth may still take less time than an algorithm whose running time has a lower order of growth.
----
### Designing Algorithms

- *Insertion Sort* was reflective of an **_incremental_** design approach - a single element was inserted into its proper place repeatedly, eventually yielding the sorted array.
- Another design approach, **_divide-and-conquer_** can be used to design a sorting algorithm whose worst-case running time is much less than Insertion Sort's.
- Many algorithms are **_recursive_** - to solve a given problem they call themselves recursively one or more times to deal with closely related sub-problems.
  - Usually these algorithms follow a *divide-and-conquer* approach - they break the problem into several sub-problems that are similar to the original, but smaller in size, solve the problems recursively, and then combine the solutions to create a solution to the original problem.

##### The Divide-and-Conquer Paradigm
- **Divide** - Divide the problem into a number of sub-problems that are smaller instances of the original.
- **Conquer** - Conquer the sub-problems by solving them recursively. If the sub-problem sizes are small enough, however, just solve them in  a straightforward manner.
- **Combine** - Combine the solutions to the sub-problem into the solution for the original problem.

The *Merge Sort* algorithm closely follows the Divide-and-Conquer paradigm.
 
