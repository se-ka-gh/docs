# close_pool
`toloka.async_client.client.AsyncTolokaClient.close_pool` | [Source code](https://github.com/Toloka/toloka-kit/blob/v1.1.0.post1/src/async_client/client.py#L0)

```python
async close_pool(self, pool_id: str)
```

Stops distributing tasks from the pool


If all tasks done, the pool will be closed automatically.

## Parameters Description

| Parameters | Type | Description |
| :----------| :----| :-----------|
`pool_id`|**str**|<p>ID of the pool that will be closed.</p>

* **Returns:**

  Pool object with new status.

* **Return type:**

  [Pool](toloka.client.pool.Pool.md)

**Examples:**


```python
open_pool = next(toloka_client.get_pools(status='OPEN'))
toloka_client.close_pool(pool_id=open_pool.id)
```
