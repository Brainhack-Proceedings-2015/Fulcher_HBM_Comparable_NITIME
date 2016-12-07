---
event: '2015 OHBM Hackathon (HI)'

title:  'Highly Comparable Time-Series Analysis in Nitime'

author:

- initials: BDF
  surname: Fulcher
  firstname: Ben D.
  email: ben.fulcher@monash.edu
  affiliation: aff1
  corref: aff1

affiliations:

- id: aff1
  orgname: 'Monash Institute of Cognitive and Clinical Neurosciences, Monash University'
  street: 770 Blackburn Rd
  postcode: 3168
  city: Melbourne
  state:
  country: Australia


url: https://github.com/benfulcher/hctsa_python

coi: None

acknow: The authors would like to thank the organizers and attendees of the 2015 OHBM Hackathon.

contrib: BF wrote the software and the report.

bibliography: brainhack-report

gigascience-ref: \href{http://gigadb.org/dataset/100225}{doi:10.5524/100225}
...

# Introduction
The aim of this project was to demonstrate that an existing Matlab-based package for implementing thousands of time-series analysis methods, [hctsa](https://github.com/benfulcher/hctsa) (\url{https://github.com/benfulcher/hctsa}), could be extended to a python-based implementation, for potential future inclusion into [Nitime](http://nipy.org/nitime/) (\url{http://nipy.org/nitime/}).

Recent work has contributed a comprehensive library of over 35,000 pieces of diverse time-series data, and over 7,000 unique structural features extracted from hundreds of different time-series analysis methods \cite{Fulcher2013}, which can be explored through an associated [website](www.comp-engine.org/timeseries) (\url{www.comp-engine.org/timeseries}) and implemented using the Matlab-based code package, [hctsa](https://github.com/benfulcher/hctsa).
The *hctsa* software provides a systematic, algorithmic platform for computing a wide range of structural properties from a single time series, including basic statistics of the distribution, linear correlation structure, stationarity, information theoretic and entropy measures, methods from the physical nonlinear time-series analysis literature, linear and nonlinear model fits, and others.
Thus, hctsa can be used to map a time series to a comprehensive vector of interpretable structural features and these features can then be systematically compared to determine and understand the most useful features for a given scientific objective (e.g., features of an EEG signal that help classify different patient groups).

<!-- We are currently applying the hctsa package to EEG and fMRI datasets to determine the most useful time-series features for predicting disease labels from these types of data. -->

In order to apply highly comparative time-series analysis in the neuroscience community, it would be desirable to implement some time-series analysis methods into [Nitime](http://nipy.org/nitime/), a python-based software package for performing time-series analysis on neuroscience data.
<!-- While the Nitime data format supports unevenly sampled data, *hctsa* does not; although for evenly sampled data it is trivial to extract the data vector from the Nitime Timeseries class and run important time-series algorithms on these data vectors. -->
Implementation of useful time-series features into python, and potential integration with Nitime, would not only facilitate their use by the neuroscience community, but also their maintenance and development within an open source framework.

# Approach
An illustration of the approach is shown in Fig. \ref{centfig}.
Each time series is converted to a vector of thousands of informative features using the *hctsa* package; machine learning methods can then be used to determine the most useful features (e.g., that best discriminate patient groups, and where in the brain the best discrimination occurs).
In this project, we wanted to demonstrate a feasible pathway for incorporating these useful features into the Nitime package.

\begin{figure}[h!]
  \includegraphics[width=.47\textwidth]{nitime.png}
  \caption{\label{centfig} Illustration of the highly comparative approach to time-series data from neuroscience.}
\end{figure}


# Results
I successfully implemented a handful of basic time-series analysis functions from Matlab into python using partials (a python function that freezes a given set of input arguments to a more general function).
The proof-of-principle implementation has full support for vectors of data stored in numpy arrays, and basic support for the Nitime data format (extracting the data vector from the Nitime TimeSeries class for evenly sampled data).
The code is [here](https://github.com/benfulcher/hctsa_python).

# Conclusions
Our results demonstrate that time-series analysis methods, discovered using the [hctsa package](https://github.com/benfulcher/hctsa), can be implemented natively in python in a systematic way, with basic support for the time-series format used in Nitime.
This will help facilitate future work on time-series analysis to be incorporated straightforwardly into this open source environment.
Although there are no plans to reimplement the full *hctsa* feature library in python, our hope is that published work describing useful time-series features (discovered using the *hctsa* library) can also contribute a python implementation, to promote its use by the neuroscience community.
