About mlconjug
==============

Home: https://github.com/SekouD/mlconjug

Package license: MIT

Feedstock license: BSD 3-Clause

[![pypi](https://img.shields.io/pypi/v/mlconjug.svg)](https://pypi.python.org/pypi/mlconjug)    [![travis](https://img.shields.io/travis/SekouD/mlconjug.svg)](https://travis-ci.org/SekouD/mlconjug)   [![appveyor](https://ci.appveyor.com/api/projects/status/6iatj101xxfehbo8/branch/master?svg=true)](https://ci.appveyor.com/project/SekouD/mlconjug) [![readthedocs](https://readthedocs.org/projects/mlconjug/badge/?version=latest)](https://mlconjug.readthedocs.io/en/latest/?badge=latest)  [![pyup](https://pyup.io/repos/github/SekouD/mlconjug/shield.svg)](https://pyup.io/repos/github/SekouD/mlconjug/)   [![codecov](https://codecov.io/gh/SekouD/mlconjug/branch/master/graph/badge.svg)](https://codecov.io/gh/SekouD/mlconjug)    [![snyk](https://snyk.io/test/github/SekouD/mlconjug/badge.svg?targetFile=requirements.txt)](https://snyk.io/test/github/SekouD/mlconjug?targetFile=requirements.txt)

Summary: A Python library to conjugate French, English, Spanish, Italian, Portuguese and Romanian verbs using Machine Learning techniques.


Any verb in one of the supported language can be conjugated, as the module contains a Machine Learning model of how the verbs behave.

Even completely new or made-up verbs can be successfully conjugated in this manner.

The supplied pre-trained models are composed of:

- a binary feature extractor,
- a feature selector using Linear Support Vector Classification,
- a classifier using Stochastic Gradient Descent.

MLConjug uses scikit-learn to implement the Machine Learning algorithms.

Users of the library can use any compatible classifiers from scikit-learn to modify and retrain the models.

The training data for the french model is based on Verbiste https://perso.b2b2c.ca/~sarrazip/dev/verbiste.html .

The training data for English, Spanish, Italian, Portuguese and Romanian was generated using unsupervised learning techniques
  using the French model as a model to query during the training.


* Free software: MIT license
* Documentation: https://mlconjug.readthedocs.io.

Supported Languages
-------------------

- French
- English
- Spanish
- Italian
- Portuguese
- Romanian


Features
--------

- Easy to use API.
- Includes pre-trained models with 99% + accuracy in predicting conjugation class of unknown verbs.
- Easily train new models or add new languages.
- Easily integrate MLConjug in your own projects.
- Can be used as a command line tool.

Credits
---------

This package was created with the help of [Verbiste](https://perso.b2b2c
.ca/~sarrazip/dev/verbiste.html) and [scikit-learn](http://scikit-learn.org/stable/index.html).

The logo was designed by [Zuur](https://github.com/zuuritaly).



Current build status
====================

All platforms:
[![noarch](https://img.shields.io/circleci/project/github/conda-forge/mlconjug-feedstock/master.svg?label=noarch)](https://circleci.com/gh/conda-forge/mlconjug-feedstock)

Current release info
====================

| Name | Downloads | Version | Platforms |
| --- | --- | --- | --- |
| [![Conda Recipe](https://img.shields.io/badge/recipe-mlconjug-green.svg)](https://anaconda.org/conda-forge/mlconjug) | [![Conda Downloads](https://img.shields.io/conda/dn/conda-forge/mlconjug.svg)](https://anaconda.org/conda-forge/mlconjug) | [![Conda Version](https://img.shields.io/conda/vn/conda-forge/mlconjug.svg)](https://anaconda.org/conda-forge/mlconjug) | [![Conda Platforms](https://img.shields.io/conda/pn/conda-forge/mlconjug.svg)](https://anaconda.org/conda-forge/mlconjug) |

Installing mlconjug
===================

Installing `mlconjug` from the `conda-forge` channel can be achieved by adding `conda-forge` to your channels with:

```
conda config --add channels conda-forge
```

Once the `conda-forge` channel has been enabled, `mlconjug` can be installed with:

```
conda install mlconjug
```

It is possible to list all of the versions of `mlconjug` available on your platform with:

```
conda search mlconjug --channel conda-forge
```


About conda-forge
=================

conda-forge is a community-led conda channel of installable packages.
In order to provide high-quality builds, the process has been automated into the
conda-forge GitHub organization. The conda-forge organization contains one repository
for each of the installable packages. Such a repository is known as a *feedstock*.

A feedstock is made up of a conda recipe (the instructions on what and how to build
the package) and the necessary configurations for automatic building using freely
available continuous integration services. Thanks to the awesome service provided by
[CircleCI](https://circleci.com/), [AppVeyor](http://www.appveyor.com/)
and [TravisCI](https://travis-ci.org/) it is possible to build and upload installable
packages to the [conda-forge](https://anaconda.org/conda-forge)
[Anaconda-Cloud](http://docs.anaconda.org/) channel for Linux, Windows and OSX respectively.

To manage the continuous integration and simplify feedstock maintenance
[conda-smithy](http://github.com/conda-forge/conda-smithy) has been developed.
Using the ``conda-forge.yml`` within this repository, it is possible to re-render all of
this feedstock's supporting files (e.g. the CI configuration files) with ``conda smithy rerender``.

For more information please check the [conda-forge documentation](https://conda-forge.org/docs/).

Terminology
===========

**feedstock** - the conda recipe (raw material), supporting scripts and CI configuration.

**conda-smithy** - the tool which helps orchestrate the feedstock.
                   Its primary use is in the construction of the CI ``.yml`` files
                   and simplify the management of *many* feedstocks.

**conda-forge** - the place where the feedstock and smithy live and work to
                  produce the finished article (built conda distributions)


Updating mlconjug-feedstock
===========================

If you would like to improve the mlconjug recipe or build a new
package version, please fork this repository and submit a PR. Upon submission,
your changes will be run on the appropriate platforms to give the reviewer an
opportunity to confirm that the changes result in a successful build. Once
merged, the recipe will be re-built and uploaded automatically to the
`conda-forge` channel, whereupon the built conda packages will be available for
everybody to install and use from the `conda-forge` channel.
Note that all branches in the conda-forge/mlconjug-feedstock are
immediately built and any created packages are uploaded, so PRs should be based
on branches in forks and branches in the main repository should only be used to
build distinct package versions.

In order to produce a uniquely identifiable distribution:
 * If the version of a package **is not** being increased, please add or increase
   the [``build/number``](http://conda.pydata.org/docs/building/meta-yaml.html#build-number-and-string).
 * If the version of a package **is** being increased, please remember to return
   the [``build/number``](http://conda.pydata.org/docs/building/meta-yaml.html#build-number-and-string)
   back to 0.