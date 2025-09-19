# Plant-pollination
Plant pollination and evolution study

🧩 How the model works

Pollinator preference vector

Example: [0.58, 0.26, 0.28]

This says: the pollinator (could be a bee, fly, ant, bat, etc.) prefers trait 1 strongly, trait 2 and 3 less.

Traits could be color, nectar amount, flower shape (we didn’t name them yet).

Plant population

Each plant has its own traits (numbers).

Example: [0.70, 0.34, 0.32].

Fitness function

Measures how close plant traits are to pollinator preferences.

Closer match = better pollination success = higher fitness.

Genetic algorithm loop

Generate many plants → evaluate their fitness → keep the best → mutate a little → repeat.

Over generations, the plants evolve traits closer to what the pollinator “wants.”

✅ What you saw

Plants started random.

After some generations, the best plant traits matched the pollinator preferences much better.

The fitness progression showed the population adapting.

⚠️ Important

This is not yet real-world pollination data (ants, bees, etc.).
It’s a simulation framework that we can later feed with:

Pollinator preference data (e.g., bees prefer blue/purple flowers, ants prefer ground-level flowers, bats prefer nocturnal scent, etc.).

Real plant traits datasets.
