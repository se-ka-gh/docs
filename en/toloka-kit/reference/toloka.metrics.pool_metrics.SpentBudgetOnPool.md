# SpentBudgetOnPool
`toloka.metrics.pool_metrics.SpentBudgetOnPool` | [Source code](https://github.com/Toloka/toloka-kit/blob/v1.1.0.post1/src/metrics/pool_metrics.py#L330)

```python
SpentBudgetOnPool(
    self,
    pool_id: str,
    money_name: Optional[str] = None,
    *,
    toloka_client: Optional[TolokaClient] = None,
    atoloka_client: Optional[AsyncTolokaClient] = None,
    timeout: timedelta = ...
)
```

How much money has already been spent on this pool, excluding fee.

## Parameters Description

| Parameters | Type | Description |
| :----------| :----| :-----------|
`pool_id`|**str**|<p>From which pool track metrics.</p>
`tasks_name`|**-**|<p>Metric name for a count of tasks.</p>

**Examples:**

How to collect this metrics:
```python
def print_metric(metric_dict):
    print(metric_dict)

collector = MetricCollector([SpentBudgetOnPool(pool_id, toloka_client=toloka_client)], print_metric)
asyncio.run(collector.run())
```
    'spent_money': [(datetime.datetime(2021, 11, 18, 9, 36, 34, 163000), Decimal('0.3'))],
}
## Methods Summary

| Method | Description |
| :------| :-----------|
[get_line_names](toloka.metrics.pool_metrics.SpentBudgetOnPool.get_line_names.md)| Returns a list of metric names that can be generated by this class instance.
