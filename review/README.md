# Delpezzo Review Workspace

This directory contains the strict verification artifacts for
`E:\Personal\Random\Random\Delpezzo\delpezzo.pdf`.

Artifacts are organized as follows:

- `packet_manifest.md`: packet IDs, scope, dependencies, and intended evidence span.
- `prompt_protocol.md`: neutral subagent prompt templates and dynamic prompt-adjustment rules.
- `status.md`: live orchestration state, dependency-gate progress, and discrepancy log.
- `merged/`: merged packet and section memoranda written after primary-agent consensus.
- `audits/`: major-section audit memoranda.

Review rules in force:

- Each small packet is reviewed by 3 identical primary subagents.
- Any major discrepancy triggers 2 identical `unsure` subagents.
- Each major section is checked by 2 identical audit subagents after merge.
- No packet is treated as accepted unless at least 2 of 3 primaries agree and no
  unresolved dependency remains open.
- Subagent prompts must remain neutral: they must not presume the paper is correct
  or incorrect, and they may be refined dynamically only to reduce bias, scope drift,
  or contamination from earlier agent behavior.

- If you are told to review a single packet, do NOT review any other packet or work on additional artifacts. You must remain within your boundaries, and are not allowed to create more than the allowed files as stated in here
