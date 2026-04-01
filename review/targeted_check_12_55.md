# Targeted Check: Proposition 12.55

Source paper: [delpezzo.pdf](E:\Personal\Random\Random\Delpezzo\delpezzo.pdf)

Checked statement: `Proposition 12.55` on printed p. `225` / PDF p. `226`.

## Question

Daniel Litt's objection was that the proof of `Proposition 12.55` is wrong because the claim

`f_* O_E = O_C`

is false when `C` is a cuspidal plane cubic.

## Conclusion

That objection is **correct**.

It is **not** the exact same issue previously recorded in the main review. The earlier synthesis had already identified `Proposition 12.55` as lying on a broken final-proof spine because it explicitly invokes already-gapped `Lemma 9.41`. Litt's point is a **new independent flaw inside the proof of `12.55` itself**.

## Where the proof fails

The proof says:

> "The fibers of the induced map `E -> C` are connected trees of rational curves, so `f_* O_E = O_C` and `R^1 f_* O_E = 0`."

The second clause is plausible fiberwise, but the first is not valid for a cuspidal cubic.

If `C` is cuspidal, then the strict transform `R` of `H` is the normalization of `C`, hence

`R ~= P^1`, `R -> C` is birational, and `(R -> C)_* O_R = nu_* O_{P^1} != O_C`.

The extra exceptional divisor over the cusp is a connected tree of rational curves attached to `R` at a single point. Contracting such a tree does **not** force the pushforward back down to `O_C`; locally it contributes no new gluing condition beyond the value at that one attachment point. So over a small neighborhood of the cusp,

`f_* O_E = nu_* O_R`,

not `O_C`.

Equivalently: for a cuspidal cubic, the reduced total transform `E` is a tree of rational curves, so its arithmetic genus is `0`, not `1`.

## Consequence

The proof's deduction

`p_a(E) = p_a(C) = 1`

fails in the cuspidal case. Therefore the next sentence,

`Lemma 9.41 applied with root R shows that E contains an elliptic tie`,

has no established input in that case.

So `Proposition 12.55` is **false as stated / unproved as written** for singular plane cubics in general. At best, the displayed argument only has a chance in the nodal case.

## Relation to the main verdict

This strengthens the existing negative verdict rather than replacing it:

- earlier review already found the final proof spine broken through `Lemma 9.41`
- this targeted check shows that `Proposition 12.55` also has its **own** internal defect

So later uses such as `Theorem 12.56` and `Theorem 12.61` now have an additional independent failure mode unless the author can separately prove that only nodal cubics arise there, or replace `12.55` with a different argument.
