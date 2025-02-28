# CreateTasksParameters
`toloka.client.task.CreateTasksParameters` | [Source code](https://github.com/Toloka/toloka-kit/blob/v1.1.0.post1/src/client/task.py#L134)

```python
CreateTasksParameters(
    self,
    *,
    allow_defaults: Optional[bool] = None,
    open_pool: Optional[bool] = None,
    skip_invalid_items: Optional[bool] = None,
    operation_id: Optional[UUID] = None,
    async_mode: Optional[bool] = True
)
```

Parameters used with the [create_tasks](toloka.client.TolokaClient.create_tasks.md) method.


If the operation is started in an asynchronous mode,
we recommend that you send the `operation_id` to avoid creating the same tasks multiple times. You can use this ID later to get information about the operation.

## Parameters Description

| Parameters | Type | Description |
| :----------| :----| :-----------|
`allow_defaults`|**Optional\[bool\]**|<p>Active overlap setting:</p> <ul> <li>True — Use the overlap that is set in the `defaults.default_overlap_for_new_tasks` pool parameter.</li> <li>False — Use the overlap that is set in the `overlap` task parameter.</li> </ul> <p></p><p>Default value: `False`.</p>
`open_pool`|**Optional\[bool\]**|<p>Open the pool immediately after creating a task suite, if the pool is closed. </p><p>Default value: `False`.</p>
`skip_invalid_items`|**Optional\[bool\]**|<p>Task validation option:</p> <ul> <li>True — All valid tasks are added. If a task does not pass validation, then it is not added to Toloka. All such tasks are listed in the response.</li> <li>False — If any task does not pass validation, then the operation is cancelled and no tasks are added to Toloka.</li> </ul> <p></p><p>Default value: `False`.</p>
`operation_id`|**Optional\[UUID\]**|<p>The ID of the operation conforming to the [RFC4122 standard](https://tools.ietf.org/html/rfc4122). Use it if the `async_mode` is set to `True`.</p>
`async_mode`|**Optional\[bool\]**|<p>Request processing mode:</p> <ul> <li>True — Asynchronous operation is started internally and `create_tasks` waits for the completion of it. It is recommended to create no more than 10,000 tasks per request in this mode.</li> <li>False — The request is processed synchronously. A maximum of 5000 tasks can be added in a single request in this mode.</li> </ul> <p></p><p>Default value: `False`.</p>
