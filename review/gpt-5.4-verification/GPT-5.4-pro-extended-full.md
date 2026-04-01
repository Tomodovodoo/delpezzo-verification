After checking the PDF itself, the existing audit workspace, and the late Section 12 proof spine, my verdict is:

**The manuscript is not correct as written.** More precisely, the claimed seven-point theorem is **not proved by this paper** in its current form. I am **not** saying the theorem is false; I am saying the proof given here does not establish it. The decisive point is that the final height-selection theorem, Theorem 12.72, closes its residual cases using results that depend on earlier broken inputs, and Corollary 12.73 then identifies Theorem 12.72 as the last missing ingredient for the global theorem. 

I also checked the load-bearing problematic lines against the PDF text itself, because OCR/PDF extraction errors would matter here. The bad statements really are in the PDF: Proposition 9.10 really does assert that the connected component (T) has a unique horizontal component, Corollary 9.24 really does say that in “every other case” the third contact is (F_{p-1}), and Proposition 12.55 really does invoke Lemma 9.41. These are not text-extraction artefacts.

## The strongest fatal defect: Lemma 9.41 is false as stated

Lemma 9.41 claims an equivalence between:

1. existence of a birational morphism (\varphi:S\to Y) to a smooth surface such that (\varphi(E)) is irreducible, (\varphi|_R) is birational onto (\varphi(E)), and every component of (E-R) is (\varphi)-exceptional; and
2. a contraction sequence that blows down only ((-1))-curves contained in the current image of (E-R), never contracts the current image of (R), and ends with only the image of (R). 

That equivalence is false.

Take an irreducible nodal plane cubic (C\subset \mathbf P^2), with node (p). Let
[
\alpha:S_0=\operatorname{Bl}_p(\mathbf P^2)\to \mathbf P^2,
]
let (A\subset S_0) be the exceptional curve, and let (R\subset S_0) be the strict transform of (C). Then (R\cong \mathbf P^1), (A\cong \mathbf P^1), and (R) meets (A) transversely in two points, so
[
p_a(R+A)=0+0+2-1=1.
]

Now choose a smooth point (q\in A\setminus R), and blow it up:
[
\beta:S=\operatorname{Bl}_q(S_0)\to S_0.
]
Let (R',A'\subset S) be the strict transforms of (R,A). Set
[
E:=R'+A',
\qquad \text{with root } R'.
]
Then (E) is a connected reduced SNC divisor, every component is a smooth rational curve, and
[
p_a(E)=0+0+2-1=1.
]

Now define
[
\varphi:=\alpha\circ \beta:S\to \mathbf P^2.
]
Then:

* (\varphi(E)=C) is irreducible;
* (\varphi|_{R'}:R'\to C) is birational;
* every component of (E-R') is (\varphi)-exceptional, since (A') maps to the node (p).

So condition (1) of Lemma 9.41 holds.

But condition (2) fails. Indeed,
[
E-R' = A',
\qquad (A')^2=-2.
]
So there is **no** ((-1))-curve contained in the current image of (E-R') with which to start the required contraction sequence. The necessary first ((-1))-curve is the *new* exceptional curve of (\beta), but that curve is **not a component of (E)**. Hence (1) does **not** imply (2).

So the lemma is not merely “underproved”; it is **false as stated**. The proof’s mistake is exactly the step claiming that, because the components of (E-R) are (\varphi)-exceptional, one can always find a ((-1))-curve among their current images. That is simply wrong: the ((-1))-curve needed in a factorization of (\varphi) may lie outside (E). 

This is a **fatal**, not minor, defect.

## Why that already kills the final theorem

Proposition 12.55 is one of the late Section 12 closure lemmas. It says that if (H) is birationally mapped to an irreducible singular plane cubic, then (X) has a descendant with elliptic boundary. Its proof constructs a reduced SNC divisor (E) of arithmetic genus (1), then says: “Lemma 9.41 applied with root (R) shows that (E) contains an elliptic tie.” That step is invalid because Lemma 9.41 is false. 

That is not an isolated late typo. Theorem 12.70 uses Proposition 12.55 to eliminate the purely inseparable ordinary singleton ([2])-root branch. Then Theorem 12.72 closes the final height-selection problem by citing Theorem 12.70 for case (iii), Corollary 12.67 for case (ii), and Theorem 12.33 for case (i). Finally Corollary 12.73 says that proving Theorem 12.72 proves the seven-point theorem. So once Proposition 12.55 breaks, one of the three explicit closing branches of Theorem 12.72 breaks as well, and Corollary 12.73 no longer follows. 

That alone is enough to reject the manuscript as a proof of the main theorem.

## A second, independent broken Section 12 branch

There is also a separate compromised branch through Proposition 12.39.

Proposition 12.39 handles the “mild same-component residue” on a special multisection. Its proof explicitly uses:

* Lemma 9.41 to pass from a local birational morphism to local sandwichedness/root-contractibility;
* Proposition 9.34(3) to force (m=0);
* Theorem 9.79 to conclude elliptic-boundary descent.

That is already enough to make the branch unstable:

* the use of Lemma 9.41 is invalid, because 9.41 is false;
* Proposition 9.34(3) itself is not proved correctly as written, for reasons below;
* Theorem 9.79 is itself built on Lemma 9.41.

Then Corollary 12.40 says the remaining isolated local output is excluded by Proposition 12.39, Proposition 12.41 uses Corollary 12.40 to say the separable special-multisection branch lands in old geometry, and Corollary 12.67 is used in Theorem 12.72 to close case (ii). So case (ii) is compromised independently of case (iii).

So there are **at least two independent late-stage failures** in the final Section 12 closure.

## Other non-minor defects I checked directly

### Proposition 9.10 has a real root-contractibility gap

The proof first shows (L\cdot D=2), then lets (T) be the connected component of (D+L) containing (L), and states that (T) has unique horizontal component (H). But the hypotheses only give
[
L\cdot D_{\mathrm{hor}}=1,
]
which controls the horizontal components meeting (L), not the total number of horizontal components in the connected component of (D) containing that one. So (T) may contain additional horizontal components elsewhere. The subsequent “relative minimalization” argument only contracts vertical curves, and therefore does **not** prove the asserted root-contractibility of the whole rooted configuration. This is a major proof gap, not a cosmetic issue.

### Lemma 9.6 and Proposition 9.7 rely on a false survival principle

Lemma 9.6 says that if (R) is a multiplicity-one component of a singular fiber, then after relative minimalization its image is “exactly the resulting smooth fiber.” The proof treats multiplicity one as if it forced survival. It does not. Consider a ruled surface and blow up a point on a smooth fiber. The resulting singular fiber is
[
F' + E,
]
with both components of multiplicity (1). A relative minimalization can contract (E), so the image of that multiplicity-one component is a point, not the final fiber. Thus the proof’s key implication is false. Proposition 9.7 then inherits the same gap because it cites Lemma 9.6 to deduce root-contractibility. This is again non-minor.

### Corollary 9.24 has a genuine subcase error

Here the issue is concrete. In the case (u>0) and (p=1), the local chain is
[
G_1-\cdots-G_u-F_1,
]
and (L=F_p=F_1) meets (G_u), not (F_{p-1}), because (F_{p-1}) does not exist. But the corollary says that in “every other case” the third (D)-contact is on (F_{p-1}). So the statement is literally wrong on that real subcase, and the proof follows the same wrong branch. This is local rather than fatal by itself, but it is a genuine mathematical error.

### Proposition 9.34 is not proved correctly

I do **not** have a counterexample to the *statement* of Proposition 9.34, but the proof is invalid as written. The problem is the repeated use of blowdown arithmetic as if all new incidences were simple edges. In the consecutive-contact cases, contracting (L) can turn an already existing edge into a **double edge**. If one then contracts one of the adjacent curves, the other curve’s self-intersection changes by
[
(2)^2 = 4,
]
not by (1). The proof repeatedly reasons as if the change were (1), so the exclusion of several subcases is not justified. This is a major proof gap. The packet audit independently flagged exactly this “double-edge blowdown” problem. 

### Proposition 9.44 has the same double-edge defect

The ((B,U)) case is mishandled for the same reason. After contracting (L), the edge (BU) is doubled, so contracting (U) changes (B^2) by (4), not by (1). The proof’s self-intersection bookkeeping is therefore wrong, and the claimed elimination of that case is not established. Again, this is a serious proof defect even if the final classification might still turn out true. The packet review flagged 9.44 as a real gap as well. 

### Proposition 9.48 is only finite-search evidence, but Theorem 9.58 treats it as a theorem

Proposition 9.48 gives explicit proofs for certain low cases, but its part (3) is only a search through
[
2\le n\le 20,\qquad a\in{3,4},
]
finding no other positive root-contractible cases. That is *not* an all-(n) proof. Yet Theorem 9.58 then treats Proposition 9.48 as the complete first-frontier classification and packages it into a formal “first-frontier exhaustion” theorem. That overreach is real and non-minor. 

### Proposition 9.75 / Corollary 9.76 use an unstated global isolation hypothesis

In Proposition 9.75 the proof says that every other component of (\sigma_*D) has zero intersection with (F): locally because only (S_1) and (S_2) meet (F), and globally because “the short bridge joins two full connected components of (D) on the first frontier.” But that global hypothesis is **not in the statement** of Proposition 9.75. Without it, extra (D)-components can attach to the local bridge cluster, and (F\cdot D) need not equal (2). So the ruling argument does not prove Corollary 9.76 as written. This is a major gap. 

### Corollary 9.80 is a real statement/proof mismatch

The statement is universal: if a characteristic-3 rank-one klt del Pezzo surface with (#\mathrm{Sing}\ge 8) contains a positive root-contractible contact-2 configuration, then either it already gives an elliptic descendant or it is a distinct-component bridge. But the proof immediately specializes to a “benchmark counterexample,” invokes Theorem 9.1, and uses the residual no-descendant assumption. So the proof establishes only a residual-sector version, not the theorem as written. This is not fatal by itself, but it is a genuine theorem/proof mismatch. 

### Proposition 8.3 has a real computational exclusion gap

The computation section for Proposition 8.3 says the unresolved MILP fringe was closed by imposing the row-index identity
[
I=(a_1+a_2)+(b_1+b_2)+(c_1+c_2)-d,
]
because that identity had been verified on previously solved exact hits. But the paper never proves that every exact decomposition in the unresolved fringe must satisfy that same identity. So the MILP only excludes a *restricted* class of candidates. The claim that the full window is closed is therefore not established. This is non-minor, and Section 9.1 later treats Proposition 8.3 as part of the “essentially exhausted” explicit search space.

### Proposition 5.1 is also not proved

The PDF itself labels Proposition 5.1 only as a “Sketch,” and the key steps are just asserted: the visible-graph reduction, the exclusion of non-visible negative curves, and the final count that yields
[
\rho(Y)\ge r.
]
The audit file for Section 5 correctly identifies both the unsupported visible-graph reduction and a genuinely defective local branchwise bound. Section 9.1 then relies on Proposition 5.1 as if that route were already closed. So this is not a harmless sketch omission.

### Corollaries 9.86 and 9.87 contain real written derivation defects

These are less important than the failures above, but they are still real. Corollary 9.86 says “so in particular (n=a) by Proposition 9.85(2),” even though the notation there does not match the surrounding proposition, and 9.87 then leans on already-broken 9.86 plus out-of-scope Corollary 9.88. So even the late anticanonical cleanup is not stable as written.

## Severity: which faults are minor, which are fatal

The defects break into two groups.

**Fatal / non-minor faults:**

* Lemma 9.41 is false.
* Proposition 12.55 depends on false Lemma 9.41.
* Theorem 12.70 depends on 12.55.
* Theorem 12.72 depends on 12.70, and Corollary 12.73 depends on 12.72.
* Proposition 12.39 depends on Lemma 9.41, Proposition 9.34(3), and Theorem 9.79.
* Proposition 9.10, Lemma 9.6, Proposition 9.7, Proposition 9.34, Proposition 9.44, Proposition 9.48, Proposition 9.75/Corollary 9.76, Proposition 8.3, and Proposition 5.1 each leave load-bearing arguments unproved or invalid.

**Real but more local / potentially patchable faults:**

* Corollary 9.24’s (u>0,p=1) subcase.
* Corollary 9.80’s statement/proof mismatch.
* Corollaries 9.86–9.87’s notation/algebra defects.

So this is not a situation where the paper is “basically right except for a typo.” The current manuscript needs genuine new arguments in several places, not just cleanup.

## Bottom line

My final judgment is:

[
\boxed{\text{The paper is not correct as written, and its main theorem is unproved in this version.}}
]

The clearest single reason is that Lemma 9.41 is false as stated, and Section 12 explicitly uses it in a branch that feeds the final theorem. Independently, Proposition 12.39 routes another late branch through 9.41 and 9.34. So the failure is not confined to one isolated local lemma; it reaches the final closure.

What I do **not** conclude is that the seven-point theorem itself is false. It may still be true. But this manuscript does not establish it.

The next best step would be a referee-style report organized theorem-by-theorem, separating “false statement,” “proof gap,” and “statement/proof mismatch,” with the dependency tree showing exactly which repairs would be needed.
