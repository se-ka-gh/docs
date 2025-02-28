# ProjectSearchRequest
`toloka.client.search_requests.ProjectSearchRequest` | [Source code](https://github.com/Toloka/toloka-kit/blob/v1.1.0.post1/src/client/search_requests.py#L178)

```python
ProjectSearchRequest(
    self,
    status: Optional[Project.ProjectStatus] = None,
    id_lt: Optional[str] = None,
    id_lte: Optional[str] = None,
    id_gt: Optional[str] = None,
    id_gte: Optional[str] = None,
    created_lt: Optional[datetime] = None,
    created_lte: Optional[datetime] = None,
    created_gt: Optional[datetime] = None,
    created_gte: Optional[datetime] = None
)
```

Parameters for searching projects.

## Parameters Description

| Parameters | Type | Description |
| :----------| :----| :-----------|
`status`|**Optional\[[Project.ProjectStatus](toloka.client.project.Project.ProjectStatus.md)\]**|<p>Project status. Refer to the [ProjectStatus](toloka.client.project.Project.ProjectStatus.md) page for more information on the available `status` values.</p>
`id_lt`|**Optional\[str\]**|<p>Projects with IDs less than the specified value.</p>
`id_lte`|**Optional\[str\]**|<p>Projects with IDs less than or equal to the specified value.</p>
`id_gt`|**Optional\[str\]**|<p>Projects with IDs greater than the specified value.</p>
`id_gte`|**Optional\[str\]**|<p>Projects with IDs greater than or equal to the specified value.</p>
`created_lt`|**Optional\[datetime\]**|<p>Projects created before the specified date.</p>
`created_lte`|**Optional\[datetime\]**|<p>Projects created before or on the specified date.</p>
`created_gt`|**Optional\[datetime\]**|<p>Projects created after the specified date.</p>
`created_gte`|**Optional\[datetime\]**|<p>Projects created after or on the specified date.</p>
