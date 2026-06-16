# Adoptee Test v3 — Coding Rubric (the validity gate)

Every latent variable is scored in [0,1] (W_g floored at 0.01). Anchors below make codings
reproducible. Record `coding_confidence` (illustrative / low / med / high) and a short
`evidence_basis` for every value. Two coders should reach the same value from the same source.

## H_g — experienced harm to the group
- 0.00  no harm
- 0.25  measurable but bounded harm, recoverable
- 0.50  serious, durable harm
- 0.75  severe harm to identity, relationships, or rights
- 1.00  catastrophic / identity-destroying harm

## W_g — detection probability (does the framework SEE the harm)
- 1.00  group's harm is named and measured by the framework; group is represented in its review
- 0.50  harm is mentioned but not measured; no seat at the table
- 0.10  token or incidental acknowledgement
- 0.01  effectively invisible (floor; never literally 0)
Indicators: is the group seated on the evaluating body? is its harm a measured input or an aside?

## R_g — rights retained / P_g — power possessed
- 0.00 none ... 1.00 full. Score against the rights/power the framework claims to protect.

## F, K, C, N — identity continuity (before and after the severance event)
Each in [0,1]: 1.00 fully retained, 0.00 fully severed.
- F family continuity, K knowledge of origins, C cultural continuity, N legal identity continuity
- I = F·K·C·N (multiplicative: any single 0 collapses integrity)

## D_loss — framework detection of the identity loss
- 0.00 the framework does not register the severance at all
- 1.00 the framework fully registers and records it
F_I = |ΔI| · (1 − D_loss): a large undetected severance scores high failure.

## Derived (computed — do not hand-enter)
H_id = −log2(W_g) ; A_g = H_g·H_id ; ΔI = I_after − I_before ; F_I = |ΔI|·(1−D_loss)
recall(S) = Σ(W_g·H_g)/Σ(H_g)