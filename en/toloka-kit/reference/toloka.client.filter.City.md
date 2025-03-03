# City
`toloka.client.filter.City` | [Source code](https://github.com/Toloka/toloka-kit/blob/v1.1.0.post1/src/client/filter.py#L355)

```python
City(
    self,
    operator: InclusionOperator,
    value: int
)
```

Filtering Tolokers by a city specified in their profiles.

## Parameters Description

| Parameters | Type | Description |
| :----------| :----| :-----------|
`operator`|**[InclusionOperator](toloka.client.primitives.operators.InclusionOperator.md)**|<p>An operator used in a condition. Allowed set of operators depends on the filter.</p>
`value`|**int**|<p>The [ID](https://toloka.ai/en/docs/api/concepts/regions) of the city.</p>
