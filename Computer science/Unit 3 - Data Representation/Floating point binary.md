
Floating point representation of a binary number can be used to represent extremely large and extremely small numbers in binary, using a similar system to standard form in denary. While standard form is expressed as:
$$\Huge mantissa\times10^{exponent}$$
Floating point binary is expressed as:
$$\Huge mantissa\times2^{exponent}$$
The point in a floating point number is always after the first digit.

# Rounding errors:

To fully represent a number in binary, the whole part must be expressed as a sum of powers of 2,  and the fractional part must be broken down into a sum of negative powers of 2. To represent numbers that cannot be broken down in this way, truncation and rounding are used.

Truncation is when any bits after a fixed amount are discarded, rounding is when a number is rounded to the nearest number that can be fully broken down. Both methods result in a loss of accuracy. This loss can be represented as an absolute or relative error.

# Range and precision:

The mantissa of a floating point number holds its value, while the exponent is an expression of its magnitude. This can be a positive or negative value to represent large or small numbers respectively. Increasing bits allocated for the mantissa allows for a more detailed value to be stored, resulting in more precision. Increasing bits allocated for the exponent allows for larger and smaller values for the magnitude, increasing the range of numbers that can be represented.

Normalisaiton of floating point form maximises the avaiblible precision for fractional numbers given the amount of bits allocated.

# Normalisation:

Similar to how the mantissa of a standard form number must be between 1 and 10, the mantissa of a floating point number must be in the simplest form possible so that maximum precision is availible for the number of bits allocated for the mantissa.

To do this, logical shifts are performed on the mantissa, and the exponent is increased or decreased based on the number of shifts in either direction. The normalised form of a positive fractional number has no leading zeroes after the binary point, $0.1$. The normalised form of a negative fractional number has no leading ones after the binary point, $1.0$.

If a number is positive, it is normalised by moving the binary point until it is in front of the first bit in the mantissa, whose value is 1. If a number is negative, it is normalised by moving the binary point until it is in front of the first bit in the mantissa, whose value is 0. In both cases, the exponent must be adjusted by incrementing it for every LSR and decrementing it for every LSL, to account for dividing and multiplying the number by 2.

# Over/Under flow:

Overflow occurs when the result of a calculation is too large to be represented using the amount of availible bits. The results of a calculation cause leading 1s to turn to 0s, causing the appearance of an unresonably small number.

Underflow occurs when the result of a calculation is too small to be represented using the amount of availible bits. There are not enough bits in the mantissa or exponent to hold the detail and magnitude of a number. This happens when the result of a calculation is close to zero.