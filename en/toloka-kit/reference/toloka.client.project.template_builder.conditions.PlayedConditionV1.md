# PlayedConditionV1
`toloka.client.project.template_builder.conditions.PlayedConditionV1` | [Source code](https://github.com/Toloka/toloka-kit/blob/v1.1.0.post1/src/client/project/template_builder/conditions.py#L193)

```python
PlayedConditionV1(
    self,
    *,
    hint: Optional[Any] = None,
    version: Optional[str] = '1.0.0'
)
```

Checks the start of playback.


Validation will be passed if playback is started. To play media with the condition.played check, you can use
view.audio and view.video. The condition.played check only works in the player's validation property.

## Parameters Description

| Parameters | Type | Description |
| :----------| :----| :-----------|
`hint`|**Optional\[Any\]**|<p>Validation error message that a Toloker will see.</p>
