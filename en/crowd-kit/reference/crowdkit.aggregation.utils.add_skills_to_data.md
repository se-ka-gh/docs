# add_skills_to_data
`crowdkit.aggregation.utils.add_skills_to_data` | [Source code](https://github.com/Toloka/crowd-kit/blob/v1.1.0/crowdkit/aggregation/utils.py#L153)

```python
add_skills_to_data(
    data: DataFrame,
    skills: Series,
    on_missing_skill: str,
    default_skill: Optional[float]
)
```

## Parameters Description

| Parameters | Type | Description |
| :----------| :----| :-----------|
`skills`|**Series**|<p>workers&#x27; skills. A pandas.Series index by workers and holding corresponding worker&#x27;s skill</p>
`on_missing_skill`|**str**|<p>How to handle assignments done by workers with unknown skill. Possible values:</p> <ul> <li>&quot;error&quot; — raise an exception if there is at least one assignment done by user with unknown skill;</li> <li>&quot;ignore&quot; — drop assignments with unknown skill values during prediction. Raise an exception if there is no assignments with known skill for any task;</li> <li>value — default value will be used if skill is missing.</li> </ul>
