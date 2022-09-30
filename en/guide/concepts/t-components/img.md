# Image

{% note info %}

The task interface configuration guide describes the features of the HTML/JS/CSS editor. You can also try adding an image in {% if locale == "en-com" %}[Template Builder](https://toloka.ai/en/docs/template-builder/operations/insert-images){% endif %}.

{% endnote %}


To add an image to the task, use the `{{img src=<image URL>}}` component. Example:

```no-highlight
{{img src=url width="100px" height="75px"}}
```

You [can store your files in Yandex Cloud](../use-object-storage.md).

#### Parameters


Parameter
 |
Description
 |
Required
 |
Default value

----- | ----- | ----- | -----
``` src ``` | Image URL. Supported values:<br/><br/>- URL from the task [input](../../../glossary.md#input-output-data-ru) data. For example, from the field with `url` ID: `src=url`.<br/>    <br/>- Direct link. The HTTPS protocol is recommended. For example, `src="https://mywebsite.ru/img1.png"`. | yes | no
``` width ``` | Width of the image. Set in the following units:<br/><br/>- Pixels. For example, `width="100px"`.<br/>    <br/>- Percentage of the size of the parent element. For example, `width="100%"`.<br/>    <br/><br/>You can also use a formula for setting the width. For example, `width="calc(100%-30px)"`. | no | ``` "300px" ```
``` height ``` | Height of the image. Set in the following units:<br/><br/>- Pixels. For example, `height="100px"`.<br/>    <br/>- Percentage of the size of the parent element. For example, `height="100%"`.<br/>    <br/><br/>You can also use a formula for setting the width. For example, `height="calc(100%-30px)"`. | no | ``` "300px" ```
``` real-size ``` | Image scale. Acceptable values:<br/><br/>- `real-size=false` — Stretch the image to the size of the parent element.<br/>    <br/>- `real-size=true` — Use the original image size (if it isn't larger than the size of the parent element). | no | ``` false ```
``` class ``` | CSS class for the image. | no | ``` ".img" ```

{% include [contact-support](../../_includes/contact-support-help.md) %}