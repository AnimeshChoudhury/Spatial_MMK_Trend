# Spatial Modified Mann-Kendall Trend

In order to determine whether or not there is a increasing or decreasing trend in a set of time series data, statisticians use the Mann-Kendall Trend Test (often abbreviated as MK test). 

The null hypothesis for this test is that there is no monotonic trend in the series.

The alternate hypothesis is that a trend exists. 

This trend can be positive, negative, or non-null.The idea is that if a trend is present, the sign values will tend to increase constantly, or decrease constantly. Every value is compared to every value preceding it in the time series, which gives a total of n(n ā 1) / 2 pairs of data, where ānā is the number of observations in the set.

The data does not need to be normally distributed since this is a non-parametric test, but there should be no serial correlation in the data. Serial correlation in the data may have a major impact on the significance level (p-value). It might cause confusion. Multiple variants of the Mann-Kendall test were developed to address this issue (Hamed and Rao Modified MK Test, Yue and Wang Modified MK Test, Modified MK test using Pre-Whitening method, etc.). In order to account for seasonality, the Seasonal Mann-Kendall test was devised.

Since the Mann-Kendall Test is so effective at detecting trends, it has inspired a number of variants tailored to the spatial context, such as the Multivariate MK Test, the Regional MK Test, the Correlated MK Test, the Partial MK Test, etc. [pyMannkendal](https://pypi.org/project/pymannkendall/) is a Python library for doing non-parametric Mann-Kendall trend analysis, which unifies the vast majority of Mann-Kendall Test variants. This package currently contains 11 Mann-Kendall tests and 2 sen's slope estimator functions. In this study, Land Surface Temperature (LST) trend for Kolkata has been checked with the help of [MODIS LST](https://developers.google.com/earth-engine/datasets/catalog/MODIS_061_MOD11A1). The [Hamed and Rao Modified MK Test](https://www.sciencedirect.com/science/article/abs/pii/S002216949700125X?via%3Dihub) for each pixel has been performed at p=0.05. The Theil-Sen's Slope of the trend is then spatially plotted to visualize the intensity of the trend. 
