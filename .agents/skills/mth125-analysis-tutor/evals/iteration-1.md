# Iteration 1: proof-audit regression

The first skill-enabled pressure test obeyed the source, anchor, sequencing, and English-proof rules, but its proof of `n^(1/n) -> 1` contained a false implication:

> “If `n epsilon > 1`, Bernoulli's inequality gives `(1 + epsilon)^n >= 1 + n epsilon > n`.”

The premise only makes `1 + n epsilon > 2`; it does not imply `1 + n epsilon > n` for small epsilon. The answer then marked its own proof as passing the logic audit.

Refactor:

- Require every claimed sufficient condition to be written and checked as an implication chain.
- Require `N(epsilon)` and `delta(epsilon)` to be substituted back into the original target.
- Add the failed root-limit argument as a concrete counterexample and regression eval.
