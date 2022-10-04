title: Pereira...Murthy (2020) Nat Neuro. Quantifying behavior to understand the brain
tags: #review #deeplabcut #computation #tracking
methods:

# 1 Line
Detailed overview of methods behind popular animal tracking techniques, as well as an overview of their differences along with advatnages and disadvantages.

# Abstract


# Key points
### Tracking 
Coarsest quantification of animal behavior is to track its centroid, treating animal behavior as a single point. Can model animal as ellipse, detecting heading and angle as well. Animal pose estimation tracks limbs and joints of animals. Rich literature on human pose estimation (eg facial recognition). Heatmaps / confidence map representation of landmark locations encodes the location of each landmark as a density function of a 2D Gaussian distribution centered on the ground truth image coordinates of each landmark. This compares the probability of each tracked point being assigned to each landmark. Convolutional neural nets (CNNs) are well-suited for this. Problem of having the training dataset to compare the tracked points to. One approach is to use transfer learning to apply the parameters learned from a broad set of images to a specific set of images, allowing fine-tuning and minimizing the need for learning. 
### Quantifying the dynamics of behavior 
Simplest way to define behavior is to have fixed set of rules parameterizing the behavior. This maay fail to capture the variability of a behavior. A more flexible approach is to use computer-aided classification via supervised machine learning -- though this still suffers from the bias of humans annotating the behavioral examples. Another alternative to have computer learning identify clusters of distinct states. Typially, dimensionality reduction and feature extraction (PCA, t-SNE (t-stochastic neighbor embedding) are applied to raw data (post estimation). The similarity between points is quantified (Euclidean distance). Clustering then attempts to group all points such that each cluster is more similar to its within-group members than its outside-group members. Popular methods such as k-means and Guassian mixed models require a priori assumptions of the numbers of clusters. Density based clustering (watershed transformation) avoid a priori estimates of cluster number, by identifying "peaks in the estimated distribution of time points in the space of extracted features". Clusters will be self-similar, but may not neatly fit into human labels. One problem is these identify combinations of behaviors (walking and sniffing) as a distinct behavior, not as from its component parts. Hidden Markov models are popular, with explciit modeling of the characteritstics defining behavioral systems. 
# Related

# Comments

# Figures