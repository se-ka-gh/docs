# LinkOpenedConditionV1
`toloka.client.project.template_builder.conditions.LinkOpenedConditionV1` | [Source code](https://github.com/Toloka/toloka-kit/blob/v1.1.0.post1/src/client/project/template_builder/conditions.py#L166)

```python
LinkOpenedConditionV1(
    self,
    url: Optional[Any] = None,
    *,
    hint: Optional[Any] = None,
    version: Optional[str] = '1.0.0'
)
```

Checks that the Toloker clicked the link.


Important: To trigger the condition, the Toloker must follow the link from the Toloka interface — you must give Tolokers
this option. The condition will not work if the Toloker opens the link from the browser address bar.

This condition can be used in the view.link component and also anywhere you can use (conditions).

## Parameters Description

| Parameters | Type | Description |
| :----------| :----| :-----------|
`url`|**Optional\[Any\]**|<p>The link that must be clicked.</p>
`hint`|**Optional\[Any\]**|<p>Validation error message that a Toloker will see.</p>
