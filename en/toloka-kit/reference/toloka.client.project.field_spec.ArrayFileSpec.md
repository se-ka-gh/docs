# ArrayFileSpec
`toloka.client.project.field_spec.ArrayFileSpec` | [Source code](https://github.com/Toloka/toloka-kit/blob/v1.1.0.post1/src/client/project/field_spec.py#L201)

```python
ArrayFileSpec(
    self,
    *,
    required: Optional[bool] = True,
    hidden: Optional[bool] = False,
    min_size: Optional[int] = None,
    max_size: Optional[int] = None
)
```

A file array field specification (only for output data)

## Parameters Description

| Parameters | Type | Description |
| :----------| :----| :-----------|
`required`|**Optional\[bool\]**|<p>Whether the object or input field is required.</p>
`hidden`|**Optional\[bool\]**|<p>Whether to hide the input field from Tolokers.</p>
`min_size`|**Optional\[int\]**|<p>Minimum number of elements in the array</p>
`max_size`|**Optional\[int\]**|<p>Maximum number of elements in the array</p>
