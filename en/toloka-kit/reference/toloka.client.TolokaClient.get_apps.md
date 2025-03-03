# get_apps
`toloka.client.TolokaClient.get_apps` | [Source code](https://github.com/Toloka/toloka-kit/blob/v1.1.0.post1/src/client/__init__.py#L3580)

Finds all App solutions that match certain criteria.


`get_apps` returns a generator. You can iterate over all found solutions using the generator. Several requests to the Toloka server are possible while iterating.

If you need to sort solutions use the [find_apps](toloka.client.TolokaClient.find_apps.md) method.

## Parameters Description

| Parameters | Type | Description |
| :----------| :----| :-----------|
`after_id`|**Optional\[str\]**|<p>The ID of a solution used for cursor pagination.</p>
`lang`|**Optional\[str\]**|<p>ISO 639 language code.</p>
`id_gt`|**Optional\[str\]**|<p>Solutions with IDs greater than the specified value.</p>
`id_gte`|**Optional\[str\]**|<p>Solutions with IDs greater than or equal to the specified value.</p>
`id_lt`|**Optional\[str\]**|<p>Solutions with IDs less than the specified value.</p>
`id_lte`|**Optional\[str\]**|<p>Solutions with IDs less than or equal to the specified value.</p>
`name_gt`|**-**|<p>Solutions with names lexicographically greater than the specified value.</p>
`name_gte`|**-**|<p>Solutions with names lexicographically greater than or equal to the specified value.</p>
`name_lt`|**-**|<p>Solutions with names lexicographically less than the specified value.</p>
`name_lte`|**-**|<p>Solutions with names lexicographically less than or equal to the specified value.</p>

* **Yields:**

  The next matching solution.

* **Yield type:**

  Generator\[[App](toloka.client.app.App.md), None, None\]
