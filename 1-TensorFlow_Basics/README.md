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
- Session manages the execution of the graph and holds the state of variables.