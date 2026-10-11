# Lab Report — Lab 01: Efficient Separable Gaussian Convolution

## Overview

The goal was to make Gaussian convolution faster by using separable 1D filters instead of a single 2D filter.

## Implementation

I created a normalized 1D Gaussian kernel and applied it horizontally and vertically using `sliding_window_view` and `tensordot`. I also handled image padding to preserve the output dimensions.

## Results

The separable method reduced the number of calculations compared to the full 2D convolution baseline, making it more efficient. The implementation produced the expected output in the pytests.
