# Equivalence Checking of Quantum Circuits Based on Dirac Notation

This repository presents a support tool developed in Maude to check the equivalence of quantum circuits based on Dirac notation.

## Dependencies
- Maude is a programming/specification language based on rewriting logic. How to download and install Maude can be found [here](http://maude.cs.illinois.edu/w/index.php/The_Maude_System).

## How to install
- Clone the source code to your computer and go to the source code directory.

- Feed a Maude file that is the formal specification of quantum circuits being verified into Maude.

For example, we can type the following command in CLI in order to check the equivalence of quantum circuits for various case studies specified in the `case-studies.maude` file:

```console
maude case-studies.maude
```

- For testing, go to the `test` folder and run the `./tester` file in CLI.

## Case Studies
We successfully verify the equivalence of quantum circuits for some case studies:
- Control Reversal
- Distributed CNOT
- CNOT mirror
- Parallel to Λ CNOT
- Superdense coding as a state transfer
- ...

We verify not only the equivalence of quantum circuits for the case studies, but also successfully verify the non-equivalence of modified quantum circuits for the case studies, where we randomly remove a gate from their circuits or randomly change indices to which a gate can be applied.

We found a counterexample for the quivalence of quantum circuits used to represent Superdense coding as a state transfer, although they were reported as equivalent quantum circuits in literature.
Readers can see the counterexample at the end of case-studies.maude file for more details.

## Publication
- Canh Minh Do and Kazuhiro Ogata, "**Theoretical Foundation for Equivalence Checking of Quantum Circuits**", In The 2nd International Workshop on Formal Analysis and Verification of Post-Quantum Cryptographic Protocols, 2023. [[PDF]]()
- TBA