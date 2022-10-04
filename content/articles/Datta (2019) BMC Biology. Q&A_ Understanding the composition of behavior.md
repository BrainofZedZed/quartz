created: 20201005152529780
first_author: Datta
journal: BMC Biology
last_author: 
methods: review
modified: 20210504034006412
species: 
tags: [[computational modeling]] behavior technique MoSeQ
title: Datta (2019) BMC Biology. Q&A: Understanding the composition of behavior
type: text/vnd.tiddlywiki
year: 2019


!!Summary
Datta lab (Harvard) has developed [[MoSeq]] (for Motion Sequencing), an algorithm to identify the behavioral structure of mice. The article is a Question and Answer session going over how MoSeq works.

It uses a top down, 3D camera for pose estimation, then a generative computation model to identify behavioral 'modules' to understand the behavioral 'grammar'.

Behavioral modules are unique, single units. Different modules combine into a new module (eg 'chewing gum' and 'walking' modules combine into 'chewing gum and walking' module).

Fundamental assertion of MoSeq is that behaviors are flexibly composed from a finite set of stereotyped, repeated components.

Human annotation of behavior biases the behaviors toward those readily identified (and relevant) to humans. 

Organizes behavior into sub-second structure. Argues that this is empirically detectable in the data, and is at a similar timescale for relevant information processing (eg cortico-striato-thalamic loop). Even so, there are larger timescale behaviors that MoSeq misses (eg sleeping vs awake). 

CURRENT LIMITATIONS:

* requires 3D camera, inherently lower resolution than many 2D camera
* requires single mouse, simple arenas
* ignores limb and whisker information; only concerned with overall pose
* currently requires coding skills and detailed knowledge of algorithm (but working on user friendly version)

!!Related concepts
* [[DeepLabCut]]

!!Key points