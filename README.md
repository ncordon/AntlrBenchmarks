# ANTLR Benchmarks

The repository is a fork of [https://github.com/KvanTTT/AntlrBenchmarks](https://github.com/KvanTTT/AntlrBenchmarks) to measure the perfomance loss of the antlr parsers in Javascript relative to Java ones, from antlr 4.8 to antlr 4.13.

## How to run

[Install Powershell](https://learn.microsoft.com/en-us/powershell/scripting/install/installing-powershell-on-macos?view=powershell-7.3) and run the script `./benchmark.ps1` in `Benchmark` directory

## Results
For [antlr 4.8](https://github.com/ncordon/AntlrBenchmarks/commit/45dce0f0f004c112178572ffe6ea78357f9224d6):

| Runtime                                 |  Mean [ns] |      Ratio |
| ---                                     |        --- |        --- |
| JavaStandard_NotLeftRecursion           |     171426 |       1.00 |
| JavaScriptStandard_NotLeftRecursion     |     678276 |       3.96 |
| JavaStandard_LeftRecursion              |     211838 |       1.24 |
| JavaScriptStandard_LeftRecursion        |     736566 |       4.30 |

For [antlr 4.13](https://github.com/ncordon/AntlrBenchmarks/commit/c8f4154bfe55ebf78a521310f851c982dfd8b56b):

| Runtime                                 |  Mean [ns] |      Ratio |
| ---                                     |        --- |        --- |
| JavaStandard_NotLeftRecursion           |     166219 |       1.00 |
| JavaScriptStandard_NotLeftRecursion     |   38756208 |     233.16 |
| JavaStandard_LeftRecursion              |     257626 |       1.55 |
| JavaScriptStandard_LeftRecursion        |   35087463 |     211.09 |
