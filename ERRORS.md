# ERRORS

- `prod_of_ratios` (file: `PNT3_RiemannZeta.lean`): removed a crucial condition from the blueprint, but `simplify_prod_ratio` goes through, so harmless misformalization
- `inv_inequality` (file: `PNT3_RiemannZeta.lean`): weakened `hab` to be `a < b` instead of `a <= b`. This causes `abs_term_inv_bound` to fail. Ideal agent would recognize this when proving `abs_term_inv_bound` and fix `inv_inequality`
- `lem_rho_in_disk_R1` (file: `PNT3_RiemannZeta.lean`): added `R < 0.5`, making it too strict to use (future lemmas rely on it being `R < 1`). Propagated this down a few lemmas and stopped at `lem_R_div_mod_rho_ge_R_over_R1`; interesting whether an agent adds the condition there or corrects `lem_rho_in_disk_R1`.
