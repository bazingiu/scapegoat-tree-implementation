# 🌳 Scapegoat Tree Implementation

[![C++](https://img.shields.io/badge/Language-C%2B%2B-blue.svg)](https://isocpp.org/)
[![Academic Project](https://img.shields.io/badge/Course-Algorithms-orange.svg)](#)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## 📌 Project Overview
An implementation of a **Scapegoat Tree**, a self-balancing binary search tree. Unlike other balanced trees such as Red-Black or AVL trees, the Scapegoat Tree does not require storing extra information (like colors or heights) in every node, making it exceptionally memory-efficient.

This project was developed for the **Algorithms** course (A.Y. 2020/2021) at the University of Catania.

### 🔬 Key Features
* **Self-Balancing Logic**: Employs the "scapegoat" concept to rebuild unbalanced subtrees only when necessary.
* **Performance**: Guarantees a worst-case amortized time complexity of $O(\log n)$ for insertion and deletion operations.
* **Memory Efficient**: Minimal node structure without the overhead of balancing metadata.

---

## 📁 Repository Structure
The project is organized as follows:

* **`Scapegoat-Tree.cpp`**: Complete C++ source code of the data structure.
* **`Scapelgoat tree documentation.pdf`**: Detailed technical report including complexity analysis and performance testing.
* **`Scapelgoat tree documentation.zip`**: Source files for the documentation (LaTeX/Assets).

---

## 📖 Theoretical Insights
A Scapegoat Tree relies on a balancing parameter $\alpha$ (typically ranging from $0.5$ to $1$). A node is considered unbalanced if:

$$\text{size}(\text{child}) > \alpha \cdot \text{size}(\text{node})$$

When this condition is violated during an insertion, the algorithm traverses up the tree to find the **"scapegoat"** (the first unbalanced ancestor) and rebuilds that specific subtree into a perfectly balanced state.



---

## 🛠️ How to Use
To compile and run the project:

```bash
g++ -O3 Scapegoat-Tree.cpp -o ScapegoatTree
./ScapegoatTree
