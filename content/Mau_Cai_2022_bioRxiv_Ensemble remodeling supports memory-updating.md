title: Mau_Cai_2022_bioRxiv_Ensemble remodeling supports memory-updating
tags: #learning [[hippocampus]] #ensemble #miniscope #analysis #cool-methods #ensemble-analysis
methods: zero maze with reward zones, reversal learning, mice, miniscope

# 1 Line
Memory updating is reflected by remodeling of hippocampal ensembles.

# Abstract
Memory-updating is critical in dynamic environments because updating memories with new information promotes versatility. However, little is known about how memories are updated with new information. To study how neuronal ensembles might support memory-updating, we used a hippocampus-dependent spatial reversal task to measure hippocampal ensemble dynamics when mice switched navigational goals. Using Miniscope calcium imaging, we identified neuronal ensembles (co-active neurons) in dorsal CA1 that were spatially tuned and stable across training sessions. When reward locations were moved during a reversal session, a subset of these ensembles decreased their activation strength, correlating with memory-updating. These “remodeling” ensembles were a result of weakly-connected neurons becoming less co-active with their peers. Middle-aged mice were impaired in reversal learning, and the prevalence of their remodeling ensembles correlated with their memory-updating performance. Therefore, we have identified a mechanism where the hippocampus breaks down ensembles to support memory-updating.


# Key points
FIG 1 - No global or rate remapping following relearning of spatial reward maze.

FIG 2 - Co-active neurons form ensembles that contain info about space and behavior.

Identified ~50 ensembles per session, with around 3% total population membership within each ensemble (if 1000 neurons, around 30 each). The size of ensembles did not change over time.

FIG 3 - A subset of CA1 ensembles remodel during memory-updating, correlating with enhanced behavioral performance

FIG 4 - Ensembles remodel due to decoupling of weakly-connected neurons

FIG 5 - Middle-aged mice have reversal learning deficit that correlates with presence of fewer remodeling ensembles.

# Related
[[Mau...Cai (2020) eLife The brain in motion How ensemble fluidity drives memory-updating and flexibility]]


# Comments
Helpful methods on ensemble analysis.
METHODS

Averaged almost 1000 neurons per animal!

Used calcium event rate. Unspecified how calcium event was calculated.

ENSEMBLE GENERATION:

>Used unsupervised PCA then ICA to generate ensembles. “Binarized calcium activity was smoothed using a 5-bin moving average (~300 ms, slightly larger than a single theta cycle) and z-scored. Using this activity matrix, we performed PCA and compared the eigenvalues of each principal component to a surrogate distribution of eigenvalues, created using activity matrices where all neurons had their activities circularly shuffled relative to each other, repeated 500 times. The number of ensembles (independent components) was the number of principal components that had eigenvalues higher than 99% (p < 0.01) of the eigenvalues from the surrogate distribution. We then use this number as the number of independent components to be extracted with fast-ICA algorithm. Each ensemble (independent component) has a weight vector representing the contribution of each neuron to the ensemble, , and neurons were considered ensemble members if their weight exceeded 2 standard deviations above the mean of that ensemble. We then used the outer product of the weight vector to produce the projection matrix P, which can be used to project neural activity into ensemble activation strength. To compute the activation strength of each ensemble at each temporal bin b, we used the formula: 𝑅𝑏 = 𝑍𝑏𝑇𝑃𝑍𝑏 Where 𝑍𝑏 is the normalized calcium activity at time bin b, and P is the projection matrix, with the main diagonal set to zero to ensure that calcium activity of a single neuron does not contribute to the ensemble strength Rb. Ensembles were classified as “remodeled” using the non-parametric Mann-Kendall trend test97. For an ensemble to be called a remodeled ensemble, its activation strength needed to have a negative slope across time and p<0.005 after Šidák correction for multiple comparisons across all ensembles.” (Mau and Cai, p. 24)

ALIGNMENT

Aligned cells using CellReg. Aligned ensembles by first aligning cells then ‘computed cosine similarities between each ensemble pair’s weight vectors’.
# Figures