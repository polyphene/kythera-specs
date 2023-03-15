# Inspirations

## Testing frameworks

When looking at solutions over different ecosystems for toolsets, there are a few candidates that the FVM Native Toolset
should get inspiration from. In the following section we go over some potential inspirations and their strengths.

### Ethereum - Hardhat


The [Hardhat](https://github.com/NomicFoundation/hardhat) project from the Ethereum ecosystem is a great example of a 
simple toolset, focusing on providing users with **a complete, yet simple, testing environment**.

There are two main components for the project, *Hardhat Runner* and *Hardhat Network.*

*Hardhat Runner* is the main component that users interact with and contains most of the logic related to smart contracts
development, like compilation, testing and deployment. *Hardhat Network* on the other hand provides a local Ethereum network
node designed for development.

Tests development and management is done through JavaScript or Typescript. Hardhat provides its own set of 
[Chai matchers](https://hardhat.org/hardhat-chai-matchers/docs/overview) to help design test cycles that are as DRY 
(Don’t Repeat Yourself) and self-documented as possible.

One of the key strength of *Hardhat* comes from its *plugin* system. The *Hardhat Runner* comes with a set of built-in *
tasks* (`compile` , `run` , `test` …). *Plugins* can be created by users to compose with built-in *tasks* or even overwrite
them. Another interesting feature is the existing integration with the template system, *Open Zeppelin.* By installing the
npm package handed out by the *Open Zeppelin* team, it is possible for developer to easily refer to a template contracts
in their solidity code (e.g.: `import "@openzeppelin/contracts/token/ERC20/ERC20.sol"` ).

### Ethereum - Foundry

[Foundry](https://github.com/foundry-rs/foundry) is another toolset from the Ethereum ecosystem. It is more recent than 
Hardhat and tries to fill the caveats of its senior. Where Hardhat focuses on simplicity, Foundry proposes a more complex
but richer solution for testing.

When installing Foundry, three components are made available: *forge*, *cast* and *anvil.*

*Forge* is the testing framework, like *Hardhat Runner*. It handles the compilation and testing for smart contracts 
development. Advanced features goes from fuzzy testing to generating gas reports for a contract. *Cast* is the command-line
interface (CLI) for performing Ethereum RPC calls to make smart contract calls, send transactions, or retrieve any type 
of chain data. *Anvil* is the local Ethereum network node, like *Hardhat Network*.

Tests are written in Solidity, testing utilities are available through smart contracts that can be imported in the test 
contracts.

The strength of *Foundry* is **its compilation speed**, attained through a solid caching system and parallel compilation.
Along with the compilation speed, *Foundry* allows for fast test development thanks to their Solidity-based approach.

### Solana - Anchor

[Anchor](https://www.anchor-lang.com/)’s toolset has emerged for the Solana ecosystem. Its goal is to provide convenient 
developer tools for writing smart contracts compatible with the Solana chain.

Anchor could be a great inspiration with their technical architecture and implementation. They leverage Rust and macros 
to facilitate development of programs.

The toolset testing is handled through JavaScript or Typescript.

## FVM testing environment

For the implementation of Kythera we should also get inspiration from @anorth [FVM Workbench](https://github.com/anorth/fvm-workbench/)
and the [integration test framework](https://github.com/filecoin-project/ref-fvm/tree/master/testing/integration) from the ref-fvm repository.