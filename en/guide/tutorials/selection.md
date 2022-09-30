# Object recognition & detection

In this tutorial, you will learn how to run object recognition in Toloka. We will use a project preset designed specifically for this type of data labeling.

Object recognition is a type of data labeling task with an image and an editor for selecting an image area.

Tolokers look at the image and select the objects that you need to detect. After you collect all the labeled images, you can apply your dataset for computer vision training.

## Prerequisites {#prerequisites}

Before you begin:

- {% include [tutorials-register](../_includes/tutorials/register.md) %}

- {% include [tutorials-top-up-tutorial](../_includes/tutorials/top-up-tutorial.md) %}

## Choose a preset {#preset}

{% include [toloka-requester-source-use-preset](../_includes/toloka-requester-source/id-toloka-requester-source/use-preset.md) %}

1. Follow [this link]({{ object-recognition-preset }}), or create a project manually:

    1. {% include [tutorials-create-project-button](../_includes/tutorials/create-project-button.md) %}

        {% include [tutorials-choose-preset-image](../_includes/tutorials/choose-preset-image.md) %}

    1. Select the {% if locale == "en-com" %}**Object recognition & detection**{% endif %} preset.

1. Click {% if locale == "en-com" %}**Choose solution**{% endif %} in the pop-up tab.

## Create a project {#project}

{% include [tutorials-who-are-tolokers](../_includes/tutorials/who-are-tolokers.md) %}

1. {% include [tutorials-add-name-description](../_includes/tutorials/add-name-description.md) %}

    - {% if locale == "en-com" %}**Name to show performers**{% endif %}: In 2–5 words, state the general idea of the project.

    - {% if locale == "en-com" %}**Description for performers**{% endif %}: In a couple of sentences, explain what you expect Tolokers to do. This is just an overview. You will write instructions later.

    <a target="_blank" href="https://yastatic.net/s3/doc-binary/src/support/toloka/en/guide/tutorials/selection/create-project-step-1.png"><img src="https://yastatic.net/s3/doc-binary/src/support/toloka/en/guide/tutorials/selection/create-project-step-1.png" alt="Create a project. Step 1" style="border:1px solid #ccc;border-radius:6px;cursor:zoom-in;width:700px;" /></a>

1. In the {% if locale == "en-com" %}**Task interface**{% endif %} section, set up what your tasks will look like. This preset has a task template with validation, keyboard shortcuts, and task layout pre-configured.

    {% include [toloka-requester-source-tb-or-html](../_includes/toloka-requester-source/id-toloka-requester-source/tb-or-html.md) %}

    1. Using the {% if locale == "en-com" %}**Visual editor**{% endif %}, set up your task in the {% if locale == "en-com" %}**Config**{% endif %} section:

        - {% if locale == "en-com" %}**Paste link to a sample image**{% endif %}: This image is only used to display the task interface preview on the right.

        - {% if locale == "en-com" %}**Choose the shape for outlining objects in photos**{% endif %}: All tasks in a project use the same shape.

        <a target="_blank" href="https://yastatic.net/s3/doc-binary/src/support/toloka/en/guide/tutorials/selection/selection-visual-editor.png"><img src="https://yastatic.net/s3/doc-binary/src/support/toloka/en/guide/tutorials/selection/selection-visual-editor.png" alt="Create a project. Visual editor" style="border-radius:6px;cursor:zoom-in;width:700px;" /></a>

    1. Select the {% if locale == "en-com" %}**I want to outline multiple types of objects**{% endif %} checkbox if you need to detect more than one category of objects in an image. Replace the samples with your types:

        - {% if locale == "en-com" %}**Object name for performers**{% endif %}: This is the label that Tolokers will see. Make sure it is clear and correct.

        - {% if locale == "en-com" %}**Name in labeling results**{% endif %}: This is the value you will see in the file with the labeling results.

    1. {% include [toloka-requester-source-specification-definition](../_includes/toloka-requester-source/id-toloka-requester-source/specification-definition.md) %}

        {% include [toloka-requester-source-click-show-specifications](../_includes/toloka-requester-source/id-toloka-requester-source/click-show-specifications.md) %}

        - {% if locale == "en-com" %}**Input data**{% endif %}: Parameters in the file with raw task data.

        - {% if locale == "en-com" %}**Output data**{% endif %}: Parameters in the file with labeling results.

        {% include [toloka-requester-source-specification-match](../_includes/toloka-requester-source/id-toloka-requester-source/specification-match.md) %}

1. {% include [toloka-requester-source-instructions](../_includes/toloka-requester-source/id-toloka-requester-source/instructions.md) %}

    In this type of project, Tolokers will select objects in images with the shape you’ve specified in the {% if locale == "en-com" %}**Config**{% endif %} section.

    <a target="_blank" href="https://yastatic.net/s3/doc-binary/src/support/toloka/en/guide/tutorials/selection/selection-instructions.png"><img src="https://yastatic.net/s3/doc-binary/src/support/toloka/en/guide/tutorials/selection/selection-instructions.png" alt="Create a project. Selection instructions" style="border:1px solid #ccc;border-radius:6px;cursor:zoom-in;width:700px;" /></a>

    {% include [toloka-requester-source-instruction-check](../_includes/toloka-requester-source/id-toloka-requester-source/instruction-check.md) %}

    {% include [toloka-requester-source-instruction-note](../_includes/toloka-requester-source/id-toloka-requester-source/instruction-note.md) %}

1. To save your data and continue, click {% if locale == "en-com" %}**Create a project**{% endif %}.

    {% include [tutorials-create-project-image](../_includes/tutorials/create-project-image.md) %}

## Create a pool {#pool}

{% include [toloka-requester-source-what-is-pool](../_includes/toloka-requester-source/id-toloka-requester-source/what-is-pool.md) %}

1. Click {% if locale == "en-com" %}**Create new pool**{% endif %}.

1. Under {% if locale == "en-com" %}**General information**{% endif %}, set the {% if locale == "en-com" %}**Pool name**{% endif %}.

1. {% include [toloka-requester-source-audience-settings](../_includes/toloka-requester-source/id-toloka-requester-source/audience-settings.md) %}

    1. Clear {% if locale == "en-com" %}**My tasks may contain shocking or pornographic content**{% endif %} if your project has none of those.

    1. {% include [toloka-requester-source-filters](../_includes/toloka-requester-source/id-toloka-requester-source/filters.md) %}

        For example, add the {% if locale == "en-com" %}**Languages**{% endif %} filter:

        <a target="_blank" href="https://yastatic.net/s3/doc-binary/src/support/toloka/en/guide/tutorials/selection/create-pool-step-3.2.png"><img src="https://yastatic.net/s3/doc-binary/src/support/toloka/en/guide/tutorials/selection/create-pool-step-3.2.png" alt="Create a pool. Step 3.2" style="border-radius:6px;cursor:zoom-in;width:700px;" /></a>

    1. Tasks in pools will automatically be available in the web version of Toloka and the mobile app. If you want to change the default settings and limit the visibility of the task for any of the versions, add the {% if locale == "en-com" %}**Client**{% endif %} filter and select the desired value: {% if locale == "en-com" %}**Toloka web version**{% endif %} or {% if locale == "en-com" %}**Toloka for mobile**{% endif %}.

    1. Use the {% if locale == "en-com" %}**Speed/quality balance**{% endif %} slider to change the number of Tolokers who can see your tasks. Move the slider to the right to exclude Tolokers with lower ratings from participating in your project.

        {% include [tutorials-speed-filter-image](../_includes/tutorials/speed-filter-image.md) %}

1. Under {% if locale == "en-com" %}**Quality control**{% endif %}, set quality control rules for more accurate results.

    1. Click the {% if locale == "en-com" %}**Non-automatic acceptance**{% endif %} toggle, and specify the number of days for checking the task in the {% if locale == "en-com" %}**Review period in days**{% endif %} field.

        {% cut "What is non-automatic acceptance (assignment review)?" %}

        The non-automatic acceptance option allows you to review completed assignments before accepting them and paying for them. If the Toloker didn't follow the instructions, you can reject the assignment.

        {% endcut %}

    1. Keep the pre-configured {% if locale == "en-com" %}**Fast responses**{% endif %} rule as is. This rule filters out Tolokers who complete tasks too fast. The default settings mean that Tolokers are banned from the project for 1 day if they complete tasks in 4 out of 5 task suites in less than 15 seconds.

    1. Delete the pre-configured {% if locale == "en-com" %}**Majority vote**{% endif %} rule.

    1. Click {% if locale == "en-com" %}**Add a quality control rule → Results of assignment review**{% endif %}, and enter the following values:

        <a target="_blank" href="https://yastatic.net/s3/doc-binary/src/support/toloka/en/guide/tutorials/selection/selection-results-rule.png"><img src="https://yastatic.net/s3/doc-binary/src/support/toloka/en/guide/tutorials/selection/selection-results-rule.png" alt="Create a pool. Selection results rule" style="border-radius:6px;cursor:zoom-in;width:700px;" /></a>

        This means that if 35% or more of a Toloker's responses are rejected, the Toloker is banned and can't access your tasks for 15 days. The rule takes effect after 3 responses of the Toloker are reviewed.

1. Click {% if locale == "en-com" %}**Show advanced settings**{% endif %}. In the {% if locale == "en-com" %}**Additional settings**{% endif %}, specify {% if locale == "en-com" %}**Time per task suite, sec**{% endif %}. It should be long enough to read the instructions and wait for task data to download (for example, 1,200 seconds).

1. {% include [toloka-requester-source-price-settings](../_includes/toloka-requester-source/id-toloka-requester-source/price-settings.md) %}

    1. In {% if locale == "en-com" %}**Price per task suite**{% endif %}, set the amount of money to pay per task suite done by one Toloker. A task suite is a page with a number of tasks. It can contain one or several tasks.

        If the tasks are simple, you can add 8–10 tasks per suite.

    1. {% include [toloka-requester-source-overlap-settings](../_includes/toloka-requester-source/id-toloka-requester-source/overlap-settings.md) %}

        For image area selection tasks, it is usually 1. This means that each task will have 1 response.

1. To save the settings and continue, click {% if locale == "en-com" %}**Create pool**{% endif %}.

## Upload data {#upload}

At this step, upload your task data to Toloka.

1. Click {% if locale == "en-com" %}**Upload data**{% endif %}.

1. Create the tasks for Tolokers:

    1. {% include [toloka-requester-source-download-template](../_includes/toloka-requester-source/id-toloka-requester-source/download-template.md) %}

        For this type of project, the file with tasks must have one parameter. Its name equals `INPUT:image`, and the values are links to the images.

        ```plaintext
        INPUT:image
        https://tlk.s3.yandex.net/sdc/photos/0c7b15d0f4e5db0416189afe6486f3cb.jpg
        https://tlk.s3.yandex.net/sdc/photos/3e5d32e31dfd50fe826fd46b761481cf.jpg
        https://tlk.s3.yandex.net/sdc/photos/0fb80721932aa59ecc684141433170b6.jpg
        ```

    1. Open the downloaded file, and replace the sample links with links to your images.

    1. Click {% if locale == "en-com" %}**Drop file here or select**{% endif %}, and upload the file you’ve just made.

    1. Click {% if locale == "en-com" %}**Continue**{% endif %}.

1. {% include [toloka-requester-source-task-suits](../_includes/toloka-requester-source/id-toloka-requester-source/task-suits.md) %}

    - {% if locale == "en-com" %}**General tasks**{% endif %}: These are tasks for Tolokers to label.

    - {% if locale == "en-com" %}**Control tasks**{% endif %}: These are tasks with predefined answers used to control the quality of responses. You don’t need control tasks in area selection projects.

    - {% if locale == "en-com" %}**Training tasks**{% endif %}: These are tasks with predefined answers and explanations for Tolokers. Normally you use training tasks in separate training pools. You don’t have to include them.

    For example, you can add 8 general tasks per suite:

    <a target="_blank" href="https://yastatic.net/s3/doc-binary/src/support/toloka/en/guide/tutorials/selection/selection-upload-data-step-3.png"><img src="https://yastatic.net/s3/doc-binary/src/support/toloka/en/guide/tutorials/selection/selection-upload-data-step-3.png" alt="Create a pool. Step 3" style="border:1px solid #ccc;border-radius:6px;cursor:zoom-in;width:636px;" /></a>

1. Click {% if locale == "en-com" %}**Combine tasks into suites**{% endif %}.

## Start labeling {#labeling}

1. Make sure you have [topped up your account](../concepts/refill.md).

1. {% include [toloka-requester-source-start-button](../_includes/toloka-requester-source/id-toloka-requester-source/start-button.md) %}

    <a target="_blank" href="https://yastatic.net/s3/doc-binary/src/support/toloka/en/guide/tutorials/selection/start-labeling-step-2.png"><img src="https://yastatic.net/s3/doc-binary/src/support/toloka/en/guide/tutorials/selection/start-labeling-step-2.png" alt="Start labeling. Step 2" style="border-radius:6px;cursor:zoom-in;width:700px;" /></a>

1. In the pop-up panel, review the budget and click {% if locale == "en-com" %}**Launch**{% endif %}.

## See the results {#results}

Track the labeling progress on the pool page. You can start the review when the first results are received.

After the specified time period, all responses are automatically accepted, regardless of their quality.

1. Go to the pool, and click {% if locale == "en-com" %}**Review assignments**{% endif %}.

    <a target="_blank" href="https://yastatic.net/s3/doc-binary/src/support/toloka/en/guide/tutorials/selection/selection-review-results.png"><img src="https://yastatic.net/s3/doc-binary/src/support/toloka/en/guide/tutorials/selection/selection-review-results.png" alt="See results. Step 1" style="border-radius:6px;cursor:zoom-in;width:700px;" /></a>

1. Choose an assignment.

1. Check the responses, and click {% if locale == "en-com" %}**Accept**{% endif %} or {% if locale == "en-com" %}**Decline**{% endif %}. For rejected responses, enter a comment to specify the reason.

    {% note info %}

    To learn about other ways of review, see the [Reviewing Tolokers' responses](../concepts/accept.md) section.

    {% endnote %}

1. After checking all the assignments, click {% if locale == "en-com" %}**Download results**{% endif %}.

    <a target="_blank" href="https://yastatic.net/s3/doc-binary/src/support/toloka/en/guide/tutorials/selection/selection-results-download.png"><img src="https://yastatic.net/s3/doc-binary/src/support/toloka/en/guide/tutorials/selection/selection-results-download.png" alt="See results. Step 4" style="border-radius:6px;cursor:zoom-in;width:700px;" /></a>

    You will get the TSV file with the labeling results. The point coordinates in the file are presented in JSON.

## See also {#seealso}

- [Instructions](https://toloka.ai/knowledgebase/instruction/)
- [Quality control](https://toloka.ai/knowledgebase/quality-control/)
- [Pricing](https://toloka.ai/knowledgebase/pricing/)
- [Template Builder — object recognition](../../template-builder/templates/object-recognition.md)
- [Toloka-Kit — object recognition](https://github.com/Toloka/toloka-kit/blob/main/examples/1.computer_vision/object_detection/object_detection.ipynb)

## Datasets and reference {#datasets}

- [Sample dataset file with tasks](https://tlk.s3.yandex.net/toloka-kit/knowledge-base/road_signs.tsv)