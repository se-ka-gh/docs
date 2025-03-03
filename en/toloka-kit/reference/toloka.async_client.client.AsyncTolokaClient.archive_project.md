# archive_project
`toloka.async_client.client.AsyncTolokaClient.archive_project` | [Source code](https://github.com/Toloka/toloka-kit/blob/v1.1.0.post1/src/async_client/client.py#L0)

```python
async archive_project(self, project_id: str)
```

Sends project to archive


Use it when you have no need this project anymore. To perform the operation, all pools in the project must be archived.
The archived project is not deleted. You can access it when you will need it.

## Parameters Description

| Parameters | Type | Description |
| :----------| :----| :-----------|
`project_id`|**str**|<p>ID of project that will be archived.</p>

* **Returns:**

  Object with updated status.

* **Return type:**

  [Project](toloka.client.project.Project.md)

**Examples:**


```python
toloka_client.archive_project(project_id='1')
```
