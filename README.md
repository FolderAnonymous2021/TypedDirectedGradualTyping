# Coq Formalization Artifact
Type-Directed Operational Semantics for Gradual Typing

## Building Instructions

Our Coq proofs are verified in **Coq 8.10.2**. 
We rely on two Coq libraries: [`metalib`](https://github.com/plclub/metalib) for the locally nameless
representation in our proofs; and
[`LibTactics.v`](http://gallium.inria.fr/~fpottier/ssphs/LibTactics.html),
which is included in the directory.



### Prerequisites

1. Install Coq 8.10.2.
   The recommended way to install Coq is via `OPAM`. Refer to
   [here](https://coq.inria.fr/opam/www/using.html) for detailed steps. Or one could
   download the pre-built packages for Windows and MacOS via
   [here](https://github.com/coq/coq/releases/tag/V8.10.2). Choose a suitable installer
   according to your platform.

2. Make sure `Coq` is installed (type `coqc` in the terminal, if you see "command
   not found" this means you have not properly installed Coq), then install `Metalib`:
   1. Open terminal
   2. `git clone https://github.com/plclub/metalib`
   3. `cd metalib/Metalib`
   4. Make sure the version is correct by `git checkout 04b7aea`
   5. `make install`

3. Note to compile the `variant`, it is necessary to replace `LibLNgen.v` in `Metalib` by the file in the same name provided in the directory.
   1. `cd metalib/Metalib`
   2. copy the `LibLNgen.v` into it for replacement
   3. `make clean && make && make install`

### Build and Compile the Proofs

1. Enter  `calculus/coq` , `calculus_label/coq` `variant/coq` or `variant_label/coq` directory.

2. Type `make` in the terminal to build and compile the proofs.


## Proof Structure

