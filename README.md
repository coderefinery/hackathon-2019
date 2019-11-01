

# CodeRefinery Hackathon 2019

Stockholm Nov 6-7, 2019

Event website: https://coderefinery.org/events/2019-11-06-stockholm/


## Projects

### 1. Improve training material for inter-service-communication on Kubernetes (Carsten Thiel and colleagues)

This project is about improving [CESSDA](https://www.cessda.eu) training
material for an internal training in December. This is mostly focussed around
microservice architecture and inter-service-communication as well as automated
testing with quality gates/linting and ultimately running on our Kubernetes
setup.  The plan is to do this based on a virtual
[CESSDA](https://www.cessda.eu) Café consisting of a cashier, coffee
machine(s), and a waiter.  The components are ready and at the December
training participants will bring their own dockerised coffee machine along and
then deploy it in a continuous integration service with tests and running in
the Café by the end.

The goal is to make this material as re-usable as possible and would welcome
collaboration on the less CESSDA-specific (i.e. our Kubernetes) parts.


### 2. Efficient implementation of the bootstrap particle filter in Julia using StaticArrays (Samuel Wiqvist)

To run the pseudo-marginal Metropolis-Hastings algorithm [1] fast for
state-space models is it of importance to efficiently estimate the likelihood
numerically with a bootstrap filter [3] (or some other sequential Monte Carlo
algorithm). Therefore, this project aims to implement a bootstrap particle
filter using the static array support in Julia
(https://github.com/JuliaArrays/StaticArrays.jl). Using the StaticArray
support in Julia could potentially improve the performance of the particle
filter quite a bit (we could perhaps achieve a 10x speed-up). A starting point
could be to implement the static bootstrap filter for the simple example
"example 1" in [2]. However, an extension could be to implement a generic
filter, for instance using functional programming and/or metaprogramming.

[1] Andrieu, Christophe, Arnaud Doucet, and Roman Holenstein. "Particle markov chain monte carlo methods."
Journal of the Royal Statistical Society: Series B (Statistical Methodology) 72.3 (2010): 269-342.

[2] Cappé, Olivier, Simon J. Godsill, and Eric Moulines. "An overview of existing methods and recent advances in sequential Monte Carlo."
Proceedings of the IEEE 95.5 (2007): 899-924.

[3] Gordon, Neil J., David J. Salmond, and Adrian FM Smith. "Novel approach to nonlinear/non-Gaussian Bayesian state estimation."
IEE proceedings F (radar and signal processing). Vol. 140. No. 2. IET Digital Library, 1993.
