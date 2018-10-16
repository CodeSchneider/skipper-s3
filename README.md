# Sails S3 Adapter


## Installation

```
$ npm install skipper-s3-alt --save
```


## Usage

```javascript
req.file('avatar')
.upload({
  // Required
  adapter: require('skipper-s3-alt'),
  key: 'thekyehthethaeiaghadkthtekey',
  secret: 'AB2g1939eaGAdesoccertournament',
  bucket: 'my_stuff',
  // Optional
  token: 'temporary_sts_creds'
}, function whenDone(err, uploadedFiles) {
  if (err) {
    return res.serverError(err);
  }
  return res.ok({
    files: uploadedFiles,
    textParams: req.params.all()
  });
});
```


```
