# [**10.** API Reference](@id API-Reference)

This section describes the function interface, or "API mode"
for interacting with Pkg.jl. The function API is recommended
for non-interactive usage, in i.e. scripts.

## [**10.1.** Package API Reference](@id Package-API-Reference)

In the REPL mode packages (with associated version, UUID, URL etc) are parsed from strings,
for example, `"Package#master"`,`"Package@v0.1"`, `"www.mypkg.com/MyPkg#my/feature"`.
It is possible to use strings as arguments for simple commands in the API mode (like `Pkg.add(["PackageA", "PackageB"])`,
more complicated commands, that e.g. specify URLs or version range, uses a more structured format over strings.
This is done by creating an instance of a [`PackageSpec`](@ref) which are passed in to functions.

```@docs
PackageSpec
PackageMode
UpgradeLevel
Pkg.add
Pkg.develop
Pkg.activate
Pkg.rm
Pkg.update
Pkg.test
Pkg.build
Pkg.pin
Pkg.free
Pkg.instantiate
Pkg.resolve
Pkg.setprotocol!
```


## [**10.2.** Registry API Reference](@id Registry-API-Reference)

The function API for registries uses [`RegistrySpec`](@ref)s, similar to
[`PackageSpec`](@ref).

```@docs
RegistrySpec
Pkg.Registry.add
Pkg.Registry.rm
Pkg.Registry.update
Pkg.Registry.status
```
