# CATALOG




To find the constant term c of the polynomial given the roots in the specified format, we will follow these steps:

Read the Test Case (Input):

Parse the JSON input to extract the number of roots n, the minimum number of roots required k, and the roots themselves.
Each root is represented as an object with a key x and a value y encoded in a specific base.
Decode the Y Values:

Convert the encoded y values to their decimal equivalents.
Find the Secret (C):

Use Lagrange interpolation to find the polynomial that passes through the given points.
Extract the constant term c from the polynomial.
Let's start with the given test case:

{
  "keys": {
    "n": 4,
    "k": 3
  },
  "1": {
    "base": "10",
    "value": "4"
  },
  "2": {
    "base": "2",
    "value": "111"
  },
  "3": {
    "base": "10",
    "value": "12"
  },
  "6": {
    "base": "4",
    "value": "213"
  }
}
Step 1: Read the Test Case (Input)
n=4
k=3
Roots:
Root 1: x=1, y=4 (base 10)
Root 2: x=2, y=111 (base 2)
Root 3: x=3, y=12 (base 10)
Root 6: x=6, y=213 (base 4)
Step 2: Decode the Y Values
So, the decoded roots are:

(1,4)
(2,7)
(3,12)
(6,39)
Since k=3, we only need any 3 of these points to find the polynomial. Let's use the first three points: (1,4), (2,7), and (3,12).

Step 3: Find the Secret (C)
We use Lagrange interpolation to find the polynomial P(x) that passes through these points. The Lagrange interpolation formula is:

The constant term c is 3.

Thus, the secret c is:
3
