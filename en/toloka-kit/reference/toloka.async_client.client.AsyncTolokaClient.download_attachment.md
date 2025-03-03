# download_attachment
`toloka.async_client.client.AsyncTolokaClient.download_attachment` | [Source code](https://github.com/Toloka/toloka-kit/blob/v1.1.0.post1/src/async_client/client.py#L0)

```python
async download_attachment(
    self,
    attachment_id: str,
    out: BinaryIO
)
```

Downloads specific attachment

## Parameters Description

| Parameters | Type | Description |
| :----------| :----| :-----------|
`attachment_id`|**str**|<p>ID of attachment.</p>
`out`|**BinaryIO**|<p>File object where to put downloaded file.</p>

**Examples:**

How to download an attachment.

```python
with open('my_new_file.txt', 'wb') as out_f:
    toloka_client.download_attachment(attachment_id='1', out=out_f)
```
