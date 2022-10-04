title: Grant...Otis (2021). Specialized coding patterns among dorsomedial prefrontal neuronal ensembles predict conditioned reward seeking. eLife
tags: [[PFC]] [[prelimbic]] #cool-methods #computation #calcium-imaging #reward #analysis #ensemble-analysis 
methods: 2P calcium imaging, Pavlovian reward conditioning

# 1 Line
Excitatory [[prelimbic]] neurons show a heterogenous response during Pavolovian reward learning, clustering into several groups with different task-event and reward dynamics, the most prominent of which show a decrease in activity late in learning.

# Abstract
In a Pavlovian reward conditioning task (CS+ to sucrose water delivery), using 2P head fixed calcium imaging, recorded excitatory (CamK2-GCaMP6s) responses across within-session trials and across days. Used PCA to identify multiple (5) clusters of responses to cue (both CS+ and CS-) and reward presentation. Some ensembles emerged early in learning, others late. 

# Key points
Previous work looked at [[PFC]] [[prelimbic]] specific projection populations and still observed heterogenous activity, though could be characterized by a 'general' response. Framed as a push-pull between heterogeneity of population activity vs finding appropriate level of grouping for cells (gene expression, afferent, efferent projection). 

The specific clustering algorithm chosen affected how many clusters were found, between 4 and 5. Noted limitation of clustering algorithms providing only a rough understanding of the possible groupings.

The cluster with the strongest behavioral correlation, also with the most decoding accuracy, was the cluster with an inhibitory response to CS+ cue onset. This dynamic evolved only in late-learning.

Using data from late-learning, total population activity could decode all elements of the task. Early-learning data, only some elements. 

Ensembles showed within-day and between-day stability of coding. This suggests that there are subgroupings of these ensembles (based on gene expression, projections, etc)

# Related
[[Otis, Namboodiri...Stuber (2017) Nature. Prefrontal cortex output circuits guide reward seeking through divergent cue encoding]]


# Comments
Can check this paper out for cool ideas on how to do PCA and analysis in a similar task
Analysis notes

#ensemble-analysis  METHODS
- Ensembles and Clustering
	- Generated peristimulus time histogram of responses for each cell, across CS presentation, for late learning session (1 session)
	- Then did PCA
		- chose number of PCs based on inflection point of scree plot, which shows numebr of PCs versus percent variance explained
		- Data projected onto PCs then fed into clustering algorithm
			- Used sklearn.cluster.SpectralClustering
	- After clustering, each neuron assigned a cluster label. Then used to track clusters over time. 
- Decoding
	- Done both on whole population and ensembles
	- Used a binary decoder, implented in Scikit-learn (sklearn.discriminant_analysis, sklearn.decompisition, sklearn.svm)
	- For total population encoding, decoding scores normalized to 'max vlaue for a decoded variable' ??
	- To determine if better than chance, compared to shuffled data using two-way ANOVA or one-way ANOVA
- Cell alignment
	- used spatial and morphological traits to align
	- then did corrleations at the cluster level across days. Compared to shuffled Cell IDs, to show that correlated activity requires accurate tracking

# Figures
![[Pasted image 20210719084444.png]]