# Prompt Protocol

This file records the neutral prompt policy for all Delpezzo review agents.

## Core Rules

- Every packet gets 3 identical primary review prompts.
- Every major section audit gets 2 identical audit prompts.
- If a major discrepancy appears, 2 identical `unsure` prompts are issued on the
  conflict packet only.
- Prompts must remain neutral: they may not assume the paper is correct, and they
  may not assume the paper is flawed.
- Prompt revisions are allowed only when agent behavior shows a need to reduce
  bias, scope drift, contamination from earlier context, or implementation chatter.

## Current Primary Prompt Template

Use `fork_context: false`.

Prompt body:

`You are reviewing one packet from a mathematical proof. Assess only the packet
as written. Do not assume it is correct. Do not assume it is incorrect. Your goal
is to determine, as precisely and neutrally as possible, what is actually shown in
the text, what is cited, and what is only asserted.

Scope: [packet scope]
Pages: [exact PDF pages]
Source: E:\\Personal\\Random\\Random\\Delpezzo\\delpezzo.pdf

Instructions:
1. Work only on this packet.
2. Do not create or edit any files.
3. Do not discuss implementation, workspace management, or prior agent outputs.
4. If the packet is background-only, say so explicitly.
5. For each theorem-like item in scope:
   - transcribe the statement exactly enough to identify hypotheses and conclusion,
   - normalize the statement in your own words,
   - list the dependencies actually invoked,
   - outline the proof skeleton,
   - check each nontrivial inference,
   - check local calculations,
   - check whether each citation is precise enough for the claimed use,
   - flag hidden assumptions or missing hypotheses,
   - give a verdict: verified, gap, or unclear.
6. Keep the tone neutral and precise.
7. Be concise and packet-bounded: give the full review, but do not add
   unnecessary exposition outside the stated scope.

Output headings:
- Packet classification
- Statement inventory
- Step checks
- Hidden assumptions / citation issues
- Verdict`

## Current Audit Prompt Template

Use `fork_context: false`.

Prompt body:

`You are auditing a merged mathematical review memo. Do not assume the paper is
correct. Do not assume the merged memo is correct. Your goal is to assess whether
the merged memo accurately and neutrally represents the packet-level review.

Material:
- merged memo: [path or pasted memo]
- packet scope: [scope]
- pages: [exact PDF pages]
- source: E:\\Personal\\Random\\Random\\Delpezzo\\delpezzo.pdf

Instructions:
1. Work only on the stated major section.
2. Do not create or edit any files.
3. Do not discuss implementation, workspace management, or prior agent outputs
   beyond the material provided.
4. Decide whether the merged memo:
   - covers every theorem-like item in scope,
   - tracks dependencies faithfully,
   - avoids overstating certainty,
   - omits any material caveat.
5. State whether amendments are required.

Output headings:
- Audit scope
- Agreement with merged memo
- Missing or overstated points
- Audit verdict`

## Dynamic Prompt Adjustments Already Made

- Early prompts accidentally invited implementation chatter and cross-packet
  contamination. The current prompts explicitly forbid file editing, workspace
  commentary, and discussion of prior agent work.
- The current prompts explicitly tell agents to say when a packet is
  background-only, to prevent forced proof-style commentary on non-proof text.
- The current prompts explicitly instruct agents not to presume correctness or
  incorrectness, addressing bias concerns raised during the orchestration.
- For search-heavy packets, especially `Section 8`, the prompts now explicitly
  require agents to separate literature/background claims, heuristic motivation,
  theorem-like statements, and reported computations, and to assess whether a
  computational exclusion is actually established in the packet or merely
  reported with limited reproducibility detail.
- When an exact page span contains the start of the next packet, the prompts now
  explicitly tell agents to ignore visible theorem-like items outside the stated
  scope rather than commenting on them or importing them into the packet review.
- After several Section 9 runs drifted into very long execution times, the
  current prompts also ask for concise packet-bounded reporting. This is a
  runtime-control adjustment only; it does not change the neutral review
  standard or the required checks.
- After repeated shutdown-without-output failures on dense Section 9 packets,
  stalled-packet prompts may also ask for verdict-first compact reporting:
  concise per-item findings are preferred over long prose, provided the core
  neutral checks are still covered.
- If a packet still fails after that compact prompt, a replacement primary wave
  may keep the same model family and identical prompt while lowering reasoning
  effort from `xhigh` to `high` for runtime stability. This is treated as an
  execution-control fallback, not a change in review standard.
- If a packet continues to stall after those fallbacks, the replacement wave
  may receive the exact packet text directly in the prompt instead of being
  asked to retrieve it from the PDF. This is an evidence-delivery fallback
  only; the packet scope and neutral review standard remain unchanged.
