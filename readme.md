## Repro for Paket framework: auto-detect problem

In this repository:
* PaketFrameworksProblemRepro - contains a solution that reproduces the problem
* ReproNugetPackage - contains a package project (this package is one of the conditions for the problem to surface)

### The problem

When doing `paket install` in the PaketFrameworksProblemRepro solution:
* If no paket.lock exists, works ok
* If there already is a paket.lock file, following error message is displayed

```
Paket failed with:
        Package Autofac  - framework: net452 was referenced, but it was not found in the paket.lock file in group Main.
```