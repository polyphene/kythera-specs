# Introduction

## Abstract

When dealing with the development of smart contracts (or **actors** per Filecoin lexicon), developers have to go through
multiple stages before safely deploying their code. Typically an actor developer would evolve through 3 different environments:

- Development environment: Most likely located on a local machine, the development environment provides a sandbox where 
the developer can safely experiment and unit test the different features that are supposed to be delivered.
- Staging environment: In dApp development the staging environment is usually referring to a *testnet* where the conditions
of the network are emulated to behave the same as the *mainnet*.
- Production environment: Commonly referred to as the *mainnet*, this is where the developed actor will be deployed to be
available to any client.

The goals of the **FVM Native Toolset** are to ease the **development stage** for the developer by bringing an FVM-compatible
execution environment and libraries for testing utilities, and facilitate the transition to the staging and production environments.

## Motivation

With the release of milestone 2.1 of the FVM, it will be possible for Ethereum smart contract developers to try out the capabilities
of the FEVM. The choice to first release the FEVM, cashing on the Ethereum ecosystem and its maturity, might allow for smooth adoption.

However, the FEVM has one limitations, it limits a developer in only imagining applications limited to the EVM context 
while WASM-based actors open-up new possibilities.

But for these possibilities to exist, the ecosystem of native actors is in need of tooling on par with the Ethereum 
ecosystem. We think that a toolset is the first key component for developers as it allows for experimentation over use 
cases and a consolidation of code bases reliability. Developing such a solution would also prove useful in organizing 
hackathons, and allowing developers to directly dive in their actors’ implementation.

As such a component is a strategic resource for the Filecoin ecosystem, we believe that a team like Polyphene could be 
the right one to handle its specification and development.

