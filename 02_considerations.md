# Considerations

## Multiplicity of source languages

The native actors being deployed on the Filecoin chain and executed in the FVM are in a WASM binary format. This compact 
binary format can be compiled to from a diversity of languages like Rust, Assembly Script, Go... This diversity of source
languages is actually an asset for native actors as it allows for developers from different background to still try to work
on applications leveraging the Filecoin network and the FVM. **Kythera should leverage this asset and allow for any developer 
of a native actors to have a testing framework for their project.**

This statement has a few impacts in how Kythera should be conceived:
- No specifications or implementation choices should restrict the possibility of Kythera to work along a native actors
project that can compile to a WASM binary format
- Using Kythera along such projects should be possible without necessitating evolution of the testing framework

From those constraints we can derive a few implementation notes:
- Kythera should not be a project with a given file structure containing native projects. Instead **Kythera should be a tool
to use on top of native projects**, with no impact on the file structure of the project
- **To work Kythera will only require a given location where WASM binaries are stored**, instead of building the project files 
when needed.

## Maintainability and updatability

To ensure that the testing capabilities of Kythera are aligned with the behaviour of the Filecoin network we will need
to have a local execution environment conform to [FVM specifications](https://github.com/filecoin-project/FIPs/blob/master/FIPS/fip-0030.md).
The easiest way to do so is to leverage the [`ref-fvm`](https://github.com/filecoin-project/ref-fvm/) implementation as 
this repository will most likely always be updated based on specification evolution.

**Kythera should the aim to use or extends as much as possible from this implementation** instead of re-implementing it, to 
ease its maintenance.
