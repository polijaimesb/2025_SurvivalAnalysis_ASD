# Evaluating the risk of metabolic syndrome after psychotropic medication in autism spectrum disorder: A survival analysis
This repository contains markdown scripts for cohort construction, medication event classification, and survival analysis to examine the association between psychotropic polypharmacy and metabolic syndrome-related conditions in individuals with Autism Spectrum Disorder (ASD).

## Prerequisites
The following R libraries must be installed.

```
library(dplyr)  
library(tidyr)  
library(stringr)  
library(RColorBrewer)  
library(data.table)  
library(ggplot2)  
library(AdhereR)  
library(lubridate)  
library(survival)  
library(survminer)  
library(tableone)  
library(stats)  
library(sjPlot)  
library(tidyverse)  
library(tidytable)  
library(lsr)  
library(car)  
```
## Authorization
Data used in this project is not available for public access.

## How to use it
The first markdown script (1.CohortIdentification) performs all steps required to clean and filter the study cohort of individuals with ASD who received psychotropic medications and were later diagnosed with a metabolic syndrome-related condition.

The second markdown script (2.PolypharmacyIdentification) processes prescription data to define and classify polypharmacy and monotherapy episodes based on overlapping medication events.

The third markdown script (3.SurvivalAnalysis) conducts a time-to-event analysis of metabolic syndrome onset following psychotropic exposure, using Cox proportional hazards models with sensitivity analyses.

## Analysis
The cohort is restricted to individuals with incident psychotropic use after 2012, with confirmed ASD diagnoses and continuous enrollment prior to first exposure. Exclusion criteria are applied to eliminate early diagnoses of metabolic syndrome and non-oral or invalid prescriptions.

Polypharmacy is defined using overlapping episodes (≥30 days) of multiple psychotropic medications. A custom pipeline identifies overlapping and merged events, and classifies them as either monotherapy or polypharmacy based on medication count and duration.

Survival models assess the association between psychotropic medication patterns and the risk of developing metabolic conditions such as weight gain or hypertension. Sensitivity analyses vary definitions of polypharmacy duration and follow-up windows. Forest plots and cumulative hazard plots are used to visualize results.

## Publication
This code supports a study intended for submission to a peer-reviewed journal.

