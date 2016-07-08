MiniPi
==

Mini Pi approximations in JS (WIP)

---

*Gregory-Leibniz series:*

π = (4/1) - (4/3) + (4/5) - (4/7) + (4/9) - (4/11) + (4/13) - (4/15) ...

(super inefficient: ~3h to get 6 decimals, ~18h to get 7 decimals, ...)

- [commented](http://xem.github.io/miniPi/1.html)
- [golfed](http://xem.github.io/miniPi/1.min.html) (256b)

---

*Nilakantha series:*

π = 3 + (4/(2*3*4)) - (4/(4*5*6)) + (4/(6*7*8)) - ...

(exponential: computes 10+ decimals in a few seconds then it gets very long)

- [commented](http://xem.github.io/miniPi/2.html)
- [golfed](http://xem.github.io/miniPi/2.min.html) (241b)

---

*Machin formula:*
π = 16*atan(1/5) - 4*atan(1/239)<br>
with atan(x) = x - x^3/3 + x^5/5 - ...

(linear! computes ~1,4 digit per iteration, inspired by http://stephenbrooks.org/misc/jspi/decimal_animated.html, to recode properly)

- [commented](http://xem.github.io/miniPi/3.html)

---

*Other "simple" formulae to test maybe:*

- Pi = x * sin(180 / x), for x as big as possible
- pi = 2 * (Arcsin(sqrt(1 - x^2)) + abs(Arcsin(x))), for x in [-1;1]
- pi = (k_6 sqrt(k_3))/(S), where k_1 = 545140134; k_2 = 13591409; k_3 = 640320; k_4 = 100100025; k_5 = 327843840; k_6 = 53360; S = sum_(n = 0)^oo (-1)^n ((6n)!(k_2 + nk_1))/(n!^3(3n)!(8k_4k_5)^n)
