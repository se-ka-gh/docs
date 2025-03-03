# UserBonusSearchResult
`toloka.client.search_results.UserBonusSearchResult`

```python
UserBonusSearchResult(
    self,
    *,
    items: Optional[List[UserBonus]] = None,
    has_more: Optional[bool] = None
)
```

The result of searching Tolokers' rewards.

## Parameters Description

| Parameters | Type | Description |
| :----------| :----| :-----------|
`items`|**Optional\[List\[[UserBonus](toloka.client.user_bonus.UserBonus.md)\]\]**|<p>A list with found rewards.</p>
`has_more`|**Optional\[bool\]**|<p>A flag showing whether there are more matching rewards.</p> <ul> <li>`True` — There are more matching rewards, not included in `items` due to the limit set in the search request.</li> <li>`False` — `items` contains all matching rewards.</li> </ul>
