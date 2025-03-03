# DistanceConditionV1
`toloka.client.project.template_builder.conditions.DistanceConditionV1` | [Source code](https://github.com/Toloka/toloka-kit/blob/v1.1.0.post1/src/client/project/template_builder/conditions.py#L93)

```python
DistanceConditionV1(
    self,
    from_: Optional[Union[BaseComponent, str]] = None,
    to_: Optional[Union[BaseComponent, str]] = None,
    max: Optional[Union[BaseComponent, float]] = None,
    *,
    hint: Optional[Any] = None,
    version: Optional[str] = '1.0.0'
)
```

This component checks whether the sent coordinates match the ones that you specified


For example, you want a Toloker to take a photo of a specific place. The condition.distance component checks whether
the photo was taken at the location that you specified.

## Parameters Description

| Parameters | Type | Description |
| :----------| :----| :-----------|
`from_`|**Optional\[Union\[[BaseComponent](toloka.client.project.template_builder.base.BaseComponent.md), str\]\]**|<p>First point.</p>
`to_`|**Optional\[Union\[[BaseComponent](toloka.client.project.template_builder.base.BaseComponent.md), str\]\]**|<p>Second point.</p>
`max`|**Optional\[Union\[[BaseComponent](toloka.client.project.template_builder.base.BaseComponent.md), float\]\]**|<p>The distance in meters by which the X and Y coordinates may differ.</p>
`hint`|**Optional\[Any\]**|<p>Validation error message that a Toloker will see.</p>

**Examples:**

How to check that a Toloker is in the right place.

```python
distance_condition = tb.conditions.DistanceConditionV1(
    tb.data.LocationData(),
    tb.data.InputData('coordinates'),
    500,
    hint='You are too far from the destination coordinates.',
),
```
