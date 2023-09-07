# hpc-build-box

This container provides an environment with key libraries and tools for high-performance computing (HPC) development. It includes MPI (Message Passing Interface), OpenMP (Open Multi-Processing), Eigen (C++ template library for linear algebra), and CMake build system.

## Features

- **MPI**: Pre-installed Open MPI for parallel computing.
- **OpenMP**: Support for multi-platform shared-memory parallel programming.
- **Eigen**: Eigen 3.4 for high-level linear algebra operations.
- **CMake**: Version 3.25.0 for configuring and building your projects.

## Pre-requisites

- [Singularity](https://sylabs.io/guides/3.7/user-guide/quick_start.html) installed on your machine.

## Download 

To pull the latest version of the container:

```
singularity pull https://github.com/bjorgve/hpc-build-box/releases/download/0.0.2/bjorgve-hpc-build-box.build.sif
```

## Usage

### Running CMake

```
./bjorgve-hpc-build-box.build.sif cmake [options]
```

### Compiling Code with Make

```
./bjorgve-hpc-build-box.build.sif make [options]
```

### Running Executables

```
./bjorgve-hpc-build-box.build.sif ./executable [options]
```

## Inside the Container

Here's what gets installed in the container based on the `.def` file:

- Basic build utilities (`build-essential`, `wget`, `git`, `curl`, etc.)
- OpenMP (`libgomp1`)
- Open MPI (`libopenmpi-dev`, `openmpi-bin`)
- Boost libraries (`libboost-all-dev`)
- CMake 3.25.0
- Eigen 3.4

## Contributions and Issues

Feel free to open issues or submit pull requests if you have suggestions or encounter issues.
