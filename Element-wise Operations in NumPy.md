## Element-wise Matrix Operations

The same functions and operators that work with scalars and matrices also work with other dimensions. You just need to make sure that the items you perform the operation on have compatible shapes.

Let's say you want to get the squared values of a matrix. That's simply `x = m * m`(or if you want to assign the value back to `m`, it's just `m *= m`

This works because it's an element-wise multiplication between two identically-shaped matrices. (In this case, they are shaped the same because they are actually the same object.)

Here's the example from the video:

```
  a = np.array([[1,3],[5,7]])
  a
  # displays the following result:
  # array([[1, 3],
  #        [5, 7]])

  b = np.array([[2,4],[6,8]])
  b
  # displays the following result:
  # array([[2, 4],
  #        [6, 8]])

  a + b
  # displays the following result
  #      array([[ 3,  7],
  #             [11, 15]])

```

