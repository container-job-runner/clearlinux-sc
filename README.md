# clearlinux-sc
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://github.com/gitbucket/gitbucket/blob/master/LICENSE)

A prebuilt cjr stack for scientific computing that is based on Clear linux.

This stack provides basic support for the following packages:

1. **Languages**
   - Python 3
   - c, c++
   - Fortran
   - Julia
   - R
   - Latex
2. **Libraries**
   - Matplotlib
   - BLAS, LAPACK
   - Open MPI
   - X11
3. **Dev Environments**
   - Jupyter notebook, Jupyter lab
   - Theia
   - vim, git, vim, emacs, tmux

The configurations for Jupyter and Theia are respectively stored the directories `config/jupyter` and `config/theia` which are bound to `~/.jupyter` and `~/.theia` in the container.
The stack comes preconfigured with Theia extensions for python, c/c++ and Fortran.

On start, the image entrypoint dynamically modifies the default container user so that id and group id match with the host.

## Installation

To use use this stack with cjr simply run the command
```console
cjr stack:pull https://github.com/container-job-runner/clearlinux-sc.git
```
You can then build the stack by running
```console
cjr stack:build clearlinux-sc
```
To run an interactive shell with this stack run
```console
cjr shell --stack=clearlinux-sc
```