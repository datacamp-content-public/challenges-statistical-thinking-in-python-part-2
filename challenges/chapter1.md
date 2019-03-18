---
title: 'Chapter 1: Parameter estimation by optimization'
output: html_document
description: ""
---

## [MC] Choose the right answer

```yaml
type: MultipleChoiceChallenge
key: d688ac0440
```

`@assignment1`
Choose the right answer about **Optimal Parameters**.

`@options1`
- They are calculated from the observed data.
- They represent parameters that best approximates the model the actual data.
- Their relevance depends if the selected model is appropriate for the observed data.
- [All the alternatives.]

---

## Insert challenge title here

```yaml
type: BlanksChallenge
key: f23838a536
```

`@context`


`@code1`
```{python}
data = {{var1}}
print({{func1}}(data))
```

`@pre_challenge_code`
```{python}
import dccpu.generators as g
```

`@variables`
```yaml
var1:
- '!expr g.int_vector(lo=-2, hi=2, sort=True, size=4)'
func1:
- 'np.mean'
```

`@distractors`
```yaml
func1:
- 'np.std'
- 'np.max'
- 'np.min'
```

---

## [BC] Creating theoretical distributions

```yaml
type: BlanksChallenge
key: 2412b0e696
```

`@context`
Consider observations stored in `data` and assume that this variable has a normal distribution. The package `numpy` has been imported as `np`.

`@code1`
```{python}
import numpy as np
data = [1, 5, 1, 2, 1]
{{mean}}
{{std}}
{{samples}}
(len(samples))
```

`@pre_challenge_code`
```{python}

```

`@variables`
```yaml
mean:
- 'np.mean(data)'
std:
- 'np.std(data)'
samples:
- 'samples = np.random.normal(mean, std, size=10000)'
```

`@distractors`
```yaml
mean:
- 'np.avg(data)'
std:
- 'std = np.standard(data)'
samples:
- 'samples = np.normal(mean, std, size=10000)'
```

---

## [OC] popping lists

```yaml
type: OutputChallenge
key: 6258197972
```

`@context`
Consider observations stored in `data`, assuming that this varaible has an normal distribution

`@code1`
```{python}
l1 = {{$l1}}
p = l1.pop()
print(p)
```

`@code2`
```{python}
l1 = {{$l1}}
p = l1.pop({{n}})
print(p)
```

`@pre_challenge_code`
```{python}
import dccpu.generators as g
```

`@variables`
```yaml
l1:
- '!expr g.int_vector(size=6)'
n:
- '!expr g.rand_int(hi=5)'
```

---

## [BC] concatenating lists

```yaml
type: BlanksChallenge
key: 8a565a9166
```

`@context`


`@code1`
```{python}
l1 = {{l1}}
l2 = {{l2}}
print(l1 {{_op}} l2)
```

`@pre_challenge_code`
```{python}
import dccpu.generators as g
```

`@variables`
```yaml
l1:
- '!expr g.int_vector(size=3)'
l2:
- '!expr g.int_vector(size=3)'
:
- '+'
```

`@distractors`
```yaml
op:
- '-'
- '*'
```
