# Estimating Multiple Structural Breaks in Large Panels With Unobserved Heterogeneity

---

## Paper Description

This paper proposes a novel algorithm to identify potentially multiple breaks in
linear panel data models, while the slope coefficients can have individual heterogeneity and the cross-sectional dimension is allowed to diverge jointly with the time span.
The algorithm adopts a shrinkage penalty to detect breaks, and delivers a consistent estimator for the number of breaks and fraction-consistent estimators for break
dates. In the presence of latent grouped heterogeneity, we employ the classifier-Lasso
method to further derive super-consistent break-date estimators based on the break
identification result given by the shrinkage algorithm. We demonstrate the satisfactory performance of the proposed methodology in finite samples with Monte Carlo
simulations. Empirically, we illustrate the use of our methods to study structural
breaks and unobserved heterogeneity in cross-sectional risk premiums.

---

## Repository Overview

This repository provides the code, data access instructions, and scripts used in:

> "Estimating Multiple Structural Breaks in Large Panels With Unobserved Heterogeneity"  
> Wenxin Huang (Shanghai Jiao Tong University), Yucheng Sun (Capital University of Economics and Business), Yiru Wang (University of Pittsburgh)  

It supports full replication of all empirical and simulation results reported in the paper.  
The repository includes MATLAB scripts, processed datasets, and supporting functions for the analyses performed.

---

## Folder Structure and Descriptions

The repository consists of three main folders:

| Folder | Description |
|--------|-------------|
| `functions/` | Contains all MATLAB function files used to implement the methodology described in the paper. |
| `simulation/` | Contains scripts that generate the simulation experiments reported in the paper. This folder includes subfolders for heterogeneous panels and grouped panels, corresponding to Tables 1–4 in the manuscript. |
| `real-data-code/` | Contains the empirical application code to reproduce the figures and real-data results presented in the paper. It also includes the datasets `sample10_all.mat` and `SP500.mat`. |

---

## Requirements

The code was developed and tested using the following environment:

| Software | Version | Notes |
|----------|---------|-------|
| MATLAB | R2023a | Required |

All scripts have been tested on macOS and Windows operating systems.

---

## Overview of Scripts and Figure Generation

Below is a list of figures from the paper, mapped to the folders that produce them.  
Each folder contains a local README or instruction file describing detailed workflows.  
Please run the scripts in order to fully reproduce the results.

| Output | Folder | Main Script(s) | Notes / Approx. Running Time |
|---------|---------|----------------|------------------------------|
| Fig. 1, 2 | `real-data-code` | `MAIN_EST_PLOTS.m` | Approximately 16 minutes on an Intel(R) Core(TM) i7-10700 CPU @ 2.90 GHz with 32 GB RAM |

---

## Data Dictionary

Two MATLAB `.mat` data files are used for the empirical analysis.  
They can be found in the folder `real-data-code/`.

### 1. `sample10_all.mat`
This file contains the following variables: firm-level returns, market beta, size, book-to-market ratio, and momentum. 

| Column | Variable | Description |
|---------|-----------|-------------|
| 1 | Firm ID | CRSP firm identifier (PERMNO) |
| 2 | Generated Firm Number | Internal numeric identifier for processing |
| 3 | Date | Monthly date (in Stata format) |
| 4 | Return | Monthly firm-level return |
| 5 | Market Beta | Estimated from market model |
| 6 | Size | Market capitalization |
| 7 | Book-to-Market Ratio |
| 8 | Momentum | 


### 2. `SP500.mat`
This dataset contains monthly S&P 500 index values.

| Column | Variable |  Description |
|---------|-----------|-------------|
| 1 | Date | Monthly date | 
| 2 | S&P 500 Index | 

