# action.set

Sets the value from `payload` in the data in the `data` property.

[Learn more about working with data](../operations/work-with-data.md).

For example, let's say you want to add shortcuts for the [field.radio-group](field.radio-group.md) option. You need the shortcut to perform the same action as the selected option, which is to set the specified value in the data. To set this action, use `action.set`.

[![image](../_images/buttons/view-example.svg)](https://clck.ru/asRw2)

As another example, you can use this component to count the number of clicks on an option and write the value in the output data. When the page is refreshed, set the value to 0.

[![image](../_images/buttons/view-example.svg)](https://clck.ru/asRwg)

## Component properties {#properties}

#|
|| **Name** | **Type** | **Description** ||
|| `type`<span style="color: red">\*</span> | "action.set" | Set component type ||
|| `data` | _writable_ | Data with values that will be processed or changed. ||
|| `payload` | _any_ | The value to write to the data. ||
|#
