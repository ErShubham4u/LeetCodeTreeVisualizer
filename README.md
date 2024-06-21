# Binary Tree Visualization

This repository contains a simple JavaScript implementation to visualize a binary tree on a web page. The project uses HTML, CSS, and JavaScript to create an interactive canvas where users can input binary tree structures and see them rendered visually.

## Files and Structure

1. **BinaryTreeNode.js**: This file defines the `BinaryTreeNode` class, which represents a node in a binary tree. Each node has a value, and pointers to its left and right children. The class also includes methods to set the left and right children and to calculate the height of the tree.

2. **drawBinaryTree.js**: This script handles the logic for drawing the binary tree on a canvas element. It includes functions to initialize the canvas, calculate the required dimensions for the tree, and recursively draw the nodes and edges connecting them.

3. **index.html**: This file contains the HTML structure of the application. It includes a textarea for inputting the tree structure, buttons to apply the input or clear the canvas, and a canvas element where the tree is drawn.

4. **treeUtils.js**: This utility file includes functions for various tasks such as calculating the required height and width for the canvas, drawing nodes and edges, and constructing the tree from input data. It also defines some default configuration values for the drawing, such as node radius and spacing.

## Usage

To use this application, open `index.html` in a web browser. The user interface allows you to input a binary tree structure in a specific format and visualize it on the canvas. 

1. **Input Format**: The binary tree should be represented as a comma-separated list of values. Use "null" for absent children. For example: `1,2,3,null,null,4,5`.
   
2. **Buttons**:
   - **Apply**: Parses the input and draws the binary tree on the canvas.
   - **Clear**: Clears the input and the canvas.

## Algorithm

The primary algorithm used in this project is the **Breadth-First Search (BFS)** for constructing the binary tree from the input string. Here's a detailed breakdown:

1. **Parsing Input**: The input string is parsed and split into an array of values. "null" values are used to represent absent children.

2. **Tree Construction (BFS)**:
   - A queue is used to construct the tree level by level.
   - The root node is created from the first value in the array and added to the queue.
   - Iteratively, each node is dequeued, and its left and right children are created from the subsequent values in the array and added to the queue.
   
3. **Tree Drawing**:
   - The dimensions of the canvas are calculated based on the height and width of the tree.
   - Nodes are drawn on the canvas using their calculated positions.
   - Edges are drawn to connect parent nodes with their left and right children.

## Configuration

The drawing configurations can be adjusted in `treeUtils.js`:

- **Radius**: The radius of the node circles.
- **Node Spacing**: The horizontal and vertical spacing between nodes.
- **Font Size**: The size of the text inside the nodes.

## Example

Here is an example input and its corresponding binary tree visualization:

- **Input**: `1,2,3,null,null,4,5`
- **Tree Structure**:

  1
 / \
2   3
   / \
  4   5


## License

This project is open-source and available under the MIT License.

## Author

Developed by Shubham Kumar.
