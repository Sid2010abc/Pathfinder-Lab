# Pathfinder Lab

Pathfinder Lab is a sandbox for comparing graph search algorithms on user-defined maps, covering one of the most broadly applicable problems in computer science: finding an efficient path between two points given a set of constraints.

The map itself is entirely user-drawn using a brush tool, and start and goal nodes can be placed anywhere on it. Six classic search algorithms are implemented and run against the resulting grid graph, making their theoretical differences directly observable:

- Breadth-first search expands uniformly outward, guaranteeing shortest path on an unweighted grid at the cost of exploring a large search space.
- Dijkstra's algorithm generalizes this to weighted terrain, always expanding the lowest-cost frontier node next.
- A* adds a heuristic function (commonly Euclidean or Manhattan distance to the goal) to Dijkstra's approach, biasing the search toward the goal and typically exploring far fewer nodes while still guaranteeing optimality when the heuristic is admissible.
- The remaining algorithms round out the comparison with different tradeoffs between completeness, optimality, and exploration efficiency.

Because the map is fully custom, you can construct mazes, bottlenecks, open terrain, or adversarial worst-case layouts to stress-test how each algorithm's assumptions hold up.

Features:
- Freeform map drawing with a brush tool
- Movable start and goal points
- Six pathfinding algorithms available for direct, simultaneous comparison
- Real-time visualization of frontier expansion, not just the final path

Tech: single self-contained HTML file, vanilla JavaScript, no build step, no dependencies beyond Google Fonts.

Usage: open `PathfinderLab.html` in a browser. Draw obstacles with the brush, place start and goal, and run one or more algorithms to compare their search behavior.
