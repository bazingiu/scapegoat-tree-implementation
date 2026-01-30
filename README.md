# 🌳 Scapegoat Tree Implementation

[![C++](https://img.shields.io/badge/Language-C%2B%2B-blue.svg)](https://isocpp.org/)
[![Academic Project](https://img.shields.io/badge/Course-Algorithms-orange.svg)](#)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## 📌 Project Overview
Implementazione di uno **Scapegoat Tree** (Albero Capro Espiatorio), una struttura dati di ricerca binaria auto-bilanciante. A differenza di altri alberi come i Red-Black o gli AVL, lo Scapegoat Tree non richiede di memorizzare informazioni extra (come colori o altezze) in ogni nodo, rendendolo estremamente efficiente in termini di memoria.

Il progetto è stato realizzato per il corso di **Algoritmi** (A.A. 2020/2021) presso l'Università di Catania.

### 🔬 Key Features
* **Self-Balancing Logic**: Utilizza il concetto di "capro espiatorio" per ricostruire sottoalberi sbilanciati solo quando necessario.
* **Performance**: Garantisce una complessità temporale ammortizzata di $O(\log n)$ per le operazioni di inserimento e cancellazione.
* **Memory Efficient**: Struttura dei nodi minimale senza overhead aggiuntivo.

---

## 📁 Repository Structure
Il progetto è organizzato come segue:

* **`Scapegoat-Tree.cpp`**: Codice sorgente C++ completo dell'implementazione.
* **`Scapelgoat tree documentation.pdf`**: Relazione tecnica dettagliata con analisi della complessità e test di performance.
* **`Scapelgoat tree documentation.zip`**: File sorgente della documentazione (LaTeX/Assets).

---

## 📖 Theoretical Insights
Uno Scapegoat Tree si basa su un parametro di bilanciamento $\alpha$ (tipicamente tra $0.5$ e $1$). Un nodo si definisce sbilanciato se:
$$\text{size}(\text{child}) > \alpha \cdot \text{size}(\text{node})$$
Quando questa condizione viene violata durante un inserimento, l'algoritmo risale l'albero per trovare lo "scapegoat" (il primo antenato sbilanciato) e ricostruisce quel sottoalbero in modo perfettamente bilanciato.

---

## 🛠️ How to Use
Per compilare ed eseguire il progetto:

```bash
g++ -O3 Scapegoat-Tree.cpp -o ScapegoatTree
./ScapegoatTree
