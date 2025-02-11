The OctCall.jl interface is unmaintained and doesn't work, since it depends on Cxx.jl. However you can [install and invoke the Octave binaries from within Julia](https://github.com/JuliaPackaging/Yggdrasil/issues/8397).

# OctCall: Calling GNU Octave from Julia

[![Build Status](https://travis-ci.org/JuliaInterop/OctCall.jl.svg?branch=master)](https://travis-ci.org/JuliaInterop/OctCall.jl)

This package allows you to call and interact with [GNU Octave](https://www.gnu.org/software/octave/), a mostly *Matlab-compatible* free-software numerical-computing language, from Julia.   It works by directly accessing the GNU Octave C++ libraries using [Cxx.jl](https://github.com/JuliaInterop/Cxx.jl), and hence should have performance comparable to calling Octave functions from within Octave.

Currently, communication of basic types such as numeric/boolean scalars, matrices/vectors, and strings are supported.  Support for more types will be added in the future.

Currently, OctCall is a pre-release preview.

## Installation

Before installing OctCall, make sure that GNU Octave is installed on your machine and that `mkoctfile` is in your `PATH`.

You should also add `ENV["JULIA_CXX_RTTI"]=1` to your `~/.julia/config/startup.jl` file.
