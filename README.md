<!-- badges: start -->
  [![R-CMD-check](https://github.com/Quanlin222/api/actions/workflows/R-CMD-check.yaml/badge.svg)](https://github.com/Quanlin222/api/actions/workflows/R-CMD-check.yaml)
<!-- badges: end -->

# api package

The `api` package provides functionality to connect to the Kolada API, allowing users to access statistical data related to Swedish municipalities. This package includes functions to download data directly from the API in JSON format, process the data, and perform basic filtering and transformations. This document will introduce how to use the package and demonstrate its capabilities.

## 1.1 Installing and Loading the Package

First, ensure you have the package installed and loaded:

devtools::install_github("Quanlin222/api")

library(api)


## 1.2 Example: Fetching Data from the API

The getdata_api function allows users to retrieve data for a specified year. The year must be between 2000 and 2023 (inclusive).

year <- 2021  # Specify the year

data <- getdata_api(year)  # Fetch data

## 1.3 Error Handling

The getdata_api function handles errors gracefully. If there are issues such as invalid years, HTTP errors, or empty responses, it will return NULL and print a warning message


