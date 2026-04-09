# GRAIN
GRAIN — Gut-derived Release of Agents Influencing Nociception
ReadMe: High-Dimensional Neuroimmune Profiling of Histamine-Driven Visceral Hyperalgesia

1. Research Overview and Scientific Significance

The interaction between the mucosal immune system and the enteric nervous system is a primary determinant of the "mechanistic endotype" underlying Irritable Bowel Syndrome (IBS). Investigating gut microbiota-derived metabolites—specifically neuroactive mediators like histamine—is strategically essential for decoding how luminal signaling translates into chronic visceral pain. While clinical correlations between dysbiosis and IBS are common, establishing a causal, metabolic basis for peripheral sensitization has remained elusive until the integration of gnotobiotic modeling and high-dimensional spatial proteomics.

This repository provides the computational and experimental framework associated with the findings of De Palma et al. (Science Translational Medicine, 2022). The study established a definitive causal link between the bacterial species Klebsiella aerogenes and the induction of visceral hyperalgesia. Utilizing three independent patient cohorts, researchers identified a specific hdc (histidine decarboxylase) gene variant in K. aerogenes as the driver of excessive histamine production. Crucially, this metabolic output is highly sensitive to the local microenvironment; histamine production is a function of colonic acidification and microbial fermentation rates, peaking at a luminal pH of 7.0 and decreasing significantly as the environment acidifies.

The clinical "So What?" layer resides in the transition from viewing IBS as a general sensitivity disorder to understanding it as a targetable metabolic interaction. By demonstrating that dietary fermentable carbohydrates provide the substrate for K. aerogenes—and that low-fermentable diets reduce both the abundance of these bacteria and urinary histamine levels—the research provides a mechanistically grounded rationale for symptom management. This repository contains the MIBI (Multiplexed Ion Beam Imaging) data and marker specifications used to map the spatial architecture of this neuroimmune axis.

2. Experimental Model: Gnotobiotic Mouse Cohorts

Gnotobiotic (germ-free) mice represent the gold standard for validating the impact of human fecal microbiotas on host physiology, as they allow for the isolation of specific microbial signals without interference from an indigenous flora. This model is essential for proving that the IBS-HH (High Histamine) phenotype is a transferable trait driven by the microbiota itself rather than host genetics alone.

Cohort Specifications and Physiological Assays This study utilized National Institutes of Health (NIH) Swiss and C57BL/6 germ-free mice. These cohorts were colonized via oral gavage with fecal transplants from human donors characterized by high urinary histamine (IBS-HH) or low urinary histamine (IBS-LH). To ensure experimental continuity, the mice used for the MIBI experiments are identical to those described in the De Palma et al. (2022) publication.

The physiological contrast between cohorts was quantified using high-precision assays:

* Visceromotor Response (VMR): Conscious mice were subjected to colorectal distension at specific volumes of 100 µl and 200 µl, showing significantly elevated responses in IBS-HH mice.
* Mechanosensitivity: Single afferent nerve recordings measured action potential discharge in response to von Frey hair (vFH) weights of 0.07, 0.4, and 1.0 g. IBS-HH colonized mice exhibited a dramatic shift in sensitivity thresholds compared to IBS-LH or healthy control (HC) cohorts.

These organismal-level findings of visceral hypersensitivity necessitated the sub-cellular proteomic mapping provided by the MIBI panel to identify the specific cellular junctions of pain signaling.

3. Cellular Lineage Phenotypes and Robust Markers

Mapping the intestinal neuroimmune landscape requires a high-fidelity classification of cellular lineages. The following table identifies the robust lineage markers used to define the spatial architecture of the intestinal barrier, the Enteric Nervous System (ENS), and the mucosal immune compartments.

Cell Type	Lineage Markers	Cellular Category	Tissue Context
Enteroendocrine cells	CHGA	Epithelial / Neuroendocrine	Intestinal barrier
Goblet cells	MUC2	Epithelial	Intestinal barrier
Epithelial cells	E-cadherin	Epithelial	Intestinal barrier
Neurons and nerve fibers	TUJ1, GAP43	Neural	ENS
Sensory neurons	CGRP, SUBP	Neural	ENS
Cholinergic neurons	CHAT	Neural	ENS
Nitrergic neurons	NOS1	Neural	ENS
Enteric glial cells	S100B	Neural	ENS
T-lymphocytes	CD3e, CD4, CD8a	Immune	Intestinal tissue
Macrophages	CD11b, F4/80, CD163	Immune	Intestinal tissue
Mast cells	Tryptase, Chymase	Immune	Intestinal tissue
Leucocytes	CD45	Immune	Intestinal tissue
Eosinophils	EMBP	Immune	Intestinal tissue
Smooth muscle / Myofibroblasts	\alphaSMA	Stromal / Structural	Intestinal wall
Mesenchymal / Stromal cells	Vimentin	Stromal / Structural	Intestinal tissue
Endothelial cells	CD31	Structural / Vascular	Blood vessels

Analysis of Neuroimmune Proximity and Nerve Density Beyond lineage identification, high-dimensional spatial analysis revealed that the IBS-HH microbiota creates a "perfect storm" for peripheral sensitization. In hyperalgesic mice, there is a significant increase in the density of Tryptase-positive mast cells. These effectors are not merely more numerous but are found in extreme proximity (< 2 µm) to PGP9.5-positive neurons. When coupled with the observed increase in colonic nerve density (sprouting) in IBS-HH mice, this proximity facilitates a direct metabolic-to-neural communication channel that drives chronic pain.

4. MIBI Multiplexed Antibody Panel Specifications

Multiplexed Ion Beam Imaging (MIBI) utilizes secondary ion mass spectrometry to detect metal-conjugated antibodies, enabling sub-cellular proteomic localization without the spectral overlap inherent in fluorescence microscopy. By targeting specific isotopic masses, we achieve high-plex resolution of the intestinal microenvironment.

The following markers from the PB-MSIBS-COHORT-PANEL are critical for reproducing the neuroimmune spatial analysis:

Target Marker	Mass & Element	Functional Classification	Predicted Localization
NaKATPase	89 Y	Transporter	Membrane
E-cadherin	113 In	Cell-Cell Adhesion	Membrane
HH3	115 In	Nucleosom component	Intracellular (Nuclear)
LPAR1	141 Pr	GPCR (Damage response)	Membrane
H1R	142 Nd	GPCR (Immune modulation)	Membrane, Intracellular
CD4	143 Nd	CD marker (T-cell coreceptor)	Membrane, Intracellular
CD11c	144 Nd	CD marker (Integrin \alpha-X)	Membrane, Intracellular
LPAR3	145 Nd	GPCR (Cellular mediator)	Membrane, Intracellular
H4R	146 Nd	GPCR (Histamine mediator)	Membrane
LPAR5	147 Sm	GPCR (LPA Receptor)	Membrane
H2R	148 Nd	GPCR (Gastric secretion)	Membrane
CHAT	150 Nd	Enzyme (ACh synthesis)	Intracellular
SUBP	151 Eu	Neuropeptide (Protachykinin-1)	Secreted
CD31	152 Sm	CD marker (Cell adhesion)	Membrane, Intracellular
Ki-67	153 Eu	Proliferation marker	Intracellular (Nuclear)
NOS1	154 Sm	Enzyme (Nitric oxide synthase)	Intracellular
CD11b	155 Gd	CD marker (Integrin \alpha-M)	Membrane, Intracellular
F480	156 Gd	GPCR (Adhesion)	Membrane, Intracellular
GAP43	157 Gd	Plasma protein (Nerve growth)	Intracellular
CD8a	158 Gd	CD marker (MHC I coreceptor)	Membrane, Intracellular
CD3e	159 Tb	CD marker (T-cell activation)	Membrane
HIF1A	160 Gd	Transcription Factor	Intracellular
Vimentin	163 Dy	Intermediate Filament	Intracellular
\alphaSMA	164 Dy	Contractile apparatus	Intracellular
TUJ1	176 Yb	Structural (Tubulin \beta-3)	Intracellular

Isotopic Precision and Signal Separation Targeting specific masses (e.g., 141Pr vs 143Nd) is critical for minimizing signal "bleed-through" in the high-plex mucosal environment. This isotopic precision allows for the simultaneous localization of receptors like H4R and lineage markers like CD3e, which is fundamental for quantifying the spatial interactions between different cell types in the lamina propria.

5. Functional Marker Analysis: Receptors and Signaling

The strategic selection of functional markers allows the repository to capture the dynamic signaling states that define histamine-driven pathology.

* Histamine Receptors (H1R, H2R, H4R): While H1R and H2R distributions are relatively stable, H4R serves as the primary mediator of the IBS-HH phenotype. Acting as a chemoattractant, H4R drives the recruitment of mast cells to the colonic mucosa.
* LPARs (1, 3, 5): Lysophosphatidic acid receptors provide a read-out of the inflammatory milieu. LPAR1 contributes to responses to tissue damage and infection agents, while LPAR3 acts as a mediator of diverse cellular activities.
* HIF1A: Identified as a master transcriptional regulator of the adaptive response to hypoxia, HIF1A expression maps the metabolic stress within the lymphoid and epithelial tissues of the colon.
* Ki-67: This proliferation marker aids in the rearrangement of chromosomes during mitosis; its localization within intestinal niches is essential for quantifying cellular turnover in response to microbially induced damage.

Pharmacological Validation The transformative insight of this study is the identification of the H4R-histamine axis as a targetable pathway. In vivo pharmacological blockade using JNJ-39758979 successfully inhibited visceral hypersensitivity and decreased colonic mast cell accumulation. Furthermore, in vitro chemotaxis assays using the antagonist JNJ-7777120 confirmed that microbially derived histamine directly recruits mast cells via H4R, providing a comprehensive signaling validation from bench to model.

6. Repository Usage and Data Access

This repository is an open-access resource for researchers focused on mucosal immunology, enteric neurobiology, and spatial proteomics.

Technical Instructions and Reproducibility To ensure experimental replication, users must adhere to the specific antibody metadata provided:

* Antibody Specifications: For MIBI replication, refer to the clones and lot numbers in the metadata/ folder (e.g., Clone EP1845Y for NaKATPase or Clone 240E11_ for Ecadherin).
* Staining Quality: Experimental success is dependent on the precise titres (ug/mL) listed in the panel metadata. Deviations from these concentrations will significantly impact the signal-to-noise ratio in ion beam imaging.
* Standard Sections:
  * Installation: Requirements for MIBI-tracker and image processing pipelines.
  * Data Structures: Architecture for raw .bin data and multi-channel .tiff stacks.
  * License: Standard academic data-sharing agreement.

Final Statement By integrating gnotobiotic mouse modeling with high-plex spatial proteomics, this resource provides a comprehensive map of the microbiota-gut-brain axis, advancing our understanding of how bacterial metabolites dictate the sensory landscape of the human gut.
