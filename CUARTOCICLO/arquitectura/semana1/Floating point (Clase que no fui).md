The ppt is in the folder. Because there is no possibility to put this on obsidian. 
There is a format for floating point. That is the IEEE format.
The floating point format is made by partitioning in parts the exponent and fraction.

| S   | Exponent | Fraction |
| --- | -------- | -------- |
The exponent could be:
-> single: 8 bits
-> double: 11 bits
The fraction could be:
-> single: 23 bits
-> double: 52 bits
The formula to represent the floating point is the next.
$$
x = (-1)^{s} \times (1 + \text{Fraction}) \times 2^{(\text{Exponent - Bias})}
$$
$S:$ This is going to tell you is it's negative or nor. 0 is not negative.
The normalized significant is literally  -> 1 + fracción. Indeed that's why $1.0 \leq |\text{significand| < 2.0}$. Because de fraction cannot be 1.
**Exponent**: Excess representation: actual exponent + Bias.
WE rest the Bias. The reason why we don't put just the exponent is because the exponent should be in a range of $[-127:127]$. So, For the hardware it is difficult to deal with negatives. Instead we'll have a stored exponent and just going to rest the Bias. In this way we just have to deal with positive numbers.
The precision would change depending on:
-> Single Bias = 127;
-> Double Bias = 1203
### The “hidden 1”

Because that leading `1` is _always_ there, IEEE 754 doesn’t bother storing it — it’s assumed.

- So instead of storing 24 bits (1 + 23 fraction bits), we only store 23, and the hardware automatically adds the leading 1.
    

That’s what people mean when they say: _“there are 23 stored bits, but effectively 24 bits of precision._
Now let's see:
## Single precision Range
Why the exponents 00000000 y 11111111 reserved? No idea.
**Smallest value**:
 For the exponent would be -126. The fraction could be 0, then the significant 1.0.
 For the largest value.
 **Largest value:**
 for the exponent: 11111110 => = 127.
 On the fraction would be 2.0 aproximately. 
 The double is analogously.
 ___
 The single fraction could carry 6 decimal digits of precision, and double 16. The demonstration is on the ppt.
 REMEMBER THE WAY TO REPRESENT IS 1.1 IS GOING TO BE 1.5. Remember that , is th half. 
## Denormal Numbers
Denormals “turn off” the hidden 1 rule.
- Exponent bits = all zero.
- Mantissa is interpreted as:
This allowed us to fill the gap between 0 and th esmallest numbers. But losing presicion.