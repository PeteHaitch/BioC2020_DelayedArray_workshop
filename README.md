
<!-- README.md is generated from README.Rmd. Please edit that file -->

# Effectively using the DelayedArray framework to support the analysis of large datasets

<!-- badges: start -->

[![R build
status](https://github.com/PeteHaitch/BioC2020_DelayedArray_workshop/workflows/.github/workflows/basic_checks.yaml/badge.svg)](https://github.com/PeteHaitch/BioC2020_DelayedArray_workshop/actions)
<!-- badges: end -->

## Key resources

  - Docker image: [Docker
    Hub](https://hub.docker.com/repository/docker/petehaitch/bioc2020_delayedarray_workshop)
  - Workshop: [pkgdown
    website](https://petehaitch.github.io/BioC2020_DelayedArray_workshop)

## Workshop description

This workshop gives an introductory overview of the DelayedArray
framework, which can be used by R / Bioconductor packages to support the
analysis of large array-like datasets. A *DelayedArray* is like an
ordinary array in R, but allows for the data to be in-memory, on-disk in
a file, or even hosted on a remote server.

Workshop participants will learn where they might encounter a
*DelayedArray* in the wild while using Bioconductor and understand the
fundamental concepts underlying the DelayedArray framework. This
workshop will feature introductory material, ‘live’ coding, and Q\&A,
all of which are adapted from the content below.

### Instructor

  - [Peter Hickey](https://peterhickey.org/) (<hickey@wehi.edu.au>)

### Pre-requisites

  - Basic knowledge of R syntax.
  - Familiarity with common operations on matrices in R, such as
    `colSums()` and `colMeans()`.
  - Some familiarity with S4 objects may be helpful but is not required.

### Workshop Participation

Students will be able to run code examples from the workshop material.
There will be a Q\&A session in the second half of the workshop.

### *R* / *Bioconductor* packages used

These packages are the focus of this workshop:

  - *[DelayedArray](https://bioconductor.org/packages/3.12/DelayedArray)*
  - *[HDF5Array](https://bioconductor.org/packages/3.12/HDF5Array)*
  - *[DelayedMatrixStats](https://bioconductor.org/packages/3.12/DelayedMatrixStats)*

Please see the workshop
[`DESCRIPTION`](https://github.com/PeteHaitch/BioC2020_DelayedArray_workshop/blob/master/DESCRIPTION)
for a full list of dependencies.

### Time outline

| Activity                                       | Time   |
| ---------------------------------------------- | ------ |
| Introductory material                          | 5 min  |
| First contact                                  | 25 min |
| Workflow tips for DelayedArray-backed analyses | 10 min |
| Q\&A                                           | 15 min |

### Workshop goals and objectives

#### Learning goals

  - Learn of existing packages and functions that *use* the DelayedArray
    framework.
  - Develop a high-level understanding of classes and packages that
    *implement* the DelayedArray framework.
  - Become familiar with the fundamental concepts of *delayed
    operations*, *block processing*, and *realization*.
  - Reason about potential bottlenecks, and how to avoid or reduce
    these, in algorithms operating on *DelayedArray* objects.

#### Learning objectives

  - Identify when an object is a *DelayedArray* or one of its
    derivatives.
  - Be able to recognise when it is useful to use a *DelayedArray*
    instead of an ordinary array or other array-like data structure.
  - Learn how to load and save a DelayedArray-backed object.
  - Learn how the ‘block size’ and ‘chunking’ of the dataset affect
    performance when operating on *DelayedArray* objects.
  - Take away some miscellaneous tips and tricks I’ve learnt over the
    years when working with DelayedArray-backed objects.

## Docker set up

  - Run `docker run -e PASSWORD=delayedarray -p 8787:8787 -d --rm
    petehaitch/bioc2020_delayedarray_workshop`. Use `-v
    $(pwd):/home/rstudio` argument to map your local directory to the
    container.
  - Log in to RStudio at <http://localhost:8787> using username
    `rstudio` and password `yourpassword`. Note that on Windows you need
    to provide your localhost IP address like
    `http://191.163.92.108:8787/` - find it using `docker-machine ip
    default` in Docker’s terminal.
  - Run `browseVignettes(package = "DelayedArrayWorkshop")`. Click on
    one of the links, “HTML”, “source”, “R code”.
      - In case of `The requested page was not found` error, add `help/`
        to the URL right after the hostname, e.g.,
        <http://localhost:8787/help/library/DelayedArrayWorkshop/doc/Effectively_using_the_DelayedArray_framework_for_users.html>.
        This is a [known
        bug](https://github.com/rocker-org/rocker-versioned/issues/178).
