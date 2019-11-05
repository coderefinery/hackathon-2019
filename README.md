

# CodeRefinery Hackathon 2019

Stockholm Nov 6-7, 2019

Event website: https://coderefinery.org/events/2019-11-06-stockholm/


## Projects

### 1. Improve training material for inter-service-communication on Kubernetes (Carsten Thiel and colleagues)

This project is about improving [CESSDA](https://www.cessda.eu) training material for 
[an internal training in December](https://www.cessda.eu/News-Events/Events/CESSDA-Technical-Infrastructure-Training-Day). This is mostly focussed on microservice architecture and inter-service-communication as well as 
on automated testing with quality gates & linting.
The services will be dockerised and running on Kubernetes.

The plan is to do this based on a virtual [CESSDA](https://www.cessda.eu) Café 
consisting of a cashier, coffee machine(s), and a waiter, for which we have example components ready.
At the December training, participants will bring along their own dockerised coffee machines,
run them through our continuous integration service and deploy them to the full Café.

The goal is to make this material as re-usable as possible also outside of CESSDA.
We would therefore welcome collaboration, in particular on the generic parts.


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


### 3. Create something interesting with our anonymized pre- and post-workshop survey results (Thor Wikfeldt)

When participants sign up for CodeRefinery workshops, they are asked to fill 
a pre-workshop survey [1]. The idea behind this survey is for the instructors 
to get an idea of who the participants are, what their background and experience 
is and what they are most interested in learning about. 

3-6 months after attending a workshop, past workshop participants are asked to fill 
another post-workshop survey which explores what, if anything, has changed in the 
way they develop code for research as a result of attending a workshop [2].

After 25 delivered workshops with over 600 participants, we have plenty of 
interesting data, but so far this data has only been analyzed superficially. 
In this project, we will dive into the details and bring to light all the
interesting trends and hidden correlations which may be hiding in the survey results!

[1] https://github.com/coderefinery/pre-workshop-survey

[2] https://github.com/coderefinery/post-workshop-survey


### 4. Update the style of CodeRefinery lessons to match https://github.com/carpentries/styles/ (Radovan Bast)

At some point CodeRefinery lessons had the same styling as Carpentries lessons
but both evolved a bit since and I think CodeRefinery lessons could benefit
from a face-lift. Not only to make the material look better, but also to make
it look more familiar to the Carpentries community and simplify uptake there.


### 5. Create a web app which can update forked branches (Radovan Bast)

Creating forks on GitHub is simple but updating forks is not easy for persons
who are not familiar or comfortable with the command line. Here we would
create an app to which one could log in using GitHub and refresh forks with a
button click. For simplicity we would allow updating forked branches only if a
fast-forward is possible.

Tech stack to be discussed but would probably involve https://vuejs.org
and https://graphql.org/learn/.


### 6. Parallel computing on HPC systems (Emiliano Molinaro)

A usual problem for a researcher working on heavy computational workflows is to scale up her/his calculation on multiple devices. Common practise is to do the development on premises and deploy the code on an HPC cluster. Here we would like to discuss examples in which the same code can be parallelized with only minor changes, keeping a SIMD/SPMD programming style. Some starting points could be: 1) how to parallelize C/C++/Fortran code with MPI on a cluster; 2) distributed calculation on multiple nodes in Python using Dask; 3) compare different parallel options for R (doSNOW, doMC, RMPI, mclapply, parLapply); 4) how to use a Spark cluster for parallel processing of big datasets.


### 7. Make lessons more relevant for R community (Sabry Razick)

R has the most advantages when it comes to data exploration with least coding
skills. So I want to try to make a short exploring-data-with-R course where we
can use snippets to integrate with Git and documentation.

There are some topics that would be more accessible to R users if they were
rewritten or adapted to R based tools. As an example lots of functionality of
Jupyter is available as notebooks via R Markdown. In addition there are plenty
of other R markdown based formats that is of support to attempts of using
literate programming and/or generating reports.

### 8. Terminal

We have tool that provides a way for the learners to see what were the commands
used by the instructor through a browser.
e.g http://folk.uio.no/sabryr/history.html. This is useful when the learners
fall behind. This is in a development stage and has basic guard against accidental
typing in a password for example.  Biggest obstacle is that for this tool we need
a web server already configured. Objective of the hackathon is to make this tool
usable more universally. What we have now https://github.com/Sabryr/Tavatar
