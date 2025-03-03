# get_projects
`toloka.async_client.client.AsyncTolokaClient.get_projects` | [Source code](https://github.com/Toloka/toloka-kit/blob/v1.1.0.post1/src/client/__init__.py#L0)

Finds all projects that match certain criteria.


`get_projects` returns a generator. You can iterate over all found projects using the generator. Several requests to the Toloka server are possible while iterating.

If you need to sort projects use the [find_projects](toloka.client.TolokaClient.find_projects.md) method.

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

* **Yields:**

  The next matching project.

* **Yield type:**

  [AsyncGenAdapter](toloka.util.async_utils.AsyncGenAdapter.md)\[[Project](toloka.client.project.Project.md), None\]

**Examples:**

Get all active projects.

```python
active_projects = toloka_client.get_projects(status='ACTIVE')
```

Get all your projects.

```python
my_projects = toloka_client.get_projects()
```
