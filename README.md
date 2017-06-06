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

## Examples

### Univariate Gaussian mean

![\theta_{MAP} =  \overline{x} * \frac{n}{n + \sigma^2} + \mu * \frac{\sigma^2}{n + \sigma^2}](https://latex.codecogs.com/gif.latex?\inline&space;\theta_{MAP}&space;=&space;\overline{x}&space;*&space;\frac{n}{n&space;&plus;&space;\sigma^{2}}&space;&plus;&space;\mu&space;*&space;\frac{\sigma^{2}}{n&space;&plus;&space;\sigma^{2}})

in other words it is sample mean plus prior mean.

## Related Topics
- The Cramer-Rao Lower Bound
  - [Central Limit Theorem](https://en.wikipedia.org/wiki/Central_limit_theorem)
    sum independent random variables are tend toward a normal distribution
- [Likelihood Ratio Test](https://en.wikipedia.org/wiki/Likelihood-ratio_test) (compare zero hypothesis with ml value)
- [Wald Test](https://en.wikipedia.org/wiki/Wald_test)
- etc

## Videos

### Jeff Miller (mathematicalmonk)
- [(ML 6.1) Maximum a posteriori (MAP) estimation](https://www.youtube.com/watch?v=kkhdIriddSI)
- [(ML 6.2) MAP for univariate Gaussian mean](https://www.youtube.com/watch?v=KogqeZ_88-g)
- [(ML 6.3) Interpretation of MAP as convex combination](https://www.youtube.com/watch?v=SFQK57G5VF8)
