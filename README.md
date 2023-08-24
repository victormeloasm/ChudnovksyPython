# Pi Computation Using Chudnovsky Algorithm

This repository contains a Python implementation of the Chudnovsky algorithm to calculate the value of π (pi) to a specified number of digits. The Chudnovsky algorithm is a fast and efficient method for calculating π using a binary splitting technique and is particularly useful for high-precision computations.

## Chudnovsky Algorithm

The Chudnovsky algorithm is a series-based formula for calculating the value of π. It was discovered by the Chudnovsky brothers, David and Gregory, in 1989. The algorithm relies on a binary splitting approach to recursively calculate the terms of the series. This method allows for rapid convergence and high precision in the computed value of π.

The formula for the Chudnovsky algorithm is given by:

<p align="center">
  <img src="https://latex.codecogs.com/png.latex?\dpi{150}&space;\large&space;\frac{1}{\pi}&space;=&space;\frac{12&space;k!&space;(6k)!(545140134k&plus;13591409)}{(3k)!&space;((k!)^3&space;(\sqrt{640320})^{3k})}" title="Chudnovsky Formula" />
</p>

In this formula:
- k is the index of the term.
- Factorials are calculated using the Gamma function for non-integer values.
- The square root of 640320 is raised to the power of 3k, and the other constants are used as coefficients.

## Implementation Details

The Python code in this repository implements the Chudnovsky algorithm using the `gmpy2` library for arbitrary-precision arithmetic. The code computes π to a specified number of digits by iteratively calculating the terms of the series and performing the required arithmetic operations.

The core steps of the implementation include:
1. Initializing the constants and required precision.
2. Using binary splitting to calculate the terms of the series recursively.
3. Performing arithmetic operations using `gmpy2` for high precision.
4. Formatting the result with the initial "3." prefix for the decimal representation of π.

## How to Use

1. Make sure you have Python 3.6 or later installed.
2. Install the `gmpy2` library by running: `pip install gmpy2`.
3. Clone this repository: `git clone https://github.com/yourusername/chudnovsky-pi.git`.
4. Navigate to the repository folder: `cd chudnovsky-pi`.
5. Run the script with the desired number of digits: `python pi_computation.py 1000` (Replace `1000` with the number of digits you want).

The calculated value of π will be stored in the `pi.txt` file.

## Conclusion

The Chudnovsky algorithm is an elegant and efficient way to compute the value of π to a high degree of precision. This repository provides a Python implementation of the algorithm, showcasing how binary splitting and arbitrary-precision arithmetic can be used to achieve accurate results. Feel free to explore the code and adapt it to your needs.
