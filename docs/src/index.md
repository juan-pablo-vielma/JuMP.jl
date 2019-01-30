![JuMP logo](assets/jump-logo-with-text.svg)
===

[![Powered by NumFOCUS](https://img.shields.io/badge/powered%20by-NumFOCUS-orange.svg?style=flat&colorA=E1523D&colorB=007D8A)](http://numfocus.org)

```@meta
# These comments do not display in the HTML output.
# See https://github.com/JuliaDocs/Documenter.jl/issues/674.
```

!!! warning
    This documentation is for the development branch of JuMP. JuMP is undergoing
    a [major transition](https://discourse.julialang.org/t/mathoptinterface-and-upcoming-breaking-changes-in-jump-0-19)
    to MathOptInterface. The development version is beta quality and the
    documentation has TODOs remaining before the release. Please provide
    feedback and file issues if you use this branch.

    The [NEWS.md](https://github.com/JuliaOpt/JuMP.jl/blob/master/NEWS.md) file
    contains a comprehensive list of the changes between JuMP 0.18 and JuMP 0.19
    to aid users updating their existing models.

[JuMP](https://github.com/JuliaOpt/JuMP.jl) is a domain-specific modeling
language for [mathematical
optimization](http://en.wikipedia.org/wiki/Mathematical_optimization) embedded
in [Julia](http://julialang.org/). It currently supports a number of open-source
and commercial solvers (see below) for a variety of problem classes, including
**linear programming**, **mixed-integer programming**, **second-order conic
programming**, **semidefinite programming**, and **nonlinear programming**.
JuMP's features include:

-   User friendliness
    -   Syntax that mimics natural mathematical expressions.
    -   Complete documentation (WIP!)
-   Speed
    -   Benchmarking has shown that JuMP can create problems at similar speeds
        to special-purpose modeling languages such as
        [AMPL](http://www.ampl.com/).
    -   JuMP communicates with most solvers in memory, avoiding the need to
        write intermediary files.
-   Solver independence
    -   JuMP uses a generic solver-independent interface provided by the
        [MathOptInterface](https://github.com/JuliaOpt/MathOptInterface.jl)
        package, making it easy to change between a number of open-source and
        commercial optimization software packages ("solvers").
    -   Currently supported solvers include
        [Artelys Knitro](http://artelys.com/en/optimization-tools/knitro),
        [Bonmin](https://projects.coin-or.org/Bonmin),
        [Cbc](https://projects.coin-or.org/Cbc),
        [Clp](https://projects.coin-or.org/Clp),
        [Couenne](https://projects.coin-or.org/Couenne),
        [CPLEX](http://www-01.ibm.com/software/commerce/optimization/cplex-optimizer/),
        [ECOS](https://github.com/ifa-ethz/ecos),
        [FICO Xpress](http://www.fico.com/en/products/fico-xpress-optimization-suite),
        [GLPK](http://www.gnu.org/software/glpk/),
        [Gurobi](http://www.gurobi.com),
        [Ipopt](https://projects.coin-or.org/Ipopt),
        [MOSEK](http://www.mosek.com/),
        [NLopt](http://ab-initio.mit.edu/wiki/index.php/NLopt), and
        [SCS](https://github.com/cvxgrp/scs).
-   Access to advanced algorithmic techniques
    -   Including efficient LP re-solves which previously required using
        solver-specific and/or low-level C++ libraries.
-   Ease of embedding
    -   JuMP itself is written purely in Julia. Solvers are the only binary
        dependencies.
    -   Being embedded in a general-purpose programming language makes it easy
        to solve optimization problems as part of a larger workflow (e.g.,
        inside a simulation, behind a web server, or as a subproblem in a
        decomposition algorithm).
        -   As a trade-off, JuMP's syntax is constrained by the syntax available
            in Julia.
    -   JuMP is [MPL](https://www.mozilla.org/MPL/2.0/) licensed, meaning that
        it can be embedded in commercial software that complies with the terms
        of the license.

Although JuMP has not reached version 1.0 yet, the releases are
stable enough for everyday use and are being used in a number of research
projects and neat applications by a growing community of users who are early
adopters. JuMP remains under active development, and we welcome your feedback,
suggestions, and bug reports.

Contents
--------

```@contents
Pages = [
    "installation.md",
    "quickstart.md",
    "variables.md",
    "expressions.md",
    "objective.md",
    "constraints.md",
    "containers.md",
    "solvers.md",
    "solutions.md",
    "nlp.md",
    "style.md",
    "extensions.md"
]
Depth = 2
```

### Citing JuMP

If you find JuMP useful in your work, we kindly request that you cite the
following paper ([pdf](https://mlubin.github.io/pdf/jump-sirev.pdf)):

``` sourceCode
@article{DunningHuchetteLubin2017,
author = {Iain Dunning and Joey Huchette and Miles Lubin},
title = {JuMP: A Modeling Language for Mathematical Optimization},
journal = {SIAM Review},
volume = {59},
number = {2},
pages = {295-320},
year = {2017},
doi = {10.1137/15M1020575},
}
```

For an earlier work where we presented a prototype implementation of JuMP, see
[here](http://dx.doi.org/10.1287/ijoc.2014.0623):

``` sourceCode
@article{LubinDunningIJOC,
author = {Miles Lubin and Iain Dunning},
title = {Computing in Operations Research Using Julia},
journal = {INFORMS Journal on Computing},
volume = {27},
number = {2},
pages = {238-248},
year = {2015},
doi = {10.1287/ijoc.2014.0623},
}
```

A preprint of this paper is [freely available](http://arxiv.org/abs/1312.1431).

---

![NumFOCUS logo](assets/numfocus-logo.png)

JuMP is a fiscally sponsored project of [NumFOCUS](https://numfocus.org), a
nonprofit dedicated to supporting the open source scientific computing
community.

You can support JuMP by
[donating](https://www.flipcause.com/secure/cause_pdetails/MzkxMDU=). JuMP's
largest expense is the annual JuMP-dev workshop. Donations will help us provide
travel support for JuMP-dev attendees and take advantage of other opportunities
that arise to support JuMP development.
