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

gigascience-ref: REFXXX
...

# Introduction
The aim of this project was to begin to extend an existing Matlab-based package for implementing thousands of time-series analysis methods, [hctsa](https://github.com/benfulcher/hctsa), to a python-based implementation, for potential future inclusion into [Nitime](http://nipy.org/nitime/).

Nitime is python-based package for performing time-series analysis on neuroscience data. The highly comparative time-series analysis approach \cite{Fulcher2013} has an associated [website](www.comp-engine.org/timeseries) and Matlab-based code package, *hctsa*, that extracts thousands of structural features from a time series and determines which are most useful for a given scientific task.
<!-- We are currently applying the hctsa package to EEG and fMRI datasets to determine the most useful time-series features for predicting disease labels from these types of data. -->

In order to apply highly comparative time-series analysis in the neuroscience community, it would be desirable to implement some time-series analysis methods into the Nitime package, or at least using the Nitime data format. This would facilitate not only their use by the neuroscience community, but also their maintenance and development within an open source framework.

# Approach
An illustration of the approach is shown in Fig. \ref{centfig}. Each time series is converted to a vector of thousands of informative features using the *hctsa* package, and then machine learning methods are used to determine the most useful features.
In this project, we wanted to demonstrate a feasible pathway for incorporating these useful features into the Nitime package.

\begin{figure}[h!]
  \includegraphics[width=.47\textwidth]{nitime.png}
  \caption{\label{centfig} Illustration of the highly comparative approach to time-series data from neuroscience.}
\end{figure}


# Results
I successfully implemented a handful of basic time-series analysis functions from Matlab into python using partials, with basic support for the Nitime data format. This proof-of-principle is [here](https://github.com/benfulcher/hctsa_python).

# Conclusions
Our results demonstrate that time-series analysis methods, discovered using the [hctsa package](https://github.com/benfulcher/hctsa), can be implemented natively in python in a systematic way, with support for the time-series format used in Nitime.
This will allow future work on time-series analysis to be incorporated straightforwardly into an open source environment.
