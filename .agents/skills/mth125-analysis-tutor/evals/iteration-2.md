# Iteration 2: concise-output regression

Observed failure in the prior skill-enabled Topic 1 run:

- The answer exposed a full `双重逻辑审计` table.
- It reported repeated `通过 / 不适用` statuses and narrated internal verification.
- This made the answer substantially longer without helping the user learn the construction or proof.

Refactor:

- Keep both logic audits mandatory but silent.
- Define a positive minimal output shape: 1–4 key ideas, an English formal proof when needed, and at most one useful Chinese note or anchor.
- Show only decisive AI-solution errors and their shortest repairs.
