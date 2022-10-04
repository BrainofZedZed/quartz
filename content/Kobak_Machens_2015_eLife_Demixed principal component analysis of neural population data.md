title: Kobak_Machens_2015_eLife_Demixed principal component analysis of neural population data
tags: #analysis #ensemble-analysis #cool-methods #computation 
methods: computation

# 1 Line
Developed a variation of PCA that allows components to be assigned to task parameters (or independent of task parameter).

# Abstract
Neurons in higher cortical areas, such as the prefrontal cortex, are often tuned to a variety of sensory and motor variables, and are therefore said to display mixed selectivity. This complexity of single neuron responses can obscure what information these areas represent and how it is represented. Here we demonstrate the advantages of a new dimensionality reduction technique, demixed principal component analysis (dPCA), that decomposes population activity into a few components. In addition to systematically capturing the majority of the variance of the data, dPCA also exposes the dependence of the neural representation on task parameters such as stimuli, decisions, or rewards. To illustrate our method we reanalyze population data from four datasets comprising different species, different cortical areas and different experimental tasks. In each case, dPCA provides a concise way of visualizing the data that summarizes the taskdependent features of the population response in a single figure.
![[Pasted image 20220819164134.png]]

# Key points
PFC neural responses can display “baffling heterogeneity”. Most neurons display mixed-selectivity.

Current dimensionality reduction approaches act without taking task parameters into account. Therefore, the mixed selectivity of cells which respond to multiple task parameters, is still present in the reduced data space.

Authors created demixed principal component analysis (dPCA). Aims to find a decomposition of the data into latent components that 1) are easily interpretable with respect to task parameters, 2) preserve original data as much as possible (to not throw away anything useful).

Common existing methods of relating neural activity to task parameter are to use statistical test (ANOVA, ROC Curve). This yields one single population, that can be averaged to get one ‘component’ for each parameter. This is supervised (feed it the parameter).

PCA is an unsupervised approach, capturing more components and more variance. But task parameter info is not taking into account, resulting in mixed components that are hard to interpret with regard to task structure.

‘Demixing’ finds a decoder (linear discriminator) of the neural activity that separates the different stimuli, ignoring any time-dependency. But LDA does not preserve the ‘geometry’ of the original neurla activity.

Compression aims to find a linear mapping (decoder) that reduces the dimensionality and preserves the original data as much as possible. This is the PCA approach. But fails to separate stimuli.

In dPCA, changes made to standard PCA approach. Compression and decompression (encoding / decoding) reconstructs not neural activity directly, but neural activity averaged over trials for a parameter.

dPCA output gives PCs but they are labeled with a condition-independent term, a task parameter term, or an interaction of task parameters term. To assess whether tuning was significant, used each component as a linear decoder to classify conditions (stimulus component to classify stimulus).

! For tasks in which trials have different lengths (eg freezing, platform), “restretch” the activity rates (time-warp) in each trial.

“In both olfactory datasets trials were self-paced. Accordingly, trials last different amounts of time, and firing rates cannot simply be averaged over trials. We used the following time warping (restretching) procedure to equalize the length of all trials and to align several events of interest (Figure 10) separately in each dataset. We defined five alignment events: odor poke in, odor poke out, water poke in, reward delivery, and water poke out. First, we aligned all trials on odor poke in (T1 ¼ 0) and computed median times of the four other events Ti; i ¼ 2 . . . 5 (for the time of reward delivery, we took the median over all correct trials). Second, we set DT to be the minimal waiting time between water port entry and reward delivery across the whole experiment (DT ¼ 0:2 s for the olfactory discrimination task and DT ¼ 0:3 s for the olfactory categorization task). Finally, for each trial with instantaneous firing rate xðtÞ we set ti; i ¼ 1 . . . 5, to be the times of alignment events on this particular trial (for error trials we took t4 ¼ t3 þ DT), and stretched xðtÞ along the time axis in a piecewise-linear manner to align each ti with the corresponding Ti.” (Kobak et al., 2016, p. 26)

Of note

-   Across all examples, condition-independent components explains the majority (60-90%) of the variance. This could relate overall firing rate changes during certain task periods, but also vary across time, like motor, attentional, breathing states.
    
-   dPCA allows component axes to be non-orthogonal (though most tend to be). Non-orthogonality means that neurons expressing one component tended to also express the other one.
    

Limitations

-   Only works with discrete parameters, and all combinations of parameters must be used as encoders.
    
-   Cannot handle missing data.
    
-   Needs sufficiently large number of neurons, ~100 for 3 task parameters.

# Related


# Comments


# Figures