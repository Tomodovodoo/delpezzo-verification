I wrote up a fuller report here: [delpezzo verification report](sandbox:/mnt/data/delpezzo_verification_report.md).

I checked the actual typeset PDF in the decisive places, not just the extracted text, precisely to avoid PDF→text/OCR artifacts. My conclusion is:

**The manuscript is not correct as written, and its final seven-point theorem is unproved in this version.** I do **not** conclude that the theorem itself is false. The strongest justified statement is that the proof fails. 

The decisive issue is **Lemma 9.41**. The paper states it as an equivalence between an “ambient birational contraction to an irreducible genus-one image” and an “internal root-preserving contraction sequence” for the divisor. The printed proof of the hard direction says, in substance, that once every component of (E-R) is (\varphi)-exceptional, then at each stage one can find a ((-1))-curve among the current images of the components of (E-R). That claim is false.

Here is a concrete counterexample.

Take an irreducible **nodal plane cubic** (C\subset \mathbf P^2), and let (p\in C) be its node. Blow up (p), with exceptional curve (F). The strict transform of (C) is smooth and meets (F) transversely in two points (p_1,p_2). Blow up (p_1) and (p_2), with exceptional curves (A) and (B). Then blow up one general smooth point of (A) away from (R\cup F), and one general smooth point of (B) away from (R\cup F); call the new exceptional curves (A') and (B'). Let (R) be the final strict transform of (C), and set
[
E:=R+F+A+B.
]

Then (E) is a connected reduced SNC divisor on a smooth surface, every component is a smooth rational curve, and its dual graph is the 4-cycle
[
R-A-F-B-R.
]
Hence
[
p_a(E)
=\sum p_a(E_i)+\sum_{i<j}E_i\cdot E_j-#{\text{components}}+1
=0+4-4+1=1.
]

Now let
[
\varphi:S\to \mathbf P^2
]
be the birational morphism contracting everything back to the plane. Then (\varphi(E)=C) is irreducible, (\varphi|_R) is birational onto (C), and every component of (E-R) is (\varphi)-exceptional. So condition (1) of Lemma 9.41 holds. But after the two extra blowups, one has
[
A^2=B^2=-2,\qquad F^2=-3.
]
Thus **none** of the components of (E-R) is a ((-1))-curve on the starting surface. Since the lemma’s condition (2) only allows blowdowns of ((-1))-curves contained in the current image of (E-R), there is no legal first move. So condition (2) fails. Therefore
[
(1)\not\Rightarrow(2),
]
and **Lemma 9.41 is false as stated**. This is a major defect, not a minor slip. The lemma’s converse direction is the bridge the paper uses to pass from “there exists a birational model” to “the divisor is root-contractible / locally sandwiched of (\delta=1).” 

That one false lemma already breaks the final spine. In **Proposition 12.55**, the paper constructs a reduced total transform (E=(f^{-1}(C))_{\mathrm{red}}) of a singular plane cubic (C), proves (p_a(E)=1), and then says “Lemma 9.41 applied with root (R) shows that (E) contains an elliptic tie.” That is exactly the false direction above. So Proposition 12.55 is **not proved as written**.

And Proposition 12.55 is not a side lemma. It is then used in **Theorem 12.56** (degree-two one-section branch), **Theorem 12.61** (pure-triple cubic branch), and **Theorem 12.70** (purely inseparable ordinary singleton ([2])-root branch). Those are then fed into **Theorem 12.72**, and Corollary 12.73 is deduced from Theorem 12.72. So once Proposition 12.55 is unproved, the final theorem is unproved.

A second late-stage failure is **Proposition 12.39**. Its proof says, essentially, that because the local block comes from resolving one singularity on a smooth ruled surface, there is a birational morphism from a neighborhood of (E:=A+L) to a smooth surface germ contracting (E-H), and since (p_a(E)=1), Lemma 9.41 implies (E) is locally sandwiched of (\delta=1), hence root-contractible. That is again the same false implication. Then the proposition leans further on Proposition 9.34(3). So Proposition 12.39 is also broken as written.

There are several additional confirmed proof problems.

**Proposition 8.3** is not established rigorously. The “complete” MILP exclusion of the unresolved fringe imposes a row-index identity
[
I=(a_1+a_2)+(b_1+b_2)+(c_1+c_2)-d
]
because it held in the already-solved slice. But the paper does not prove that identity is necessary in the unresolved 298-row fringe. So the MILP is exact only **after** adding an empirically observed restriction, and the proposition overstates what has been proved. This is a real gap, though not the fatal one. 

**Proposition 9.10** has a statement/proof mismatch. It is stated for a general klt del Pezzo surface, but the proof invokes [7, Lemma 2.8(b)] to conclude that a component of a degenerate fiber is a ((-1))-curve iff it is not contained in (D). In the cited source, that lemma is explicitly in the setting of a **surface of Picard rank one**, so the argument only justifies the proposition under that stronger hypothesis. There is also a second gap: relative minimalization of the whole fiber does not by itself produce the paper’s stricter rooted-contraction sequence. I would classify 9.10 as unproved as written, not as definitely false.  ([arXiv][1])

**Proposition 9.34** contains a genuine blowdown error. In one of the key exclusion cases, the proof treats a configuration where contracting (L) creates a **double edge**, and then reasons as if contracting one of the resulting ((-1))-curves raises the other to self-intersection (0). But the blowdown formula is
[
(C')^2=C^2+(E\cdot C)^2.
]
With a double edge, (E\cdot C=2), so the increase is (4), not (1). The sentence “contracting one raises the other to self-intersection (0)” is simply wrong in that setting. I do not claim the proposition’s classification is false, but the proof is invalid.

**Proposition 9.48** only gives a rooted-graph search up to (n\le 20), yet **Theorem 9.58** later treats it as if it supplied the complete all-(n) classification of the corridor. A finite search through (n\le 20) is not a proof for all (n). So 9.58 overreaches. 

There is also a real but comparatively **minor** written error in **Corollary 9.13(2)**. The proof writes
[
\sum_{m_i\ge 2}(m_i-1)=\sigma(F)-#{i:m_i\ge 2},
]
which is not correct as stated. The equality should subtract all components (N_i), not just those with (m_i\ge2). However, the inequality the paper wants can still be salvaged, so I would class this one as a repairable counting slip, not a theorem-killer by itself.

One place where I **do not** agree with the earlier swarm is **Corollary 9.86**. After checking the actual PDF page, the formula
[
-K_X\cdot C=-1+\frac{2}{b}+\frac{2a-1}{a^2-a+1}
]
and the deductions (b\le 3) for (a\ge 5), (b\le 4) for (a=4), are fine. So I would not list 9.86 as a confirmed defect.

So the overall situation is:

The manuscript’s central claim is **not established**. The most decisive reason is that the paper’s final Section 12 closure passes through Proposition 12.55, which depends on a false Lemma 9.41. There are also multiple earlier proof gaps and overreaches. But nothing I checked shows that the seven-point statement itself is false; only that this manuscript does not prove it. That conclusion matches the earlier workspace’s paper-level verdict, though I would revise a few item-level classifications, especially 9.86.

My final verdict is:

[
\boxed{\text{Main theorem unproved as written; theorem not disproved.}}
]

[1]: https://www.arxiv.org/pdf/2412.21174v1?utm_source=chatgpt.com "https://www.arxiv.org/pdf/2412.21174v1"
