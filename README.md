# Research-PLMs
Do Not Stop at the Last Layer: Embedding Trajectory Dynamics in Protein Language Models Reveal Functional Class Structure at Internal Layers That Final-Layer Representations Do Not Preserve

# What we observed
At multiple internal layers, we observed that proteins from the
same functional class exhibited more similar velocity and accel-
eration vectors than proteins from different classes. On DUD-E,
this held across all 15 model configurations; on the Pfam-derived
dataset, the same pattern was observed using ESM2 (150M) and
ESM3 (Small). At the final layers, the class-specific directional sim-
ilarity diminished across all evaluated models and both datasets.
FDR, silhouette score, and linear probe accuracy each peaked at
internal layers. Velocity and acceleration magnitudes increased at
the final layers across all evaluated models, regardless of architec-
ture or training objective, but this escalation did not correspond to
improved functional class separability in any configuration.
# Contributions
• First systematic trajectory dynamics analysis of PLMs.
To our knowledge, this is the first systematic application of
layer-wise trajectory dynamics (velocity and acceleration)
to protein language models, adapting the geometric frame-
work of Zhou across 15 model configurations on
DUD-E and four configurations on a Pfam-derived dataset.
• Trajectory co-travel and block-diagonal structure at
internal layers. Proteins from the same functional class
co-travel at internal layers: their velocity and acceleration
vectors are substantially more similar to each other than
to those of cross-class pairs, forming clear block-diagonal
structure in pairwise cosine similarity matrices. This block
structure is visually sharper than in static embedding matri-
ces at the same layers and is consistent across all 15 DUD-E
configurations and all 4 Pfam configurations, regardless
of model family, training objective, or pooling strategy.
Proteins from the same class share sequence similarity by
construction, and this likely contributes to the observed
co-travel; we report the geometric pattern without claiming
causal independence from sequence relatedness.
• Collapse of directional similarity at the final layers.
The class-specific directional similarity at internal layers
diminishes at the final layers across all evaluated models,
consistent with the shift toward the residue-level recon-
struction objective.
• Internal layers outperform the final layer on three
independent metrics. FDR, silhouette score, and linear
probe accuracy each peak at internal layers and decline
toward the final layer in all evaluated configurations, repli-
cating and extending prior layer-wise observations within
a trajectory framework.
• Architecture-specific magnitude escalation. ESMC ex-
hibits progressive velocity magnitude escalation from mid-
network; ESM2 and ProtT5 concentrate escalation at the
final layers. Neither pattern corresponds to improved func-
tional class separability.
