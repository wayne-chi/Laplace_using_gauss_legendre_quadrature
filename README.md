# Laplace_using_gauss_legendre_quadrature
This is a python code that numerically estimates the laplace function of any function using gauss legendre quadrature.
Mathematically converts the integral definition of laplace to a form similar to the gaussian quadrature.
then the weights and nodes are summed .


$$ L(f(t)) = \int_0^\infty e^{-st}f(t) dt$$

 let  $y = e^{-st} $

$$ e^{-st}dt = -sdy $$

$$ t = \frac{-ln(y)}{s} $$

$$ L(f(t)) = \frac{1}{s} \int_0^1 f({\frac{-lny}{s}}) dy$$

 let  $b = 2y-1 $ 

  $y = \frac{b+1}{2} $ 

$$ dy = \frac{db}{2} $$

$$ F(s) =  \frac{1}{2s} \int_{-1}^1 f({\frac{-ln\frac{b+1}{2}}{s}}) db$$

  let  $g(b,s) = f({\frac{-ln\frac{b+1}{2}}{s}}) $   
  This is known as the transformation function.

$$ F(s) =  \frac{1}{2s} \int_{-1}^1 g(b,s)db $$

 apply gauss legendre quadrature 

$$ F(s) = \frac{1}{2s} \sum_{i=1}^n w_ig(x_i,s) $$
