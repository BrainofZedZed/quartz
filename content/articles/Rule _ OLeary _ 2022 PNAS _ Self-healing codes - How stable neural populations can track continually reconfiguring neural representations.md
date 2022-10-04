title: Rule _ OLeary _ 2022 PNAS _ Self-healing codes - How stable neural populations can track continually reconfiguring neural representations
tags: #computation  #computational-modeling #theory #drift #representational-drift [[representational drift]] 
methods: modeling

# 1 Line
Authors propose a combination of Hebbian and homeostatic mechanisms to facilitate highly plastic circuits to interact reliably and predictably with rigid representations.

# Abstract


# Key points
How to reconcile representational drift (dynamic reorganization of neural activity with stable circuit-level properties) Recent observations show that neural circuits can preserve learned associations and representations while individual neurons have changing functional roles. 

One idea is that the preservation of those representations and associations is due to a redundant, distributed readout mechanism -- that changes to some neurons are offset by changes to others. How this is executed with known cellular mechanisms is unknown. Authors propose a combination of Hebbian and homeostatic mechanisms to facilitate highly plastic circuits to interact reliably and predictably with rigid representations. The intereaction of Hebbian and homeostatic mechanisms "self-heals" the readout. Major novelty is re-interpreting Hebbian plasticity as a player in maintaining associations, not just learning new ones. This allows drift to be tracked using only internally generated signals without the need for error feedback. Also propose how dynamic representations can be tracked over long periods of time if the readout population encodes a stable predictive model of the variables being represented. 

Argues that representational drift isn't random and the patterns within drift can be used to create legible readout. The "topology and course geometry" (ie PCs?) of drift appears consistent over time, therefore the statistical structure of external variables is preserved without the need for neuron-wise encoding. 

Used modeling to provide evidence for their ideas. 

The self-healing codes of representation have a hierarchy of components: 1) single-cell tuning with redundant tiling of encoded variables (which make population codes robust to small amounts of drift), 2) populations that use their own output as a training signal to update decoding weights, 3) circuit interactions that track evolving population statistics using stable internal models. 

>"The encoding population is free to reconfigure its encoding arbitrarily. However, any change in the code leads to a complementary change in how that code is read out."

# Related
[[Schoonover Fink 2020 Nature Representational drift in primary olfactory cortex]]

[[DeNardo...Luo (2019) Nature Neuroscience. Temporal evolution of cortical ensembles promoting remote memory retrieval]]

[[Driscoll _ Harvey _ 2017 Cell _ Dynamic Reorganization of Neuronal Activity Patterns in Parietal Cortex]]

# Comments
This really makes me rethink the idea of drift in my project. Drift refers to representing the same stimulus with different activity. [[systems consolidation]] is different. It's about changing the circuits involved in representation, while drift is about the changing individual neuronal tuning in the computation. 

# Figures