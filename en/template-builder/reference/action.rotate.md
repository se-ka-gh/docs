# action.rotate

Rotates the specified component by 90 degrees.

By default it rotates to the right, but you can specify the direction in the `payload` property.

[![image](../_images/buttons/view-example.svg)](https://clck.ru/asRrg)

## Component properties {#properties}

#|
|| **Name** | **Type** | **Description** ||
|| `type`<span style="color: red">\*</span> | "action.rotate" | Set component type ||
|| `payload` | _string_ | Sets the direction of rotation:

- `right` (default).
- `left`. ||
  || `view` | _ref_ | Points to the component to perform the action with. ||
  |#
