sentry-s3-nodestorage
=====================

[Sentry](https://github.com/getsentry/sentry) extension implementing the
NodeStorage interface for [Amazon Simple Storage Service](https://aws.amazon.com/s3/) and S3-compatible object storages
such as
[Minio](https://mi.io).

# Installation

```bash
$ pip install sentry-s3-nodestore
```

# Sentry Configuration

```python
SENTRY_NODESTORE = 'sentry_s3_nodestore.backend.S3NodeStorage'
SENTRY_NODESTORE_OPTIONS = {
    'bucket_name': 'my-sentry-bucket',
    'url': 'http://my-minio.local:9000',
    'aws_access_key_id': 'ABCD...',
    'aws_secret_access_key': 'EFG....'
}
```

# Note

The bucket should already exist and be accessible by access key, this extension won't create the bucket.

# Credits

- Original author [Ernest W. Durbin III](https://github.com/ewdurbin)
- Upgrade to Boto3 by [Letnab](https://github.com/letnab)