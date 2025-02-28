# UserBonusSortItems
`toloka.client.search_requests.UserBonusSortItems`

```python
UserBonusSortItems(self, items=None)
```

Keys for sorting rewards in search results.

## Parameters Description

| Parameters | Type | Description |
| :----------| :----| :-----------|
`items`|**Optional\[List\[[SortItem](toloka.client.search_requests.UserBonusSortItems.SortItem.md)\]\]**|<p>A list of sorting keys. Supported values:</p> <ul> <li>`&#x27;id&#x27;` — The ID of a reward.</li> <li>`&#x27;created&#x27;` — The date of granting a reward.</li> </ul>

**Examples:**

The example shows how to find rewards sorted by granting date in descending order. Rewards with equal granting dates are sorted by IDs in ascending order.

```python
sort = toloka.client.search_requests.UserBonusSortItems(['-created', 'id'])
result = toloka_client.find_user_bonuses(user_id=best_toloker_id, sort=sort, limit=10)
```
