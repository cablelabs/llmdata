# LLM Data Companion
This repository contains companion data sets for LLM 
publications.

## AI-Assisted Ideation
Companion data to
`Randomness Is All You Need: Semantic Traversal of Problem-Solution Spaces with Large Language Models`

Please cite that paper if making use of this data.

The generated data dumps are available in  [/aidea](aidea/).

They are organize by original problem statement that generated
them:

| Data | Problem Statement |
|:---|:---|
| timeline | Software project timelines are often underestimated, which leads to high costs. |
| employee | It is difficult to measure employee satisfaction in an unbiased way. |
| startup | It is not easy for early startups to find a customer base willing to try new technology. |
| data | Companies struggle with gaining insights from large volumes and high velocity of data. |
| satisfaction | It is hard to track and measure customer satisfaction across large geographies. |
| invest | It is difficult to plan investments in an uncertain economy. |
| innovation | It is difficult to create innovation opportunities without introducing too much process and hampering creativity. |
| talent | Retaining high-performing talent is hard in competitive emerging markets. |
| ml | Large machine learning models are expensive and time consuming to train. |
| privacy | Ensuring privacy of customers is difficult while leveraging their data for business insights. |

Problems generated from solutions have the prefix `gprob`.
The solution they are generated from has the prefix `gsol`.

The file naming convention is: 
```
<type>.<index>.<temperature>.txt
```
where `type` can be `gsol`, `gprob`, `sol` or `prob` for solutions for generated
problems, generated problems, solutions and problems respectively. The
`index` denotes the order in which the solution was generated, starting
with solution 1 which is the solution to the original problem. The ordering
is determined by a depth-first search of the related problem and generated
problem tree. The `temperature` is the LLM temperature set during solution
and problem generation from a prompt. The temperatures used include `0.5`,`0.6`,`0.7`,`0.8`, `0.9`,
`1.0`, and `1.1`. The actual temperature fed into the LLM is a uniform random number 
in the interval `[temp,temp + 0.1]`.
