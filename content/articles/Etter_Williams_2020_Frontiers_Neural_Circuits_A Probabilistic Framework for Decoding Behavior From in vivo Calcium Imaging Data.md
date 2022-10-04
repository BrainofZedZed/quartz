title: Etter_Williams_2020_Frontiers_Neural_Circuits_A Probabilistic Framework for Decoding Behavior From in vivo Calcium Imaging Data
tags: #cool-methods #computation #calcium-imaging 
methods:

# 1 Line
Easy to follow guide on how to use Bayesian decoding with behavior and miniscope data

# Abstract


# Key points
ESTABLISHING PROBABILISTIC NEURAL TUNING CURVES

Signal processing:

-   first filtered high frequency fluctations
-   then discriminated periods of activity vs inactivity using two criteria
    -   sufficiently large signal amplitude (2 sd)
    -   first order derivative is positive (ie rise period)
-   then binarized

then using binarized activity, calculate probability of neuron being active

-   P(A) = active time / total time

P(A) similar to marginal likelihood in Bayesian context.

then compute probability of behavioral state
-   P(S) = time in state / total time
	- P(S) corresponds to the prior.

Then look at the joint probability
-   P (S and A) = time neuron active in state / total time (active and in state)
    

Then compute the probability a cell is active given the animal is in the state

-   P(A|S) = time active in state / time in state
    -   this can be interpreted as a tuning curve
    -   = Bayesian likelihood


Then can do Bayesian inference, inferring probability that the behavior state (S) is occurring given the neuronal activity (A)

-   P(S|A) = (P(A|S) * P(S)) / P(A)
    -   P(S|A) is the posterior

to test significance, use circularly shuffled distribution

-   Test if activity falls outside 95% of shuffled datapoints (alpha = 0.05)
    

DECODING BEHAVIOR FROM CALCIUM IMAGING DATA

(assumes all neurons are independent, which isn’t totally true)
Can rewrite equation to use tuning curves from multiple neurons
![[Pasted image 20221003163437.png]]
However this rewriting can lead to numerical underflow in many softwares. Need to rewrite it using log form
![[Pasted image 20221003163707.png]]

To assess decoder accuracy, authors propose using:  decoder agreement and decoder error
	Decoder agreement is portion of time where state of mouse was successfully decoded
	Decoding error is distance between decoded behavior and actual behavior

Interestingly:  did in vitro ephys + 1P recording to look at different Ca++ data binarizing methods. Found deconvolution the most effective. But using in vivo data, found deconvolved to have less clear place fields, but still had approximately similar decoder error compared to their described binarizing method

# Related


# Comments

# Figures