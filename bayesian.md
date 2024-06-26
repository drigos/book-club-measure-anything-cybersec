https://en.wikipedia.org/wiki/Bayesian_statistics

```
P(A|B) = P(B|A) * P(A)
         -------------
              P(B)
```

```
            ~a                      a
    +--------------------------------------------+
    |                   /                        |
 h  |       x1         /           x2            |
    |                 /                          |
    |----------------/---------------------------|
    |               /                            |
 ~h |       x3     /               x4            |
    |             /                              |
    +--------------------------------------------+

tot = 100

h = 50 | ~h = 50
a = 70 | ~a = 30

x1 = 20
x2 = 30
x3 = 10
x4 = 40

p(a) = x2+x4 / x1+x2+x3+x4
p(a) = 70 / 100
p(a) = 0.70

p(h) = x1+x2 / x1+x2+x3+x4
p(h) = 50 / 100
p(h) = 0.50

p(h|a) = x2 / x2+x4
p(h|a) = 30 / 70
p(h|a) = 0.43

p(a|h) = x2 / x1+x2
p(a|h) = 30 / 50
p(a|h) = 0.60
```

```
p(a|h) = p(a) * p(h|a)
         -------------
             p(h)

# p(a|h) = (x2+x4 / x1+x2+x3+x4) * (x2 / x2+x4) / (x1+x2 / x1+x2+x3+x4)

p(a|h) = (    x2+x4    )   (  x2   )
         ( ----------- ) * ( ----- )
         ( x1+x2+x3+x4 )   ( x2+x4 )
         ---------------------------
               (    x1+x2    )
               ( ----------- )
               ( x1+x2+x3+x4 )

# p(a|h) = (x2+x4 / x1+x2+x3+x4) * (x2 / x2+x4) * (x1+x2+x3+x4 / x1+x2)

p(a|h) = (    x2+x4    )   (  x2   )   ( x1+x2+x3+x4 )
         ( ----------- ) * ( ----- ) * ( ----------- )
         ( x1+x2+x3+x4 )   ( x2+x4 )   (    x1+x2    )

p(a|h) = (x2+x4) * (x2 / x2+x4) * (1 / x1+x2)

p(a|h) = (      1      )   (  x2   )   (      1      )
                         *           * ( ----------- )
                                       (    x1+x2    )

p(a|h) = x2 / x1+x2
```


