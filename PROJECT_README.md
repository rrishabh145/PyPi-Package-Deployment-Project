# PyPi-Package-Deployment-Project

A python project to create python package which calculates Gaussian and Binomial distributions. This is the first project on how to create package and upload on PyPi (implementation of that is given below under the heading **How to create and upload a package to PyPi**).

Link to the PyPi package link: [pypi.org/project/statistical-distribution/1.0/](https://pypi.org/project/statistical-distribution/1.0/)

## Getting Started

To use the statistical_distribution package, pip install the package directly (Check Installing section inside the statistical_distribution directory).

In order to work with the source code: Download or clone the repository in the local system, install the prerequisites and run testing code.

### Prerequisites

Twine is needed for uploading the code to PyPi if one wants to try doing it.

```
$ pip install twine
```

For those using conda, install using conda command.

```
$ conda install twine
```

### Installing

Create and run a new virtual environment to avoid interfering with the base python library's installation on your system. Using conda, this can be done easily:

```
$ conda create -n yourenvname
$ conda activate yourenvname
```

To install the impllemented library from PyPi, pip install the package.

```
$ pip install statistical-distribution
```

To build the library from source code, go to the project directory path, which contains the setup.py file, in terminal and run the following commands.

```
$ pip install .
```

This installs the statistical-distribution package on your system in your virtual environment.
To quick check if the installation is working properly, run the following commands in a python interpreter.

```
>>> from distributions import Gaussian
>>> gaussian_one = Gaussian(25, 2)
>>> gaussian_one.mean
```

You should get the following output without any errors if the package is installed correctly.

```
>>> 25
```

## Running the tests

To check if the code of Binomial distribution and Gaussian distribution is running correctly and giving correct results, run the following test commands which runs the test.py file :

```
$ python -m unittest test
```

test.py file passes multiple values in the objects created from Binomial and Gaussian classes and checks if the numerical values returned are correct according to the mathematical formulae.

If the test ran successfully without error, you should see an 'OK' as output

If changes to the base code are made, make sure to reinstall the package locally before running the unit test again. To bring the code changes to effect, run the following code:

```
$ pip install --upgrade .
```
Note that if you change the code in the project folder after pip installing the package, Python will not know about the changes. You'll need to run above mentioned command everytime you make changes to the package files.

**----------------------------------------------------------------------------------------------------**

# How to create and upload Package to PyPi

This section explains how you can create and upload your own package on PyPi so that anyone can pip install the package.

### Prerequisites

Twine  is needed for uploading the code to PyPi if one wants to try doing it.

```
$ pip install twine
```

For those using conda, install using conda command.

```
$ conda install twine
```

## Setting up and Installion

In the directory where a setup.py file is created, run the following command:

```
$ python setup.py sdist bdist_wheel
```

This will output a folder called 'dist' having a _tar.gz_ file and a _.whl_ file. The _tar.gz_ file is called a source archive whereas the _.whl_ file is a built distribution.

We can even use just ```python setup.py sdist``` which will get only _tar.gz_ file in 'dist' folder.
When we pip install a package, pip will first look for a whl file (wheel file) and if there isn't one, will then look for the tar.gz file.

A _tar.gz file_, i.e. an sdist, contains the files needed to compile and install a Python package. A _whl_ file, i.e. a built distribution, only needs to be copied to the proper place for installation. Behind the scenes, pip installing a _whl_ file has fewer steps than a _tar.gz_ file.

## Deployment of package on PyPi repository

To upload your package to PyPi, you first need to create an account on their site. After that, run the following commands and enter your username and password to upload the package successfully.

```
$ twine upload dist/*
$ pip install numerical_distributions
```

Remember to use a unique name for your package as it cannot be similar to any other package on PyPi site.

### Test the deployment

Check the **Installing** section of *PyPi-Package-Deployment-Project*.

## License

This project is licensed under the MIT License - see the [license.txt](statistical_distribution/license.txt) file for details

## Acknowledgments

* [AWS Machine Learning Foundation Course - Udacity](https://www.udacity.com/course/aws-machine-learning-foundations--ud090)