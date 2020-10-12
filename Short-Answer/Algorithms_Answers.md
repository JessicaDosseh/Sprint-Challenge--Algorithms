#### Please add your answers to the **_Analysis of Algorithms_** exercises here.

## Exercise I

a)

Time Complexity O(n):

- This is a linear time complexity because the operation is being performed n number of times (looping).

Space complexity O(1):

- This is a constant time complexity because additional memory is not being used.

b)

Time Complexity O(n^2)

- This is a quadratic time complexity because of the nested loop

Space complexity O(1)

- This is a constant time complexity because additional memory is not being used.

c)

Time Complexity O(n)

- This is a linear time complexity because the function is called recursively n times before it reaches its base case

Space complexity O(n)

- This is a linear time complexity because the function makes n calls to the stack

## Exercise II

**Visualization:**

- **Array view**

[ 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13 ]

- [ ] Given ^ this array find the midpoint
- [ ] If it's a decimal round up

[ 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13 ]
--------------------|(break)

- [ ] pevIndex = None
- [ ] newIndex = 7
- [ ] Drop an egg.
- [ ] If it breaks than find the midpoint of the lower subset

[ 1, 2, 3, 4, 5, 6 ]
-----------|(break)

- [ ] pevIndex = 7
- [ ] newIndex = 4
- [ ] Repeat
      Drop an egg.
      If it breaks than find the midpoint of the lower subset

[ 1, 2, 3]
-----|(safe)

- [ ] pevIndex = 4
- [ ] newIndex = 2
- [ ] Drop an egg.
- [ ] If it does not breaks than find the midpoint of the upper subset

[ 2, 3 ]
-----|(break)

- [ ] pevIndex = 2
- [ ] newIndex = 3
- [ ] Drop an egg.
- [ ] If it breaks than find the midpoint of the lower subset

[ 2 ]
--|(safe)

- [ ] pevIndex = 3
- [ ] newIndex = 2
- [ ] Because there is only one value left and it is safe we know that the pevIndex value is floor f because the problem says that - "Suppose also that an egg gets broken if it is thrown off floor f or higher" and pevIndex is the lowest index were the egg breaks.

- **Time and Space Complexity**

Time Complexity O(log(n))

- Based on n floors, this is a logarithmic time complexity because the function splits the array in half every time. (this does not include other potential factors)

> The pace complexity will depend on whether the problem is solved in place or if it is not in place.

- Space complexity O(1) if no other data structures are used besides the array.

- Space complexity O(n) if the function uses other data structures (i.e., recursion)
