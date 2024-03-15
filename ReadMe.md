# Equivalence Checking of Quantum Circuits Based on Dirac Notation

This repository presents a tool called |QCEC> for <u>Q</u>uantum <u>C</u>ircuit <u>E</u>quivalence <u>C</u>hecking based on Dirac notation in Maude.

## Dependencies
- Maude is a programming/specification language based on rewriting logic. How to download and install Maude can be found [here](http://maude.cs.illinois.edu/w/index.php/The_Maude_System).
- An algebraic specification for quantum computation ([|AS4QC>](https://github.com/canhminhdo/ket-as4qc)) as a submodule in this repository.

## How to install
- Clone the source code to your computer and go to the source code directory.
```console
git clone --recurse-submodules https://github.com/canhminhdo/ket-qcec.git && cd ket-qcec
```

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

We found that some quantum circuits used to represent Superdense coding as a state transfer are non-equivalent unless constant inputs are considered.
Readers can see them at the end of case-studies.maude file for more details.

## Publication
- Canh Minh Do and Kazuhiro Ogata, "**Theoretical Foundation for Equivalence Checking of Quantum Circuits**", In The 2nd International Workshop on Formal Analysis and Verification of Post-Quantum Cryptographic Protocols, 2023. [[PDF]](https://github.com/canhminhdo/EquivCheck/blob/main/publications/Theoretical-Foundation-for-Equivalence-Checking-of-Quantum-Circuits.pdf)
- TBA