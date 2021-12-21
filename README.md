# Mind the Gap: Studying the Insecurity of Provably Secure Embedded Trusted Execution Architectures

This repository is the hub for the code accompanying our [paper]():

> M. Bognar, J. Van Bulck, and F. Piessens, "Mind the Gap: Studying the Insecurity of Provably Secure Embedded Trusted Execution Architectures," in 2022 IEEE Symposium on Security and Privacy (S&P).

The open-source release contains code demonstrating our attacks on the target architectures,
Sancus_V [(pdf)](), VRASED [(pdf)](), and APEX [(pdf)](). We also created patches for some of the vulnerabilities,
which can be accessed on a separate branch.

For more information about the attacks, including a continuous integration framework executing them
on the systems, please check out the separate repositories for each system:

- [Sancus_V](https://github.com/martonbognar/sancus-core-gap)
- [VRASED](https://github.com/martonbognar/vrased-gap)
- [APEX](https://github.com/martonbognar/apex-gap)

## Abstract

The security claims of a system can be supported or refuted by different kinds
of evidence.
On the one hand, *attack research* uses empirical, experimental, inductive
methods to refute security claims. If motivated and competent
attackers do not succeed in breaking a specific security property, this
provides some support (but no definite proof) that the system is secure.

On the other hand, *formal methods* use mathematical, deductive methods
that can prove the security of a *model* of the system. The process of
constructing a proof can uncover vulnerabilities that can then be
fixed. The use of formal methods can be very powerful and is attractive
because it seems to provide irrefutable evidence of security. However, that
evidence applies only to the mathematical model, not to any actual system, and,
hence, it is important to understand the gap between the model and the
real-world system.

In this paper, we present a case study that examines this gap for two
embedded security architectures that use formal methods to prove their
security properties. Despite strong formal evidence for security, we discover
numerous attacks against the implementations, all of which falsify proven
security properties. These attacks range from exploiting simple programming
errors to a novel DMA-based side-channel attack.
The simple attacks demonstrate that the construction of systems and proofs is
error-prone, while some of the more sophisticated attacks serve as examples to
show that formal methods alone can never guarantee the security of a
real-world system.

From our case study, we also distill actionable guidelines on how to
provide stronger evidence for the security of a system.
