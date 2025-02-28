# AssessmentEvent
`toloka.client.conditions.AssessmentEvent` | [Source code](https://github.com/Toloka/toloka-kit/blob/v1.1.0.post1/src/client/conditions.py#L105)

```python
AssessmentEvent(
    self,
    operator: IdentityOperator,
    value: Union[Type, str, None] = None
)
```

An assignment status change event.


Possible values:
    * `ACCEPT` — An assignment was accepted.
    * `ACCEPT_AFTER_REJECT` — An assignment with the previously set `REJECTED` status was accepted.
    * `REJECT` — An assignment was rejected.

`AssessmentEvent` condition can be used with the `==` operator only.

`AssessmentEvent` is used with collectors:
- [AssignmentsAssessment](toloka.client.collectors.AssignmentsAssessment.md).


**Examples:**

The example shows how to automatically increase the overlap of a task suite when an assignment was rejected.

```python
new_pool = toloka.pool.Pool(....)
new_pool.quality_control.add_action(
    collector=toloka.collectors.AssignmentsAssessment(),
    conditions=[toloka.conditions.AssessmentEvent == toloka.conditions.AssessmentEvent.REJECT],
    action=toloka.actions.ChangeOverlap(delta=1, open_pool=True),
)
```
