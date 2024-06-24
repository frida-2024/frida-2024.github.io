---
layout: home
---

# The 11th Workshop on Formal Reasoning in Distributed Algorithms

Date: Tuesday July 23rd, 2024

Location: Montreal, Canada

The workshop is organized as part of [CAV 2024](https://i-cav.org/2024/).

## Speakers

If you would like to participate as a speaker, please send an abstract as soon as possible to [Swen Jacobs](https://cispa.de/en/people/swen.jacobs) and [Giuliano Losa](https://www.losa.fr/).
We welcome talks on recent published or unpublished research as well as new and exploratory ideas.
See below for the topics of interest.

### Confirmed Speakers

* [Borzoo Bonakdarpour](http://www.cse.msu.edu/~borzoo/), Michigan State University
    <details>
    <summary>Fault-tolerant Distributed Runtime Monitoring (click the arrow to expand the abstract)</summary>
      <br>
      <p>
      Monitoring distributed applications that do not share a global clock is highly challenging as the monitor has to potentially deal with a combinatorial enumeration at run time. We also have every reason to believe that distributed monitors are not necessarily perfect and monitors are subject to all types of faults that normal distributed processes are. In this talk, I will present our results on runtime verification of distributed systems. We make a practical assumption that the distributed system under scrutiny is augmented with a clock synchronization algorithm that guarantees bounded clock skew among all processes. Second, we do not make any assumption about the structure of the formal specification under inspection. We introduce a set of distributed monitoring algorithms by employing SMT-solving that range over discrete distributed systems such as databases to cyber-physical systems such as network of autonomous vehicles. I will also present real-world case studies and demonstrate that scalable online monitoring of distributed applications is within our reach.
      </p>
    </details>
* [Thomas Wies](https://cs.nyu.edu/~wies/), NYU
* [Marco Eilers](https://www.pm.inf.ethz.ch/people/personal/meilers-pers.html), ETHZ
    <details>
    <summary>verifiedSCION: Verified Secure Routing (click the arrow to expand the abstract)</summary>
    <br>
    <p>
    SCION is a new Internet architecture that addresses many of the security vulnerabilities of today’s Internet. Its clean-slate design provides, among other properties, route control, failure isolation, and multi-path communication. The verifiedSCION project is an effort to formally verify the correctness and security of SCION. It aims to provide strong guarantees for the entire architecture, from the protocol design to its concrete implementation.
    The key step to achieving these guarantees is to formally connect a model of the entire SCION network, about which we can prove global properties, to correctness proofs of individual router implementations.
    This talk will give an overview of the verifiedSCION project and explain, in particular, how we extract specifications for individual components from a global model of a distributed system using refinement and decomposition, and how we then verify each component against its specification using deductive program verification in separation logic.
    </p>
    </details>
* [Eric Koskinen](https://www.erickoskinen.com/#/), Stevens Institute of Technology
    <details>
    <summary>Commutativity Verification/Inference for Automatic Parallelization</summary>
    </details>

* [Siddhartha Jayanti](https://sites.google.com/view/siddhartha-jayanti/research), Google Research and AI
    <details>
    <summary>Machine-Verifying Complex and Deployed Multiprocess Data Structures</summary>
    <br>
    <p>
    I will talk about machine-verifying the correctness of concurrent data structures via the universal and complete Meta-Configurations Tracking verification method for proving linearizability. We have used this method to prove algorithms with famously complex and future-dependent linearization structures and those which have been impactfully deployed in practice. We demonstrate the simplicity and power of our method by producing proofs of linearizability for the Herlihy-Wing queue and Jayanti’s single-scanner snapshot, as well as a proof of strong linearizability of the Jayanti-Tarjan union-find object, which is deployed in Google's open-source graph mining library to enable the clustering billion-scale data. All three of these proofs are machine-verified by TLAPS (the TLA+ Proof System).
    </p>
    <p>
    Bio: Siddhartha Jayanti is a Research Scientist at Google Research, Cambridge, MA. He is an algorithmist, whose work spans distributed systems, machine learning, economics and computing, security, and verification. Siddhartha earned his Ph.D. in Computer Science with a minor in Machine Learning from MIT, where he was advised by Julian Shun. He received his Master's from MIT under the guidance of Costis Daskalakis, and his Bachelor's from Princeton, where his thesis was advised by Robert Tarjan and his research on mathematics in Sanskrit was advised by Manjul Bhargava.
    </p>
    </details>
* [Isaac Sheff](https://isaacsheff.com/), Heliax
* [Nicholas V. Lewchenko](https://www.octalsrc.org/research), University of Colorado Boulder
    <details>
    <summary>Bolt-On Strong Consistency: Specification, Implementation, and Verification (click the arrow to expand the abstract)</summary>
    <br>
    <p>
    Strongly-consistent replicated data stores are a popular foundation for many kinds of online services, but their implementations are very complex. Strong replication is not ‘available’ under network partitions, and so achieving a functional degree of fault-tolerance requires correctly implementing ‘consensus algorithms’ like Raft and Paxos. These algorithms are notoriously difficult to reason about, and many data stores implement custom variations to support unique performance tradeoffs, presenting an opportunity for automated verification tools. Unfortunately, existing tools that have been applied to distributed consensus demand too much developer effort, a problem stemming from the low-level programming model in which consensus and strong replication are implemented—asynchronous message passing—which thwarts decidable automation by exposing the details of communication and the structure of the distributed network.
    </p>

    <p>
In this talk, I will explore an alternative approach: the implementation and verification of strong replication systems *as applications of* weak replicated data stores. Weak stores, being available under partition, are a suitable foundation for performant distributed applications. At the same time, they abstract asynchronous communication and allow us to derive local-scope conditions for the verification of consensus safety. To evaluate this approach, we have developed a verified-programming framework for the weak replicated state model, called ‘Super-V’. This framework enables SMT-based verification based on local-scope artifacts called ‘strong update preconditions’, improving on standard-practice global inductive invariants in both decidability by the solver and ease of discovery by the developer. I will demonstrate how this framework can be used to implement and verify a strong replication system based on an adaptation of the Raft consensus algorithm, and discuss the performance implications of this approach.
    </p>
    </details>
* [Stephen Siegel](https://vsl.cis.udel.edu/siegel.html), University of Delaware
    <details>
    <summary>Challenge Problems in Verification of MPI Programs (click the arrow to expand the abstract)</summary>
    <br>
    <p>
    MPI (Message Passing Interface) is the standard interface for writing distributed-memory parallel programs for scientific and high performance computing.   While MPI is a large library, the core functions, which suffice for expressing most algorithms, provide a simple interface with well-behaved properties, e.g., messages are never dropped and message order is preserved.  One of the main challenges in scientific computing is the mechanistic verification of programs written in C, C++, or Fortran and using MPI.   There has been some success in verifying such programs within small bounds on the number of processes, using model checking and symbolic execution techniques.  There has also been work on parameterized verification of these programs.  In this talk I will summarize MPI and show some examples of what has been accomplished so far, as well as examples for which current verification technology is insufficient.  Can ideas from distributed system verification help us solve these problems?
    </p>
    </details>
* [Kostis Sagonas](https://www.ece.ntua.gr/en/staff/77), Uppsala University, Sweden and NTUA, Greece
    <details>
    <summary>Testing and Verifying Concurrency Algorithms using Stateless Model Checking</summary>
    </details>
* [Giuliano Losa](https://www.losa.fr), Stellar Development Foundation
    <details>
    <summary>From Federated Byzantine Agreement to 3-valued logic</summary>
    </details>

## Topics of Interest

The topics of interest for the FRIDA workshop include the following, as they apply to distributed algorithms and systems:

* formal modeling
* model checking
* interactive theorem proving
* parameterized model checking
* integration of different verification techniques
* benchmarking
* synthesis
* run-time verification
* testing
* invariant inference

## Organizers

[Swen Jacobs](https://cispa.de/en/people/swen.jacobs) and [Giuliano Losa](https://www.losa.fr/)

### With support of

[Stephan Merz](https://members.loria.fr/Stephan.Merz/), [Marijana Lazić](https://www.cs.cit.tum.de/tcs/personen/marijana-lazic/#c26286), Igor Konnov, and Joseph Widder

## Previous editions

Starting a productive dialogue between distributed algorithms and verification communities was the goal of a successful [Dagstuhl Seminar “Formal Verification of Distributed Algorithms”](https://www.dagstuhl.de/en/program/calendar/semhp/?semnr=13141) which was held in April 2013. During this seminar, the participants agreed that a series of workshops should be held in order to strengthen the community that does research on these issues.
The FRIDA workshop then took place every year since 2014.

The [1st workshop on Formal Reasoning in Distributed
Algorithms](https://easychair.org/smart-program/VSL2014/FRIDA-index.html) took
place in Vienna as part of the Vienna Summer of Logic’14 and Federated Logic
Conference’14. The [2nd FRIDA
workshop](http://discotec2015.inria.fr/workshops/frida-2015/) took place in
Grenoble as part of FORTE’15. The [3rd FRIDA
workshop](https://forsyte.at/events/frida2016/) was organized in Marrakech as
part of NETYS’16. The [4th FRIDA
workshop](https://forsyte.at/events/frida2017/) took place in Vienna as part of
DISC 2017. The [5th FRIDA workshop](https://forsyte.at/events/frida2018/) was
co-located with CAV 2018, which was held as part of the Federated Logic
Conference (FLoC). The [6th
workshop](https://team.inria.fr/veridis/events/frida2019/) was co-located with
DISC 2019 in Budapest, Hungary.
Finally, [FRIDA 2020](https://frida2020.galois.com/) and [FRIDA 2021](https://frida-2021.github.io) took place as online workshops at QONFEST
2020 and DISC 2021, respectively.
[FRIDA 2022](https://frida-2022.github.io) was organized with FLoC 2022 and took place in Haifa.
[FRIDA 2023](https://frida-2023.github.io) took place in L'Aquila, Italy, along with DISC 2023.
