[![Build Status](https://travis-ci.com/shikimori/shiki-uploader.svg?branch=master)](https://travis-ci.com/shikimori/shiki-uploader)

# shiki-uploader
Used to upload files to shikimori.


### Usage
```javascript
import ShikiUploader from 'shiki-uploader';

/*
  defaultOptions = {
    node: null,
    progressContainerNode: null,
    locale: null,
    xhrEndpoint: null,
    xhrHeaders: () => ({}),
    xhrFieldName: 'image',
    maxNumberOfFiles: 150,
    isResetAfterUpload: true
  }

  events:
    upload
    file-added
    upload-success
    upload-progress
    upload-error
    complete
    restriction-failed
*/
new ShikiUploader({ node: domNodeItWillBeAttachedTo, ...options })
  .on('upload:file:success', (_e, { response }) => (
    console.log(response.html);
  ));
```
