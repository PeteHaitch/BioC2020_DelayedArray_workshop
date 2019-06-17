
<!-- README.md is generated from README.Rmd. Please edit that file -->

# Effectively using the DelayedArray framework as a user to support the analysis of large datasets

[![Travis-CI Build
Status](https://travis-ci.org/PeteHaitch/BioC2019_DelayedArray_workshop.svg?branch=master)](https://travis-ci.org/PeteHaitch/BioC2019_DelayedArray_workshop)

## Workshop description

This workshop gives an introductory overview of the DelayedArray
framework, which can be used by Bioconductor packages to support the
analysis of large datasets. A *DelayedArray* is like an ordinary array
in R, but allows for the data to be in-memory (including space-efficient
formats like sparse arrays and run length encoded arrays), on-disk in a
file, or even hosted on a remote server. Participants will learn where
they might encounter a *DelayedArray* in the wild while using
Bioconductor and help them understand the fundamental concepts
underlying the framework. This workshop will be a mixture of lecture
with example code and discussion. Examples will mostly be drawn from the
analysis of single-cell RNA-sequencing data.

### Instructor

  - Peter Hickey (<hickey@wehi.edu.au>)

### Pre-requisites

  - Basic knowledge of R syntax.
  - Familiarity with common operations on matrices in R, such as
    `colSums()` and `colMeans()`.
  - Some familiarity with S4 objects may be helpful but is not required.
  - Some familiarity with single-cell RNA-sequencing may be helpful but
    is not required.

### Workshop Participation

Students will be able to run code interactively during the workshop.
There will be opportunities throughout the workshop for questions and
discussion.

### *R* / *Bioconductor* packages used

  - *[DelayedArray](https://bioconductor.org/packages/3.9/DelayedArray)*
  - *[HDF5Array](https://bioconductor.org/packages/3.9/HDF5Array)*
  - *[DelayedMatrixStats](https://bioconductor.org/packages/3.9/DelayedMatrixStats)*
  - *[TENxBrainData](https://bioconductor.org/packages/3.9/TENxBrainData)*
  - *[TENxPBMCData](https://bioconductor.org/packages/3.9/TENxPBMCData)*
  - *[BiocSingular](https://bioconductor.org/packages/3.9/BiocSingular)*
  - *[scater](https://bioconductor.org/packages/3.9/scater)*
  - *[scran](https://bioconductor.org/packages/3.9/scran)*

### Time outline

| Activity                                       | Time |
| ---------------------------------------------- | ---- |
| Introductory material                          | 10m  |
| First contact                                  | 40m  |
| Package ecosystem                              | 10m  |
| Real world encounters analysing scRNA-seq data | 25m  |
| Workflow tips for DelayedArray-backed analyses | 15m  |

### Workshop goals and objectives

#### Learning goals

  - Learn of existing packages and functions that *use* the DelayedArray
    framework.
  - Develop a high-level understanding of classes and packages that
    *implement* the DelayedArray framework.
  - Become familiar with the fundamental concepts of delayed operations,
    block-processing, and realization.
  - Reason about potential bottlenecks in algorithms operating on
    *DelayedArray* objects.

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
