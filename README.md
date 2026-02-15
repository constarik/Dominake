# 🐍 Dominake — Domino Snake Puzzle

An original puzzle game where you divide a number grid into dominoes and chain them into a continuous snake.

**▶ [Play Now](https://constarik.github.io/Dominake/)**

## How to Play

1. **Place dominoes** — Drag between two adjacent cells to form a domino pair
2. **Connect the chain** — Click gray marks between dominoes to toggle chain links
3. **Match values** — Where dominoes connect, touching values must match (yellow = match, red = mismatch)
4. **Complete the snake** — All unique dominoes placed + N−1 matching links = win!

## Features

- **3 Grid Sizes**: 4×5 (10 dominoes), 6×7 (21 dominoes), 8×9 (36 dominoes)
- **3 Difficulty Levels**: Easy, Normal, Hard — based on trap count (false matches that mislead)
- **6 Color Themes**: Default, Ocean, Forest, Sunset, Sand, Light
- **Interactive Tutorial**: Step-by-step guide with visual examples
- **Mobile Optimized**: Touch controls, responsive layout
- **Single HTML File**: No dependencies, runs anywhere

## Mathematical Background

The game uses Hamiltonian paths on grid graphs and Eulerian paths on complete graphs K_n. Valid grid sizes must satisfy the Eulerian path constraint: K_n with even vertex degrees requires odd n, giving grids n×(n+1) for n ∈ {4, 6, 8, ...}.

Difficulty is measured by **traps** — adjacent cells between different dominoes that share the same value but aren't part of the solution chain. More traps = more false leads = harder puzzle.

## Tech

- Pure HTML/CSS/JavaScript, single file (~420 lines)
- Mulberry32 PRNG for reproducible generation
- Warnsdorff's heuristic for Hamiltonian path generation
- Backtracking chain builder with iteration limits
- GitHub Pages deployment via `/docs`

## Author

**Constantin Pgk** — Slot mathematician & game developer  
Part of the [Uncloned Math](https://unclonedmath.com) portfolio

## License

MIT
