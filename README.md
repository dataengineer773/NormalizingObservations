We want to rescale the feature values of observations to have unit norm (a total length of 1), Use Normalizer with a norm argument Many rescaling methods (e.g., min-max scaling and standardization) operate on features; however, we
can also rescale across individual observations. Normalizer rescales the values on individual
observations to have unit norm (the sum of their lengths is 1). This type of rescaling is often used when
we have many equivalent features (e.g., text classification when every word or n-word group is a
feature). Normalizer provides three norm options with Euclidean norm (often called L2) being the default
argument where x is an individual observation and xn
is that observation’s value for the nth feature. Alternatively, we can specify Manhattan norm (L1), Intuitively, L2 norm can be thought of as the distance between two points in New York for a bird (i.e., a
straight line), while L1 can be thought of as the distance for a human walking on the street (walk north
one block, east one block, north one block, east one block, etc.), which is why it is called “Manhattan
norm” or “Taxicab norm.”
Practically, notice that norm='l1' rescales an observation’s values so they sum to 1, which can
sometimes be a desirable quality 
