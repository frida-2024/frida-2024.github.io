---

layout: home
---


# The 11th Workshop on Formal Reasoning in Distributed Algorithms

Date: Tuesday July 23rd, 2024

Location: Montreal, Canada

The workshop is part of [CAV 2024](https://i-cav.org/2024/) and is organized by [Swen Jacobs](https://cispa.de/en/people/swen.jacobs) ([CISPA Helmholtz Center for Information Security](https://cispa.de/)) and [Giuliano Losa](https://www.losa.fr/) ([Stellar Development Foundation](https://research.stellar.org)).

## Tentative Schedule

(Click the arrows to display the abstracts)

* 09:05 ---
 Opening
* 09:10 to 09:50 ---
 [Siddhartha Jayanti](https://sites.google.com/view/siddhartha-jayanti/research), Google Research and AI
    <details>
    <summary>Machine-Verifying Complex and Deployed Multiprocess Data Structures (<a href="./Machine-Verifying_Complex_and_Deployed_Multiprocess_Data_Structures.pdf">slides</a>)</summary>
    <br>
    <p>
    I will talk about machine-verifying the correctness of concurrent data structures via the universal and complete Meta-Configurations Tracking verification method for proving linearizability. We have used this method to prove algorithms with famously complex and future-dependent linearization structures and those which have been impactfully deployed in practice. We demonstrate the simplicity and power of our method by producing proofs of linearizability for the Herlihy-Wing queue and Jayanti’s single-scanner snapshot, as well as a proof of strong linearizability of the Jayanti-Tarjan union-find object, which is deployed in Google's open-source graph mining library to enable the clustering billion-scale data. All three of these proofs are machine-verified by TLAPS (the TLA+ Proof System).
    </p>
    <p>
    Bio: Siddhartha Jayanti is a Research Scientist at Google Research, Cambridge, MA. He is an algorithmist, whose work spans distributed systems, machine learning, economics and computing, security, and verification. Siddhartha earned his Ph.D. in Computer Science with a minor in Machine Learning from MIT, where he was advised by Julian Shun. He received his Master's from MIT under the guidance of Costis Daskalakis, and his Bachelor's from Princeton, where his thesis was advised by Robert Tarjan and his research on mathematics in Sanskrit was advised by Manjul Bhargava.
    </p>
    </details>
* 09:50 to 10:30 ---
 [Nisarg Patel](https://cs.nyu.edu/~nrp364/), NYU
    <details>
    <summary>Verification of Lock-free Search Structure Templates (<a href="./Verification_of_Lock-free_Search_Structure_Templates.pdf">slides</a>)</summary>
    <br>
    <p>
    Concurrent search structures are a class of concurrent data structures that implement a key-value store. Concurrent search structures are integral components of modern software systems, yet they are notoriously difficult to design and implement. In the context of concurrency, linearizability is the accepted notion of correctness of a data structure. Verifying linearizability of concurrent search structures remains a formidable challenge due to the inherent complexity of the underlying algorithms. So far, verification of these data structures has often led to large, intricate proofs that are hard to comprehend and reuse. In this talk, we focus on lock-free concurrent search structures based on lists and skiplists. For this class of data structures, we present verification techniques that aid modularity and enable proof reuse. The resulting linearizability proofs are fully mechanized in the concurrent separation logic Iris. The proofs are modular and cover the broader design space of the underlying algorithms by parameterizing the verification over aspects such as the low-level representation of nodes and the style of data structure maintenance. As a further technical contribution, we present a mechanization of a recently proposed method for reasoning about future-dependent linearization points using hindsight arguments. The mechanization builds on Iris’ support for prophecy reasoning and user-defined ghost resources. We demonstrate that the method can help to reduce the proof effort compared to direct prophecy-based proofs.
    </p>
    </details>

* 10:30 to 11:00 ---
 coffee break

* 11:00 to 11:40 ---
 [Marco Eilers](https://www.pm.inf.ethz.ch/people/personal/meilers-pers.html), ETHZ
    <details>
    <summary>verifiedSCION: Verified Secure Routing</summary>
    <br>
    <p>
    SCION is a new Internet architecture that addresses many of the security vulnerabilities of today’s Internet. Its clean-slate design provides, among other properties, route control, failure isolation, and multi-path communication. The verifiedSCION project is an effort to formally verify the correctness and security of SCION. It aims to provide strong guarantees for the entire architecture, from the protocol design to its concrete implementation.
    The key step to achieving these guarantees is to formally connect a model of the entire SCION network, about which we can prove global properties, to correctness proofs of individual router implementations.
    This talk will give an overview of the verifiedSCION project and explain, in particular, how we extract specifications for individual components from a global model of a distributed system using refinement and decomposition, and how we then verify each component against its specification using deductive program verification in separation logic.
    </p>
    </details>
* 11:40 to 12:20 ---
 [Borzoo Bonakdarpour](http://www.cse.msu.edu/~borzoo/), Michigan State University
    <details>
    <summary>Fault-tolerant Distributed Runtime Monitoring (<a href="./Fault-tolerant_Distributed_Runtime_Monitoring.pdf">slides</a>)</summary>
      <br>
      <p>
      Monitoring distributed applications that do not share a global clock is highly challenging as the monitor has to potentially deal with a combinatorial enumeration at run time. We also have every reason to believe that distributed monitors are not necessarily perfect and monitors are subject to all types of faults that normal distributed processes are. In this talk, I will present our results on runtime verification of distributed systems. We make a practical assumption that the distributed system under scrutiny is augmented with a clock synchronization algorithm that guarantees bounded clock skew among all processes. Second, we do not make any assumption about the structure of the formal specification under inspection. We introduce a set of distributed monitoring algorithms by employing SMT-solving that range over discrete distributed systems such as databases to cyber-physical systems such as network of autonomous vehicles. I will also present real-world case studies and demonstrate that scalable online monitoring of distributed applications is within our reach.
      </p>
    </details>

* 12:20 to 14:10 ---
 Lunch break (lunch is not included)

* 14:10 to 14:50 ---
 [Eric Koskinen](https://www.erickoskinen.com/#/), Stevens Institute of Technology
    <details>
    <summary>Scenario-Based Proofs for Concurrent Objects</summary>
    <br>
    <p>
    Concurrent objects form the foundation of many applications that exploit multicore architectures and their importance has lead to informal correctness arguments, as well as formal proof systems. Correctness arguments (as found in the distributed computing literature) give intuitive descriptions of a few canonical executions or “scenarios” often each with only a few threads, yet it remains unknown as to whether these intuitive arguments have a formal grounding and extend to arbitrary interleavings over unboundedly many threads.
    </p>
    <p>
    We present a novel proof technique for concurrent objects, based around identifying a small set of scenarios (representative, canonical interleavings), formalized as the commutativity quotient of a concurrent object. We next give an expression language for defining abstractions of the quotient in the form of regular or context-free languages that enable simple proofs of linearizability. These quotient expressions organize unbounded interleavings into a form more amenable to reasoning and make explicit the relationship between implementation-level contention/interference and ADT-level transitions.
    </p>
    <p>
    We evaluate our work on numerous non-trivial concurrent objects from the literature (including the Michael-Scott queue, Elimination stack, SLS reservation queue, RDCSS and Herlihy-Wing queue). We show that quotients capture the diverse features/complexities of these algorithms, can be used even when linearization points are not straight-forward, correspond to original authors’ correctness arguments, and provide some new scenario-based arguments. Finally, we show that discovery of some object’s quotients reduces to two-thread reasoning and give an implementation that can derive candidate quotients expressions from source code.
    </p>
    <p>
    Joint work with Constantin Enea. To appear in OOPSLA 2024.
    </p>
    </details>

* 14:50 to 15:30 ---
 [Isaac Sheff](https://isaacsheff.com/), Heliax
    <details>
    <summary>Formal Methods at Heliax: an industry experience report (<a href="./Formal_Methods_at_Heliax:_an_industry_experience_report.pdf">slides</a>)</summary>
    <br>
    <p>
    History is littered with examples where distributed applications suffer because the underlying infrastructure is running flawed protocols or implementations. Heliax is a public goods lab building software for running distributed systems infrastructure to increase flexibility and security of applications. This talk reviews our experiences at Heliax, in particular how we integrate formal methods into our infrastructure software design process. The talk focuses on implementation plans for Heterogeneous Paxos, a consensus algorithm with complex trust assumptions, wherein different parties make different assumptions about who can fail and how. It also explains  our motivations for using formal methods, reports on our experiences with tools (including TLA⁺, TLAPS and Isabelle/HOL), and includes a “wish-list” of features that, in our experience, would maximize the impact of a formal verification tool.
    </p>
    </details>

* 15:30 to 16:00 ---
 Coffee break

* 16:00 to 16:40 ---
 [Nicholas V. Lewchenko](https://www.octalsrc.org/research), University of Colorado Boulder
    <details>
    <summary>Bolt-On Strong Consistency: Specification, Implementation, and Verification</summary>
    <br>
    <p>
    Strongly-consistent replicated data stores are a popular foundation for many kinds of online services, but their implementations are very complex. Strong replication is not ‘available’ under network partitions, and so achieving a functional degree of fault-tolerance requires correctly implementing ‘consensus algorithms’ like Raft and Paxos. These algorithms are notoriously difficult to reason about, and many data stores implement custom variations to support unique performance tradeoffs, presenting an opportunity for automated verification tools. Unfortunately, existing tools that have been applied to distributed consensus demand too much developer effort, a problem stemming from the low-level programming model in which consensus and strong replication are implemented—asynchronous message passing—which thwarts decidable automation by exposing the details of communication and the structure of the distributed network.
    </p>
    <p>
In this talk, I will explore an alternative approach: the implementation and verification of strong replication systems *as applications of* weak replicated data stores. Weak stores, being available under partition, are a suitable foundation for performant distributed applications. At the same time, they abstract asynchronous communication and allow us to derive local-scope conditions for the verification of consensus safety. To evaluate this approach, we have developed a verified-programming framework for the weak replicated state model, called ‘Super-V’. This framework enables SMT-based verification based on local-scope artifacts called ‘strong update preconditions’, improving on standard-practice global inductive invariants in both decidability by the solver and ease of discovery by the developer. I will demonstrate how this framework can be used to implement and verify a strong replication system based on an adaptation of the Raft consensus algorithm, and discuss the performance implications of this approach.
    </p>
    </details>
* 16:40 to 17:20 ---
 [Stephen Siegel](https://vsl.cis.udel.edu/siegel.html), University of Delaware
    <details>
    <summary>Challenge Problems in Verification of MPI Programs (<a href="./Challenge_Problems_in_Verification_of_MPI_Programs.pdf">slides</a>)</summary>
    <br>
    <p>
    MPI (Message Passing Interface) is the standard interface for writing distributed-memory parallel programs for scientific and high performance computing.   While MPI is a large library, the core functions, which suffice for expressing most algorithms, provide a simple interface with well-behaved properties, e.g., messages are never dropped and message order is preserved.  One of the main challenges in scientific computing is the mechanistic verification of programs written in C, C++, or Fortran and using MPI.   There has been some success in verifying such programs within small bounds on the number of processes, using model checking and symbolic execution techniques.  There has also been work on parameterized verification of these programs.  In this talk I will summarize MPI and show some examples of what has been accomplished so far, as well as examples for which current verification technology is insufficient.  Can ideas from distributed system verification help us solve these problems?
    </p>
    </details>
* 17:20 to 18:00 ---
 [Kostis Sagonas](https://www.ece.ntua.gr/en/staff/77), Uppsala University, Sweden and NTUA, Greece
    <details>
    <summary>Testing and Verifying Concurrency Algorithms using Stateless Model Checking</summary>
    <br>
    <p>
    Stateless Model Checking (SMC) is a fully automatic verification
    technique for concurrent programs that checks for safety violations by
    exploring all possible ways that threads can interleave.  It becomes
    effective when combined with Dynamic Partial Order Reduction algorithms
    and various bounding techniques.
    </p>
    <p>
    This talk will present experiences in applying two different SMC tools
    in two different case studies. The first of them applied Nidhugg, an SMC
    tool for C/Pthread programs, to the code of Tree RCU, the Hierarchical
    Read-Copy-Update synchronization mechanism for mutual exclusion used in
    the Linux kernel, a low-level and quite complex concurrent program. The
    second case study applied Concuerror, an SMC tool for Erlang programs,
    to test and verify, during their design phase by engineers at VMWare,
    chain repair methods for CORFU, a distributed shared log which aims to
    be scalable and reliable in the presence of failures and asynchrony.
    </p>
    </details>
<!-- * [Giuliano Losa](https://www.losa.fr), Stellar Development Foundation
    <details>
    <summary>From Federated Byzantine Agreement to 3-valued logic</summary>
    </details> -->

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
