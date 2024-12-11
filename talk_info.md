
# Talk info

## Abstract 
Normalizing Flow models (NFs) are neural networks designed to allow approximate sampling from intractible probability densities, e.g., to generate data or sample from a posterior density.  This talk should give you the background to conceptually understand NFs and how to train them, as well as some working example code and use cases. 

More specifically, NFs are just neural networks that are diffeomorphisms, meaning as a function from inputs to outputs, they are bijective (one-to-one and onto) and differentialble. The fundamental theorem of NFs (I made that name up) is diffeomorphisms preserve probability densities. If you've had calculus, this theorem is easy to prove and you sort of already know it! The informs how to build the loss function to approximate a given target density. Then we can train an NF to transform an "easy" distribution (like a Gaussian normal distribution) to a "hard" distribution. Once trained the NF can be used to generate samples (approximately) from the hard distribution!

There are two use cases for NFs:
1. Approximate sampling from a data distribution: you have a dataset and you want to generate more data from the same distribution. (e.g. synthesize data!)
2. Approximate sampling from an improper density: you can compute some intractable probability density up to a constant, but you cannot sample from it. (e.g., sample froma posterior distribution!)

I'll show a demo of the second use case (code in this repo) of implementing a Planar NF and its generalization to a Sylvester NF to approximate an otherwise intractable density. 

## Prerequisites for understanding everything
- concepts: basic calculus and probability, KL divergence
- coding: python basics
- ML: basic neural networks 

## Git link: 
https://github.com/aidotse/normalizing-flows-tutorial/ 

## References
The survey of NFs is fantastic: https://jmlr.org/papers/volume22/19-1028/19-1028.pdf 

This lecture is really good for the learning NFs https://www.youtube.com/watch?v=RthYBGDk7lQ 

This implementation was helpful for learning planar NFs https://github.com/VishakhG/normalizing-flows 