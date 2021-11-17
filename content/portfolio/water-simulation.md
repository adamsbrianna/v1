+++
draft = false
image = ""
showonlyimage = false
date = "2021-11-05T20:22:08+05:30"
title = "Shallow Water Simulation"
weight = 7
+++

{{< rawhtml >}} 

<img src="/img/portfolio/dam_break.gif" 
     style="max-width: 100%;" />

{{< /rawhtml >}}


<!--more-->

Structured grid computations are particularly common in fluid dynamics simulations, and the code being studied is an example of such a simulation. This project involves optimizing and parallelizing a finite volume solver for the shallow water equations, a two-dimensional PDE system that describes waves that are very long compared to the water depth. This is an important system of equations that applies even in situations that you might not initially think of as "shallow"; for example, tsunami waves are long enough that they can be modeled using the shallow water equations even when traveling over mile-deep parts of oceans. 

The purpose is to improve the performance of a shallow water simulation.

There are three tasks:

    Parallelization: parallelize code using OpenMP.

    Scaling study: Run strong and weak scaling studies analyses on Comet
    to evaluate the performance with varying numbers of processors and 
    problem sizes.

    Profiling and tuning: Look for bottlenecks in the code to optimize the simulation even further.
{{< rawhtml >}} 
<br>
{{< /rawhtml >}}
The problem domain is divided into subdomains and each subdomain is handled by a thread, allowing for parallel processing of the computations. We ran experiments on Comet to evaluate how the parallelized problem scales. The speedup plot showed us that there's an increase in speed with an increase in processors and a maximum speedup of 24.08 with 24 processors which lines up with the expectation that the speedup should be less than or equal to the number of processors. The slight variance between these values is likely negligible and stems from minute changes among running the script or overheads of managing the threads. 

In order to evaluate the execution of the code and discover potential bottlenecks the code was profiled with gperftools and valgrind/callgrind. Vectorization is another method that we experimented with for optimization. The profiling results indicate that the functions calculating the limited derivatives might profit from tuning, so we attempted vectorization of some of the involved functions. Combining the vectorization of both limited_deriv functions reduces the execution time from 13.9s to 10.6s Increasing the number of threads to 24 on Comet leads to an execution time of 2.911994s without vectorization and 2.219870s with vectorization. This brings the speedup from around 24.1 to 31.6.

Through parallelisation and some vectorization we were able to drastically reduce the execution latency of the simulation. Our efforts resulted in a speedup of 31.6 for a problem of size 1000, run on comet with 24 threads. These results were in line with the speedup that we predicted in our performance model. 
