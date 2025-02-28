# uncertainty
`crowdkit.metrics.data._classification.uncertainty` | [Source code](https://github.com/Toloka/crowd-kit/blob/v1.1.0/crowdkit/metrics/data/_classification.py#L102)

```python
uncertainty(
    answers: DataFrame,
    workers_skills: Optional[Series] = None,
    aggregator: Optional[BaseClassificationAggregator] = None,
    compute_by: str = 'task',
    aggregate: bool = True
)
```

Label uncertainty metric: entropy of labels probability distribution.


Computed as Shannon's Entropy with label probabilities computed either for tasks or workers:
$$H(L) = -\sum_{label_i \in L} p(label_i) \cdot \log(p(label_i))$$

## Parameters Description

| Parameters | Type | Description |
| :----------| :----| :-----------|
`answers`|**DataFrame**|<p>Workers&#x27; labeling results. A pandas.DataFrame containing `task`, `worker` and `label` columns.</p>
`workers_skills`|**Optional\[Series\]**|<p>workers&#x27; skills. A pandas.Series index by workers and holding corresponding worker&#x27;s skill</p>

* **Returns:**

  Union[float, pd.Series]

* **Return type:**

  Union\[float, Series\]

**Examples:**

Mean task uncertainty minimal, as all answers to task are same.

```python
uncertainty(pd.DataFrame.from_records([
    {'task': 'X', 'worker': 'A', 'label': 'Yes'},
    {'task': 'X', 'worker': 'B', 'label': 'Yes'},
]))
```

Mean task uncertainty maximal, as all answers to task are different.

```python
uncertainty(pd.DataFrame.from_records([
    {'task': 'X', 'worker': 'A', 'label': 'Yes'},
    {'task': 'X', 'worker': 'B', 'label': 'No'},
    {'task': 'X', 'worker': 'C', 'label': 'Maybe'},
]))
```

Uncertainty by task without averaging.

```python
uncertainty(pd.DataFrame.from_records([
    {'task': 'X', 'worker': 'A', 'label': 'Yes'},
    {'task': 'X', 'worker': 'B', 'label': 'No'},
    {'task': 'Y', 'worker': 'A', 'label': 'Yes'},
    {'task': 'Y', 'worker': 'B', 'label': 'Yes'},
]),
workers_skills=pd.Series([1, 1], index=['A', 'B']),
compute_by="task", aggregate=False)
```
X    0.693147
Y    0.000000
dtype: float64

Uncertainty by worker

```python
uncertainty(pd.DataFrame.from_records([
    {'task': 'X', 'worker': 'A', 'label': 'Yes'},
    {'task': 'X', 'worker': 'B', 'label': 'No'},
    {'task': 'Y', 'worker': 'A', 'label': 'Yes'},
    {'task': 'Y', 'worker': 'B', 'label': 'Yes'},
]),
workers_skills=pd.Series([1, 1], index=['A', 'B']),
compute_by="worker", aggregate=False)
```
A    0.000000
B    0.693147
dtype: float64
