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

1. Pollinator syndromes (the science behind it)

Botanists have studied for decades that different pollinators prefer different floral traits. These are called pollination syndromes.

Ants 🐜

Tend to visit small, ground-level, white/pale flowers.

Flowers are often nectar-poor, since ants are inefficient pollinators (they can damage pollen with antimicrobial secretions).

Source: Peakall et al. 1990s, and reviews on "ant pollination syndrome".

Bees 🐝

Prefer blue/violet/yellow colors (they see UV patterns).

Moderate–high nectar reward.

Flower shape often tubular or bilaterally symmetrical.

Source: Kevan & Baker (1983), "Insects as flower visitors".

Bats 🦇

Visit large, pale or white night-blooming flowers with strong scents.

High nectar volumes.

Often open at night, robust structures.

Source: Fleming et al. 2009, “Bat pollination syndrome.”

These syndromes are general patterns, not absolute rules — but they’re strong enough to predict plant traits from pollinator guilds.

2. How we mapped this to the simulation

We took 3 abstract traits:

Trait 1 = Flower color brightness (0 = white, 1 = vivid/bright).

Trait 2 = Flower size (0 = tiny, 1 = large).

Trait 3 = Nectar reward (0 = none, 1 = abundant).

Then, for each pollinator, we set a preference vector based on known syndrome traits:

Ants: [0.1, 0.2, 0.2] → small, pale, low nectar.

Bees: [0.8, 0.7, 0.5] → colorful, medium/large, moderate nectar.

Bats: [0.2, 0.8, 0.9] → pale, very large, nectar-rich.

The genetic algorithm then evolves plant populations to approach those preferences.

3. What this means scientifically

The model is not data-driven yet — it’s rule-based (pollinator syndromes mapped into numbers).

But it’s consistent with real-world biology: the fact that your ant-run evolved toward [0.12, 0.19, 0.21] is exactly what pollination ecology predicts for ant-pollinated plants.

Once we hook into trait databases (TRY, GBIF) → we can test whether real flowers that are ant-pollinated cluster near those values.

Real plant traits datasets.

🌸 Scientific Background

This simulation is based on the concept of pollination syndromes: the idea that different pollinators (ants, bees, bats, etc.) tend to favor flowers with certain combinations of traits (color, size, nectar reward). Over evolutionary time, plants adapt their traits to maximize pollination success.

Trait definitions in the model:

Trait 1: Flower color brightness (0 = white/pale, 1 = vivid/bright)

Trait 2: Flower size (0 = tiny, 1 = large)

Trait 3: Nectar reward (0 = none, 1 = abundant)

Pollinator preference profiles (syndromes):

Ants 🐜: [0.1, 0.2, 0.2] → small, pale, low-nectar flowers

Bees 🐝: [0.8, 0.7, 0.5] → colorful, medium-to-large, moderate nectar flowers

Bats 🦇: [0.2, 0.8, 0.9] → pale, large, nectar-rich night-blooming flowers

These are simplified from ecological literature:

Kevan, P. G., & Baker, H. G. (1983). Insects as flower visitors and pollinators. Annual Review of Entomology, 28, 407–453.

Fenster, C. B., Armbruster, W. S., Wilson, P., Dudash, M. R., & Thomson, J. D. (2004). Pollination syndromes and floral specialization. Annual Review of Ecology, Evolution, and Systematics, 35, 375–403.

Fleming, T. H., Geiselman, C., & Kress, W. J. (2009). The evolution of bat pollination: a phylogenetic perspective. Annals of Botany, 104(6), 1017–1043.
