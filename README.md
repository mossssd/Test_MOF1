#Mass ratio varcine based Outlier Factor (MOF)

An outlier of a finite dataset in statistics is defined as a data point that differs significantly from others. It is normally surrounded by a few data points, while normal ones are engulfed by others. This behavior leads to the proposed outlier factor called Mass-ratio-variance Outlier Factor (MOF). A score is assigned to a data point based on the variance of the mass-ratio distribution from the rest of the data points. Within a sphere of an outlier, there will be a few data points compared to a normal one. So, the mass-ratio of an outlier will be different from that of a normal data point. The algorithm to generate MOF requires no parameters and embraces the density concept.

## Installation

```bash
pip install MOF
```
## Example

```python
from MOF import MOF
import numpy as np

x_train = np.array([[0,1],[1,1],[2,1],[3,1],[0,0],[1,0],[2,0],[3,0],[0,-1],[1,-1],[2,-1],[3,-1],[8,4]])
model = MOF()
model.fit(x_train)
print(model.decision_scores_)
x_test = np.array([[20,20],[3,3],[5,5]])
print(model.predict_score(x_test)
```
## Requirements
Numpy, Spicy and Numba
##Reference
Changsakul P, Boonsiri S, Sinapiromsaran K. Mass-ratio-variance based Outlier Factor. In2021 18th International Joint Conference on Computer Science and Software Engineering (JCSSE) 2021 Jun 30 (pp. 1-5). IEEE.