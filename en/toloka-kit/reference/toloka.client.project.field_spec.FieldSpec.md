# FieldSpec
`toloka.client.project.field_spec.FieldSpec` | [Source code](https://github.com/Toloka/toloka-kit/blob/v1.1.0.post1/src/client/project/field_spec.py#L48)

```python
FieldSpec(
    self,
    *,
    required: Optional[bool] = True,
    hidden: Optional[bool] = False
)
```

A base class for field specifications used in project's `input_spec` and `output_spec`


for input and response data validation specification respectively. Use subclasses of this
class defined below to define the data type (string, integer, URL, etc.) and specify
validation parameters (such as string length).

## Parameters Description

| Parameters | Type | Description |
| :----------| :----| :-----------|
`required`|**Optional\[bool\]**|<p>Whether the object or input field is required.</p>
`hidden`|**Optional\[bool\]**|<p>Whether to hide the input field from Tolokers.</p>
