# Audio transcription

In this tutorial, you will learn how to run audio transcription in Toloka. We will use a project preset designed specifically for this type of data labeling.

Audio transcription is a type of data labeling task with an audio file and a text input area. Tolokers listen to the short recording and type the text they hear. After you collect the results, you can apply the dataset for your speech recognition models.

{% note info %}

You may need additional projects for your task, such as dataset pre-check or checking Tolokers' responses. Learn more about this in [Decomposition of the task](../concepts/solution-architecture.md).

{% endnote %}

## Prerequisites {#prerequisites}

Before you begin:

- {% include [tutorials-register](../_includes/tutorials/register.md) %}

- {% include [tutorials-top-up-tutorial](../_includes/tutorials/top-up-tutorial.md) %}

## Choose a preset {#preset}

{% include [toloka-requester-source-use-preset](../_includes/toloka-requester-source/id-toloka-requester-source/use-preset.md) %}

1. Follow [this link]({{ audio-transcription-preset }}), or create a project manually:

    1. {% include [tutorials-create-project-button](../_includes/tutorials/create-project-button.md) %}

        {% include [tutorials-choose-preset-image](../_includes/tutorials/choose-preset-image.md) %}

    1. Select the {% if locale == "en-com" %}**Transcribing audio recordings**{% endif %} preset.

1. Click {% if locale == "en-com" %}**Choose this preset**{% endif %} in the pop-up tab.

## Create a project {#project}

{% include [tutorials-who-are-tolokers](../_includes/tutorials/who-are-tolokers.md) %}

1. {% include [tutorials-add-name-description](../_includes/tutorials/add-name-description.md) %}

    - {% if locale == "en-com" %}**Name to show Tolokers**{% endif %}: In 2–5 words, state the general idea of the project.

    - {% if locale == "en-com" %}**Description for Tolokers**{% endif %}: In a couple of sentences, explain what you expect Tolokers to do. This is just an overview. You will write instructions later.

    [![Create a project. Step 1](https://yastatic.net/s3/doc-binary/src/support/toloka/en/guide/tutorials/transcript-audio/transcript-audio-create-project-step-1.png =700x)](https://yastatic.net/s3/doc-binary/src/support/toloka/en/guide/tutorials/transcript-audio/transcript-audio-create-project-step-1.png)

1. In the {% if locale == "en-com" %}**Task interface**{% endif %} section, set up what your tasks will look like. This preset has a task template with layout and validation pre-configured. The Toloker won't be able to submit the response without listening to the audio recording and adding the text.

    {% include [toloka-requester-source-tb-or-html](../_includes/toloka-requester-source/id-toloka-requester-source/tb-or-html.md) %}

    1. In the {% if locale == "en-com" %}**Config**{% endif %} section, you can change the texts Tolokers will see in your task. All tasks in a project use the same texts.

        [![Create a project. Config texts](https://yastatic.net/s3/doc-binary/src/support/toloka/en/guide/tutorials/transcript-audio/transcript-audio-config-texts.png =700x)](https://yastatic.net/s3/doc-binary/src/support/toloka/en/guide/tutorials/transcript-audio/transcript-audio-config-texts.png)

        {% note info %}

        To learn about other properties of the {% if locale == "en-com" %}**Config**{% endif %} section, their possible values and the impact on the task interface, see the [Template Builder Help](../../template-builder/templates/audio-transcript.md).

        {% endnote %}

    1. In the {% if locale == "en-com" %}**Input data example**{% endif %} section, add a link to a sample audio. This audio is only used to display the task interface preview on the right.

        [![Create a project. Input data example](https://yastatic.net/s3/doc-binary/src/support/toloka/en/guide/tutorials/transcript-audio/transcript-audio-input-example.png =700x)](https://yastatic.net/s3/doc-binary/src/support/toloka/en/guide/tutorials/transcript-audio/transcript-audio-input-example.png)

    1. {% include [toloka-requester-source-specification-definition](../_includes/toloka-requester-source/id-toloka-requester-source/specification-definition.md) %}

        {% include [toloka-requester-source-click-show-specifications](../_includes/toloka-requester-source/id-toloka-requester-source/click-show-specifications.md) %}

        - {% if locale == "en-com" %}**Input data**{% endif %}: Parameters in the file with raw task data.

        - {% if locale == "en-com" %}**Output data**{% endif %}: Parameters in the file with labeling results.

        {% include [toloka-requester-source-specification-match](../_includes/toloka-requester-source/id-toloka-requester-source/specification-match.md) %}

1. {% include [toloka-requester-source-instructions](../_includes/toloka-requester-source/id-toloka-requester-source/instructions.md) %}

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

        - For example, add the {% if locale == "en-com" %}**Languages**{% endif %} filter:

            [![Create a pool. Language filter](https://yastatic.net/s3/doc-binary/src/support/toloka/en/guide/tutorials/transcript-audio/transcript-audio-language-filter.png =700x)](https://yastatic.net/s3/doc-binary/src/support/toloka/en/guide/tutorials/transcript-audio/transcript-audio-language-filter.png)

        - It is best to launch transcription tasks in the Toloka web version so that Tolokers can use the keyboard for typing. Add the {% if locale == "en-com" %}**Device type**{% endif %} filter, and set its value to {% if locale == "en-com" %}**Personal computer**{% endif %}.

    1. Use the {% if locale == "en-com" %}**Speed/quality balance**{% endif %} slider to change the number of Tolokers who can see your tasks. Move the slider to the right to exclude Tolokers with lower ratings from participating in your project.

        {% include [tutorials-speed-filter-image](../_includes/tutorials/speed-filter-image.md) %}

1. In {% if locale == "en-com" %}**Quality control**{% endif %}, set quality control rules for more accurate results.

    1. Click the {% if locale == "en-com" %}**Non-automatic acceptance**{% endif %} toggle, and specify the number of days for checking the task in the {% if locale == "en-com" %}**Review period in days**{% endif %} field.

        {% include [tutorials-na-acceptance](../_includes/tutorials/na-acceptance.md) %}

    1. Delete the pre-configured {% if locale == "en-com" %}**Majority vote**{% endif %} rule.

    1. Edit the pre-configured {% if locale == "en-com" %}**Fast responses**{% endif %} rule to catch bots. This rule filters out Tolokers who complete tasks too fast.

        Set the {% if locale == "en-com" %}**Minimum time per task suite**{% endif %}. A task suite is a page with a number of tasks. It can contain one or several tasks. If the tasks are simple, you can add 6–10 tasks per suite.

        - The minimum time per suite value depends on two characteristics: the number of tasks on the page, and the length of audio recordings.

        - Make allowances for technical errors. For example, some recordings failed to load or play. The Toloker will quickly submit responses for tasks like this and this won't be an error.

        To catch bots, set 10–15 seconds per response. Ban Tolokers after two fast responses.

        [![Create a pool. Fast answers filter](https://yastatic.net/s3/doc-binary/src/support/toloka/en/guide/tutorials/transcript-audio/transcript-audio-fast-answers.png =700x)](https://yastatic.net/s3/doc-binary/src/support/toloka/en/guide/tutorials/transcript-audio/transcript-audio-fast-answers.png)

        This means that a user who completes two or more task suites in less than 10 seconds will be banned for 10 days and won't be able to access your tasks.

    1. For a trial pool, the settings you’ve just made are enough. You can get better results if you set the additional quality control rules.

        {% cut "The additional quality control rules" %}

        1. Click {% if locale == "en-com" %}**Add a quality control rule**{% endif %}, and add the second {% if locale == "en-com" %}**Fast responses**{% endif %} rule. It will help detect Tolokers who retype texts carelessly, make mistakes, skip words, or don't take the task seriously enough.

            In this case, the {% if locale == "en-com" %}**Minimum time per task suite**{% endif %} value depends on the length of recordings and their number per task suite, as well as on how difficult the task is (it's hard to hear, it contains jargon, it has special rules for transcribing, and so on). Ban Tolokers after three fast responses.

            [![Create a pool. Fast answers control rule](https://yastatic.net/s3/doc-binary/src/support/toloka/en/guide/tutorials/transcript-audio/transcript-audio-fast-answers2.png =700x)](https://yastatic.net/s3/doc-binary/src/support/toloka/en/guide/tutorials/transcript-audio/transcript-audio-fast-answers2.png)

            This means that a user who gives a minimum of 3 responses in less than 30 seconds will be banned for 5 days and won't be able to complete your tasks.

        1. Add the {% if locale == "en-com" %}**Results of assignment review**{% endif %} quality control rule and enter the following values:

            [![Create a pool. Assignments review control rule](https://yastatic.net/s3/doc-binary/src/support/toloka/en/guide/tutorials/transcript-audio/transcript-audio-offline-accept.png =700x)](https://yastatic.net/s3/doc-binary/src/support/toloka/en/guide/tutorials/transcript-audio/transcript-audio-offline-accept.png)

            This means that if 35% or more of a Toloker's responses are rejected, the Toloker is banned and can't access your tasks for 15 days. The rule takes effect after 3 responses of the Toloker are reviewed.

        1. Add the [Processing rejected and accepted assignments](../concepts/reassessment-after-accepting.md) rule:

            [![Create a pool. Processing rejected and accepted assignments control rule](https://yastatic.net/s3/doc-binary/src/support/toloka/en/guide/tutorials/transcript-audio/qcr-reassessment-after-accepting_example1.png =700x)](https://yastatic.net/s3/doc-binary/src/support/toloka/en/guide/tutorials/transcript-audio/qcr-reassessment-after-accepting_example1.png)

            This means that if you reject assignments during the review, they'll be sent for re-completion, but to another Toloker.

        {% endcut %}

1. {% include [toloka-requester-source-price-settings](../_includes/toloka-requester-source/id-toloka-requester-source/price-settings.md) %}

    1. In {% if locale == "en-com" %}**Price per task suite**{% endif %}, set the amount of money to pay per task suite done by one Toloker.

        The price depends on the length and complexity of the audio recordings.

    1. {% include [toloka-requester-source-overlap-settings](../_includes/toloka-requester-source/id-toloka-requester-source/overlap-settings.md) %}

        For the speech transcription, overlap is 1, as a rule. This means that each task will have 1 response.

1. Click {% if locale == "en-com" %}**Show advanced settings**{% endif %}. In {% if locale == "en-com" %}**Additional settings**{% endif %}, specify the {% if locale == "en-com" %}**Time per task suite, sec**{% endif %}.

    This time should be enough to read the instructions, load the task, listen to audio recordings, and type text (for example, 1,200 seconds).

1. To save the settings and continue, click {% if locale == "en-com" %}**Create pool**{% endif %}.

## Upload data {#upload}

At this step, upload your task data to Toloka. We recommend that all the recordings in a pool are about the same length.

1. Click {% if locale == "en-com" %}**Upload data**{% endif %}.

1. Attach a prepared dataset or media files.

    {% list tabs %}

    - A prepared dataset

        1. {% include [toloka-requester-source-download-template](../_includes/toloka-requester-source/id-toloka-requester-source/download-template.md) %}

            For this type of project, the file with tasks must have one parameter. Its name equals `INPUT:audio`, and the values are links to the audio files.

            ```plaintext
            INPUT:audio
            https://tlk.s3.yandex.net/ext_dataset/noisy_speech/noisy_tested_wav/p257_068.wav
            https://tlk.s3.yandex.net/ext_dataset/noisy_speech/noisy_tested_wav/p257_095.wav
            https://tlk.s3.yandex.net/ext_dataset/noisy_speech/noisy_tested_wav/p257_293.wav
            ```

        1. Open the downloaded file, and replace the sample links with links to your audio files.

        1. Click {% if locale == "en-com" %}**Select prepared dataset**{% endif %}, and upload the file you’ve just made.

    - Media files

        {% include [media-files](../_includes/toloka-requester-source/id-toloka-requester-source/media-files.md) %}

    {% endlist %}

1. Click {% if locale == "en-com" %}**Continue**{% endif %}.

1. {% include [toloka-requester-source-task-suits](../_includes/toloka-requester-source/id-toloka-requester-source/task-suits.md) %}

    - {% if locale == "en-com" %}**General tasks**{% endif %}: These are tasks for Tolokers to label.

    - {% if locale == "en-com" %}**Control tasks**{% endif %}: These are tasks with predefined answers used to control the quality of responses. For this project, you don’t need control tasks because of the enabled {% if locale == "en-com" %}**Non-automatic acceptance**{% endif %} option.

    - {% if locale == "en-com" %}**Training tasks**{% endif %}: These are tasks with predefined answers and explanations for Tolokers. Normally you use training tasks in separate training pools. You don’t have to include them.

    For example, you can add 5 general tasks per suite:

    [![Upload data. Tasks per suite](https://yastatic.net/s3/doc-binary/src/support/toloka/en/guide/tutorials/transcript-audio/transcript-audio-upload-data.png =700x)](https://yastatic.net/s3/doc-binary/src/support/toloka/en/guide/tutorials/transcript-audio/transcript-audio-upload-data.png)

    This means that there will be 5 audio recordings per suit, each recording with a text field for transcription.

1. Click {% if locale == "en-com" %}**Combine tasks into suites**{% endif %}.

## Start labeling {#labeling}

1. Make sure you have [topped up your account](../concepts/refill.md).

1. {% include [toloka-requester-source-start-button](../_includes/toloka-requester-source/id-toloka-requester-source/start-button.md) %}

    [![Start labeling. Step 2](https://yastatic.net/s3/doc-binary/src/support/toloka/en/guide/tutorials/transcript-audio/transcript-audio-start-labeling-step-2.png =700x)](https://yastatic.net/s3/doc-binary/src/support/toloka/en/guide/tutorials/transcript-audio/transcript-audio-start-labeling-step-2.png)

1. In the pop-up panel, review the budget and click {% if locale == "en-com" %}**Launch**{% endif %}.

## See the results {#results}

Track the labeling progress on the pool page. You can start the review when the first results are received.

After the specified time period, all responses are automatically accepted, regardless of their quality.

1. Go to the pool, and click {% if locale == "en-com" %}**Review assignments**{% endif %}.

    [![See the results. Review assignments](https://yastatic.net/s3/doc-binary/src/support/toloka/en/guide/tutorials/transcript-audio/transcript-audio-review-results.png =700x)](https://yastatic.net/s3/doc-binary/src/support/toloka/en/guide/tutorials/transcript-audio/transcript-audio-review-results.png)

1. Choose an assignment.

1. Check the responses, and click {% if locale == "en-com" %}**Accept**{% endif %} or {% if locale == "en-com" %}**Decline**{% endif %}. For rejected responses, enter a comment to specify the reason.

    {% note info %}

    To learn about other ways of review, see the [Reviewing Tolokers' responses](../concepts/accept.md) section.

    {% endnote %}

1. After checking all the assignments, click {% if locale == "en-com" %}**Download results**{% endif %}.

    [![See the results. Download results](https://yastatic.net/s3/doc-binary/src/support/toloka/en/guide/tutorials/transcript-audio/transcript-audio-results-download.png =700x)](https://yastatic.net/s3/doc-binary/src/support/toloka/en/guide/tutorials/transcript-audio/transcript-audio-results-download.png)

    You will get the TSV file with the labeling results.

## See also {#see-also}

- [Crowdsourcing concepts: Instructions](https://toloka.ai/knowledgebase/instruction/)
- [Crowdsourcing concepts: Quality control](https://toloka.ai/knowledgebase/quality-control/)
- [Crowdsourcing concepts: Pricing](https://toloka.ai/knowledgebase/pricing/)
- [Template Builder: Audio transcription](../../template-builder/templates/audio-transcript.md)

## For developers {#for-developers}

- [Toloka-Kit: Audio transcription](https://github.com/Toloka/toloka-kit/blob/main/examples/3.audio_analysis/audio_transcription/audio_transcription.ipynb)

## Datasets and reference {#datasets}

Sample dataset files with tasks

- [File 1](https://tlk.s3.yandex.net/knowledge-base/noisyspeech_wogoldens.tsv)
- [File 2](https://tlk.s3.yandex.net/knowledge-base/noisyspeech_wgoldens.tsv)
- [File 3](https://tlk.s3.yandex.net/knowledge-base/noisy_speech_exam.tsv)

{% include [contact-support](../_includes/contact-support.md) %}

{% include [image-styles](../../../_includes/image-styles.md) %}