# HORSE, Simulation, and Bayesian Decision Analysis

I wanted to see how a player should choose shots in HORSE when they don't know exactly how good they or their opponent are at each type of shot.

I built a simple model of 1v1 HORSE and used it to explore how different shot-selection strategies perform under uncertainty.

## What I did

The project starts with a simple mathematical model for the probability of giving your opponent a letter on a given turn.

From there, I add uncertainty about shooting ability using Beta distributions and Bayesian updating. I then use that information to compare different ways of choosing shots:

Thompson sampling
A simpler heuristic strategy
Random shot selection

I also look at how the results change when the assumptions of the model change, including different priors and different amounts of uncertainty in player abilities.

## Main ideas

The project uses:

- Bayesian inference
- Thompson sampling
- Simulation
- Sensitivity and robustness analysis

For a shot with your make probability $p_y$ and your opponent's make probability $p_o$, the probability of eventually giving your opponent a letter is

$$
P(\text{letter}) =
\frac{p_y(1-p_o)}{1-p_yp_o}
$$

This gives a way to compare shots when the probabilities are known. The rest of the project is about what happens when those probabilities have to be learned.

## Tools

Python, NumPy, Pandas, Matplotlib, and SciPy.

## Notebook

The full analysis is in HORSE.ipynb.