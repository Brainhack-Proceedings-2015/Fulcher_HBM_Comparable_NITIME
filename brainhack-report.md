---
event: '2015 OHBM Hackathon (HI)'

title:  'Inclusion of a Highly Comparable Time Series Analysis in NiTime'

author:

- initials: BF
  surname: Fulcher
  firstname: B
  email: bfulcher@monash.edu.au
  affiliation: aff1
  corref: aff1

affiliations: 

- id: aff1
  orgname: 'School of Psychological Sciences, Monash University'
  street: 1 Queen Quay
  postcode: 055332
  city: Melbourne
  state: 
  country: Australia


url: http://github.com/nitime

coi: None

acknow: The authors would like to thank the organizers and attendees of the 2015 OHBM Hackathon.

contrib: BF wrote the software and the report.
  
bibliography: brainhack-report

gigascience-ref: REFXXX
...

#Introduction
To prepare a framework for implementing important time-series analysis features in python, for inclusion into NiTime \cite{Fulcher2013}, from an existing HCTSA package for highly comparative time-series analysis (Matlab-based). 

NiTime is python code for performing time-series analysis on neuroscience data. HCTSA is Matlab code for extracting thousands of structural features from a time series. We are currently applying the HCTSA code in Matlab to EEG and fMRI datasets to determine the most useful time-series features for these types of data. 

In order to achieve a simple applicability of HCTSA throughout the neuroscience community, it would be desirable to implement these sets of time-series analysis methods into the NiTime package or at least using the NiTime data format. This facilitates not only their application by the neuroscience community, but also their maintenance and development within an open source framework. Currently, there is no native python implementation of HCTSA. Therefore, HCTSA was not yet included into the NiTime package. 


#Approach
This is where the approach goes.

\begin{figure}[h!]
  \includegraphics[width=.47\textwidth]{nitime.png}
  \caption{\label{centfig} Illustration of NiTime method.}
\end{figure}


#Results
I successfully implemented a handful of basic time-series analysis functions from Matlab into python using partials, with basic support for the NiTime data format. A basic, proof-of-principle result is available [here](https://github.com/benfulcher/hctsa_python). This framework now allows time-series analysis methods, discovered using the HCTSA Matlab package, to be implemented in python in a systematic way (with support for the time-series format used in NiTime). This will allow future work on time series analysis to be incorporated straightforwardly into an open source environment.

# Conclusions
This is were the conclusion goes.