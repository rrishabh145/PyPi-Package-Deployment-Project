# Statistical-Distribution-package

A python package to calculate Gaussian and Binomial distributions. First project on how to create package and upload on PyPi.

## Getting Started

To use the package, pip install the package directly (Check Installing section).

In order to work with the source code: Download or clone the repository in the local system and install the prerequisites.(Check the Project Readme file)

### Prerequisites

Default python libraries.

### Installing

_Optional_: Create and run a new virtual environment. Using conda, this can be done easily:

```
$ conda create -n yourenvname
$ conda activate yourenvname
```

Install the package by running the following command in terminal:

```
$ pip install statistical-distribution
```

To check if the installation is working properly, run the following commands in a python interpreter.

```
>>> from distributions import Gaussian
>>> gaussian_one = Gaussian(25, 2)
>>> gaussian_one.mean
```

You should get the following output without any errors if the package is installed correctly.

```
>>> 25
```

## License

This project is licensed under the MIT License - see the [license.txt](license.txt) file for details

## Acknowledgments

* [AWS Machine Learning Foundation Course - Udacity](https://www.udacity.com/course/aws-machine-learning-foundations--ud090)