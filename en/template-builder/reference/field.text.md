# field.text

A field for entering a short text, not more than a line. To add a field for entering multiple lines of text, use [field.textarea](field.textarea.md).

[![image](../_images/buttons/view-example.svg)](https://clck.ru/asSa5)

## Component properties {#properties}

#|
|| **Name** | **Type** | **Description** ||
|| `type`<span style="color: red">\*</span> | "field.text" | Set component type ||
|| `data`<span style="color: red">\*</span> | _writable_ | Data with values that will be processed or changed. ||
|| `label` | _string_ | Label above the component. ||
|| `disabled` | _boolean_ | If `true`, editing is not available. ||
|| `hint` | _string_ | Hint text. ||
|| `placeholder` | _string_ | A semi-transparent label that is shown in the box when it is empty. ||
|| `requiredMark` | _boolean_ | Show "\*" next to the label ||
|| `rtl` | _object_ | In some languages, like Arabic or Hebrew, text is written from right to left. Use this property to set up the correct display mode for the component.

[![image](../_images/buttons/view-example.svg)](https://clck.ru/amHA8)

[Learn more about RTL languages](https://www.w3.org/International/questions/qa-scripts). ||
|| `rtl.mode` | _string_ | Display mode:

- `ltr` — left to right.
- `rtl` — right to left.

The chosen value will be added to the `dir` attribute in the component's HTML code. [Learn more about dir](https://www.w3.org/International/questions/qa-html-dir). ||
|| `validation` | _condition_ | Validation based on condition. ||
|#
