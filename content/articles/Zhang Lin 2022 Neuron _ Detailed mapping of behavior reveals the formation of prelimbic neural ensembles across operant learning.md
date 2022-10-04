title: Zhang Lin 2022 Neuron _ Detailed mapping of behavior reveals the formation of prelimbic neural ensembles across operant learning
tags: #operant-conditioning [[prelimbic]] #miniscope #calcium-imaging #cool-methods #computation #behavior 
methods: operant conditioning, miniscope, mice, longitudinal calcium imaging, deep behavior mapping

# 1 Line
In a learned task, [[prelimbic]] neurons encode information about the mouse's behavioral state, and temporally proximal behaviors had a high degree of overlap between ensemble representations, resulting in a seemingly continuous and smooth representation of behavior. Suggests that prelimbic neurons facilitate the transition among behavioral states.

# Abstract


# Key points
FIG 1: examples of operant task, longitudinal imaging

FIG 2: depiction of Deep Behavior Mapping. Unsure of how unsupervised method is. Referred to as 'self-supervised'. 50 states total. Some task relevant, many not. 

FIG 3: breakdown of prelimbic neuronal tuning to behavioral microstates. Predicted activity of neurons based off its assigned category. But category activity is based on grouped neuronal activity? A little circular? Of note: ~25% of neurons did not encode anything, 50% encoded non-task variables. 

FIG 4: longitudinal analysis of beheavioral tuning of prelimbic neurons. Reward ensembles emerge as soon as reward is presented, suggesting that they are pre-existing prior to training. While task-related ensembles develop their tuning over time. Initial tuning of neurons strongly biased their final tuning, suggesting that prelimbic neurons encode behavior states somewhat independent of the context or conditional stimuli.

# Related
[[Kitamura...Tonegawa (2017) Science. Engrams and circuits crucial for systems consolidation of a memory]]
[[Tse...Morris (2007) Science. Schemas and Memory Consolidation]]
[[Zhou...Schoenbaum (2020) Nature. Evolving schema representations in orbitofrontal ensembles during learning]]

# Comments
Is the overlap between ensembles and sequential behaviors just simply a reflection that the behaviors are very similar? If the behaviors are all variations on interacting with the lever, it makes sense that those would be related

Has details on longitudinal alignment. Uses CaimAn for signal extraction

Did a bootstrap approach for tuning. Predicted the neuron's activity based on the behavioral state, and calculated the R2 value. Then shuffled activity. If R2 percentile was in top 5%, called it significant. 

# Figures