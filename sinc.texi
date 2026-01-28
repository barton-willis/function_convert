@ifnotinfo
@settitle Function sinc
@top Function sinc
@end ifnotinfo

@c  --- sinc ------------------------------------------------------------------

@defun sinc (x)
Return @code{sin(x)/x}.  The function @code{sinc(x)} is defined for all
real and complex values of @var{x}.  At @var{x} = 0 the value is defined
to be 1, corresponding to the limiting value of @code{sin(x)/x}.

When @code{sinc} is applied to a symbolic expression, the result is the
quotient @code{sin(x)/x}.  When @code{$numer} is @code{true} and the
argument is a floating or complex floating number, @code{sinc} performs
floating‑point evaluation.

Examples:

@example
(%i1) sinc(%pi/3);
(%o1) 3/(2 %pi)

(%i2) sinc(1.2 - 4.5*%i);
(%o2) 5.7043918199347985 + 7.802144269985125 %i

(%i3) integrate(sinc(x), x);
(%o3) si(x)

(%i4) taylor(sinc(x), x, 0, 5);
(%o4) 1 - x^2/6 + x^4/120 + O(x^6)

(%i5) powerseries(sinc(x), x, 0);
(%o5) sum((-1)^k * x^(2*k) / (2*k+1)!, k, 0, inf)
@end example

@end defun

