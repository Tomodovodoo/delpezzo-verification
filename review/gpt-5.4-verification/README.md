# GPT-5.4 Verification

## Overview

- All three reports agree that the paper, as written, does not prove its claimed seven-point theorem for characteristic-3 klt del Pezzo surfaces of Picard rank `1`.
- All three reports also agree that they do not disprove the theorem itself; the verdict is about failure of the manuscript's proof, not falsity of the claim.
- The shared decisive defect is `Lemma 9.41`, and all three reports trace late Section `12` failures through `Proposition 12.55` into the final closure.
- All three reports also treat `Proposition 12.39` as a second broken late-stage branch.

## False Statements

- `Lemma 9.41` is false as stated: all three reports give nodal-cubic blowup counterexamples where `9.41(1)` holds but `9.41(2)` cannot even start because the first necessary `(-1)`-curve lies outside `E`.
- `Corollary 9.13(2)` contains a false displayed equality as written; the reports treat the intended inequality as likely repairable.
- The proof of `Proposition 9.34` contains false blowdown bookkeeping in the double-edge case: once the intersection multiplicity is `2`, the self-intersection jump is `4`, not `1`.
- One fuller report additionally says `Corollary 9.24` is literally wrong in the subcase `u > 0`, `p = 1`.
- One fuller report additionally says `Lemma 9.6` rests on a false multiplicity-one survival principle, and `Proposition 9.7` inherits that failure.
- One report additionally says the proof of `Proposition 9.10` contains a literally false sentence claiming relative minimalization contracts every component of a reducible fiber.

## Unverified or Broken-As-Written Statements

- `Proposition 12.55` is not proved as written in all three reports because it explicitly uses the false direction of `Lemma 9.41`.
- `Proposition 12.39` is also broken as written in all three reports because it again uses `Lemma 9.41`, and then leans on other unstable inputs.
- The late closure chains through `12.55` and through `12.39` are therefore unproved as written, so the final Section `12` closure does not go through.
- `Proposition 8.3` is not established as a theorem: all three reports say its MILP exclusion uses an extra row-index identity that was observed or verified on solved cases but not proved for the unresolved fringe.
- `Proposition 9.10` is broken or unproved as written in all three reports, but they diagnose it differently: citation-scope mismatch, a missing "unique horizontal component" justification, and a faulty relative-minimalization step.
- `Proposition 9.48` gives only finite-search evidence, while `Theorem 9.58` treats it as an all-`n` classification; all three reports treat that as an overreach.
- One fuller report additionally flags `Proposition 5.1`, `Proposition 9.44`, `Proposition 9.75` / `Corollary 9.76`, `Corollary 9.80`, and `Corollary 9.87` as broken, overstated, or mismatched.
- `Corollary 9.86` is genuinely disputed across the reports: one report says the PDF formula and resulting bounds are fine, another says `9.86`-`9.87` still have real written derivation defects, and the third does not resolve it.

## Counterexamples

- Common `Lemma 9.41` mechanism in all three reports: start with an irreducible nodal plane cubic, blow up the node, then add extra blowup(s) away from the chosen root; define `E` so the newest exceptional curve(s) are not components of `E`; then the birational contraction exists but the required rooted contraction inside `E` cannot begin.
- The reports use different concrete realizations of that mechanism: one uses a minimal two-component divisor `R + A'`, while another uses a four-cycle `R-A-F-B-R`; they agree on the obstruction and differ only in the model.
- One fuller report gives a separate counterexample to the `Lemma 9.6` survival principle: blow up a point on a smooth fiber of a ruled surface, producing `F' + E`; the multiplicity-one component `E` can be contracted during relative minimalization, so multiplicity one does not force survival.

## Needed Reworks

- Replace `Lemma 9.41` with a correct statement: either strengthen the geometric hypothesis so `E - R` is the full relevant exceptional or reduced-total-transform locus, or weaken the contraction-sequence side to allow auxiliary blowdowns outside `E`.
- Rebuild `Proposition 12.55` and `Proposition 12.39` without using the false `9.41(1) => 9.41(2)` implication.
- Replace empirically constrained or finite-search arguments with theorem-level proofs where later results use them, especially in `Proposition 8.3` and `Proposition 9.48` / `Theorem 9.58`.
- Rewrite `Proposition 9.10` and `Proposition 9.34` with correct hypotheses and contraction arithmetic.
- Repair local written slips such as `Corollary 9.13(2)` and, if confirmed, `Corollary 9.24`.
- Recheck the disputed `Corollary 9.86` line directly from the PDF before treating it as either clean or broken.

## Final State of the Paper

- Best-supported overall verdict across the three reports: the manuscript is not correct as written, and its claimed seven-point theorem is unproved in this version.
- The reports do not show that the theorem itself is false.
- The failure is not a single isolated typo: the final Section `12` closure depends on earlier broken inputs, so the paper's last theorem does not currently follow from the arguments printed here.
