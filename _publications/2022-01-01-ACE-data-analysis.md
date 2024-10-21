---
title: "Towards an AI-based understanding of the solar wind: a critical data analysis of ACE data"
collection: publications
permalink: /publication/2022-01-01-ACE-data-analysis
excerpt: 'This paper is an analysis of a largely used dataset: Level-2 Advanced Composition Explorer’s SWEPAM and MAG measurements from 1998 to 2021 by the ACE Science Center. This work contains guidelines and highlights issues in the ACE data that are likely to be found in other space weather datasets: missing values, inconsistency in distributions, hidden information in statistics, etc.'
date: 2022-11-23
venue: 'Frontiers in Astronomy and Space Sciences'
paperurl: 'https://doi.org/10.3389/fspas.2022.980759'
citation: 'Bouriat, Simon, et al. "Towards an AI-based understanding of the solar wind: a critical data analysis of ACE data." Frontiers in Astronomy and Space Sciences: 311.'
---

All artificial intelligence models today require preprocessed and cleaned data to work properly. This crucial step depends on the quality of the data analysis being done. The Space Weather community increased its use of AI in the past few years, but a thorough data analysis addressing all the potential issues is not always performed beforehand. Here is an analysis of a largely used dataset: Level-2 Advanced Composition Explorer’s SWEPAM and MAG measurements from 1998 to 2021 by the ACE Science Center. This work contains guidelines and highlights issues in the ACE data that are likely to be found in other space weather datasets: missing values, inconsistency in distributions, hidden information in statistics, etc. Amongst all specificities of this data, the following can seriously impact the use of algorithms:
- Histograms are not uniform distributions at all, but sometime Gaussian or Laplacian. Algorithms will be inconsistent in the learning samples as some rare cases will be underrepresented. Gaussian distributions could be overly brought by Gaussian noise from measurements and the signal-to-noise ratio is difficult to estimate.
- Models will not be reproducible from year to year due to high changes in histograms over time. This high dependence on the solar cycle suggests that one should have at least 11 consecutive years of data to train the algorithm.
- Rounding of ion temperatures values to different orders of magnitude throughout the data, (probably due to a fixed number of bits on which measurements are coded) will bias the model by wrongly over-representing or under-representing some values.
- There is an extensive number of missing values (e.g., 41.59% for ion density) that cannot be implemented without pre-processing. Each possible pre-processing is different and subjective depending on one’s underlying objectives
- A linear model will not be able to accurately model the data. Our linear analysis (e.g., PCA), struggles to explain the data and their relationships. However, non-linear relationships between data seem to exist.
- Data seem cyclic: we witness the apparition of the solar cycle and the synodic rotation period of the Sun when looking at autocorrelations.

[Download paper here](https://www.frontiersin.org/articles/10.3389/fspas.2022.980759/pdf)
