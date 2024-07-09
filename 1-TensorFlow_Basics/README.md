# Tensors

<aside>
💡 A tensor is a generalization of vectors and matrices to potentially higher dimensions. Internally, TensorFlow represents tensors as n-dimensional arrays of base datatypes.

</aside>

- Tensors are the fundamental aspect of TensorFlow.
- They’re the main objects that are passed around and manipulated in the program.
- Each tensor represents a partially defined computation that will eventually produce a value. Each tensor has a data type and a shape (representation of the dimension of data).
- TensorFlow programs work by building a graph of Tensor objects that details how tensors are related, and running different parts of the graph allow results to be generated.
- Data types in tensor: ***float32***, ***int32***, ***string*** and others.

# Rank/Degree of Tensors

- Rank or degree of tensors mean the number of dimensions involved in the tensor.

- Rank-0 or Scalar tensor
    
    ```python
    num = tf.Variable(123, tf.int16)
    ```
    

- Rank-1 tensor

    ```python
    r1 = tf.Variable(["Test"], tf.string)
    ```

- Rank-2 tensor

    ```python
    r2 = tf.Variable([["hey", "hi"], ["namaste", "hello"]])
    ```

# Shape of Tensors

- It is the amount of elements that exist in each dimension.
    
    ```python
    >>r2.shape
    TensorShape([2, 2])
    ```
    

## Changing of Shape

- The number of elements of a tensor is the product of the sizes of all its shapes.
- Since, there are often many shapes having the same number of elements, it is convenient to change the shape of a tensor.

```python
>>tnsr1 = tf.ones([1, 2, 3])
>>tnsr1
<tf.Tensor: shape=(1, 2, 3), dtype=float32, numpy=
array([[[1., 1., 1.],
        [1., 1., 1.]]], dtype=float32)>
        
# Reshaping tnsr1 to 2 lists, 3 inside of those and each has 1 element
>>tnsr2 = tf.reshape(tnsr1, [2, 3, 1])
>>tnsr2
<tf.Tensor: shape=(2, 3, 1), dtype=float32, numpy=
array([[[1.],
        [1.],
        [1.]],

       [[1.],
        [1.],
        [1.]]], dtype=float32)>
```

# Types of Tensors

- Variable
- Constant
- Placeholder
- SparseTensor
- With the exception of `Variable` all of these tensors are immutable (their value may not change during execution).
    
    <aside>
    💡 Variable tensor is used when we want to potentially change the value of our tensor.
    
    </aside>

[Introduction to Tensors  |  TensorFlow Core](https://www.tensorflow.org/guide/tensor)


# TensorFlow Basics

- TensorFlow was developed by the **Google Brain Team** for internal Google use, but was released as open software in 2015.

## Tensors, Operations and Graphs

- In TensorFlow, tensors are the building blocks representing the data.
- They are similar to multidimensional arrays holding scalar values, vectors, matrices or higher dimensional data.
- Operations are mathematical operations performed on these tensors.
- TensorFlow builds a computational graph that defines the operations on their dependencies.

## Data Types and Constants

- TensorFlow supports various data types such as: *float32, int32, float64,* etc.
- Constants are tensors whose values cannot be changed during execution.

## Variables and Placeholders

- Variables are tensors whose values can be modified during execution, typically used for model parameters.
- Placeholders are tensors used to feed actual data into the computational graph during execution.

## Sessions and Execution

- To execute operations in TensorFlow, we need to create a session and run it within a session context.
- Session manages the execution of the graph and holds the state of variables as it is an environment for executing operations defined in a computational graph.
- Session handles the memory allocation, manages the resources (such as GPUs), and performs the actual computations.