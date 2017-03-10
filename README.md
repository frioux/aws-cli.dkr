# AWS Container

## Usage

```
mkdir ~/.aws

docker run -it --rm     \
  --volume ~/.aws:/.aws \
  --user $(id -u)       \
  frew/aws              \
  configure

docker run -it --rm     \
  --volume ~/.aws:/.aws \
  --user $(id -u)       \
  frew/aws              \
  ec2 describe-instances
```

## Description

The packaged versions of [aws-cli](https://github.com/aws/aws-cli) tend to be a
little out of date.  This image contains everything you need to use `aws-cli`
without installing python modules system-wide.

## Volumes

There is only a single volume, used for configuration: `/.aws/`.  It is
absolutely required and almost any usage without it is likely to fail.

## Whalebrew

Full whalebrew support!

