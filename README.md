# MLE and MAP
Machine Learning: Maximum Likelihood Estimation (MLE) and Maximum a Posteri (MAP) Estimation

## Subtleties

ML doesn't work good with sparse data because `P(X | Y)` might be zero.
(for example, Xi = birthdate, Xi = Jan_25_1992)

```
P(Y=1 | X1...Xn) = (P(Y=1) * Mult P(Xi | Y=1) for i) / P (X1...Xn)
```

We can solve it by using prior with MAP estimation.

# MLE

## Pros

- invariant under reparameterization. So we can wrap
![\theta_{MLE}](http://www.sciweavers.org/tex2img.php?eq=%20%5Ctheta_%7BMLE%7D&bc=Transparent&fc=Black&im=jpg&fs=12&ff=arev&edit=0)
in any function.


# MAP

## Pros

- avoid overfitting (regularization / shrinkage)
- tends to look like MLE asymptotically

## Cons

- point estimation (no representation of uncertainty in θ).
Because it could choose spike of θ because it has higher probability
- not invariant under reparameterization
- must assume prior on θ

## Related Topics
- The Cramer-Rao Lower Bound
  - [Central Limit Theorem](https://en.wikipedia.org/wiki/Central_limit_theorem)
    sum independent random variables are tend toward a normal distribution
- [Likelihood Ratio Test](https://en.wikipedia.org/wiki/Likelihood-ratio_test) (compare zero hypothesis with ml value)
- [Wald Test](https://en.wikipedia.org/wiki/Wald_test)
- etc
