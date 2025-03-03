# create_user_bonus
`toloka.async_client.client.AsyncTolokaClient.create_user_bonus` | [Source code](https://github.com/Toloka/toloka-kit/blob/v1.1.0.post1/src/client/__init__.py#L0)

Issues payments directly to a Toloker.


You can send a maximum of 10,000 requests of this kind per day.

## Parameters Description

| Parameters | Type | Description |
| :----------| :----| :-----------|
`user_bonus`|**[UserBonus](toloka.client.user_bonus.UserBonus.md)**|<p>To whom, how much to pay and for what.</p>
`operation_id`|**Optional\[str\]**|<p>Operation ID. If asynchronous creation is used, by this identifier you can later get results of creating bonuses.</p>
`skip_invalid_items`|**Optional\[bool\]**|<p>Validation parameters of objects:</p> <ul> <li>True - Award a bonus if the object with bonus information passed validation. Otherwise, skip the bonus.</li> <li>False - Default behavior. Stop the operation and don&#x27;t award bonuses if at least one object didn&#x27;t pass validation.</li> </ul>

* **Returns:**

  Created bonus.

* **Return type:**

  [UserBonus](toloka.client.user_bonus.UserBonus.md)

**Examples:**

Create bonus for specific assignment.

```python
import decimal
new_bonus = toloka_client.create_user_bonus(
    UserBonus(
        user_id='1',
        amount=decimal.Decimal('0.50'),
        public_title={
            'EN': 'Perfect job!',
            'RU': 'Прекрасная работа!',
        },
        public_message={
            'EN': 'You are the best!',
            'RU': 'Молодец!',
        },
        assignment_id='012345'
    )
)
```
