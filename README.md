# AI_Asn3# Chess Agents – Minimax vs Alpha-Beta

This repository contains:

- **`AI_Asn3.ipynb`**  
  Jupyter notebook implementing Minimax and Alpha-Beta pruning search on a Chess environment (`gym-chess`). The notebook:
  - Loads a sample position in FEN.
  - Runs Minimax and Alpha-Beta (depth = 3), printing root evaluation, computation time, and best move.
  - Generates SVG board snapshots and converts them to PNG inline.
  - Plots timing vs search depth and nodes expanded vs depth.
  - Summarizes and compares performance.

- **`AI_Asn3.pptx`**  
  PowerPoint slides summarizing the algorithms, evaluation function, and performance comparison.
  https://docs.google.com/presentation/d/1mTXO4u6qXLw7UTjc7x-EzhEk64uQLQpdwpBdoohpyiM/edit?usp=sharing

## Requirements

- Python 3.7+  
- `gym-chess`  
- `python-chess`  
- `cairosvg`  
- `imageio`  
- `Pillow`  
- `matplotlib`

Install with:
```bash
pip install gym-chess python-chess cairosvg imageio Pillow matplotlib
```

## Usage

### Notebook

1. Open `AI_Asn3.ipynb` in Jupyter or Google Colab.
2. Run all cells to execute the algorithms and view plots.

### Presentation

- Open `AI_Asn3.pptx` in PowerPoint (or compatible viewer).

## Evaluation Function

## Evaluation Function

- **Material Heuristic**
  - Pawn: 1
  - Knight: 3
  - Bishop: 3
  - Rook: 5
  - Queen: 9
  - King: 0

- **Game-Over Overrides**
  - **Checkmate:** +9999 if you deliver mate; –9999 if you are mated
  - **Draw/Stalemate/Insufficient Material:** 0

- **Color Sign**
  Sum **+value** for your pieces, **–value** for opponent’s  
  - Positive → agent ahead  
  - Negative → opponent ahead  

- **Overall Score**
  - > 0 → White (if agent=White) ahead  
  - = 0 → Equal  
  - < 0 → Black ahead

