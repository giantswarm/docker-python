# Small python docker image

Based on alpine.

See https://github.com/gliderlabs/docker-alpine

## Usage

Just derive from the image in `FROM` and the current directory will be added as `/app` in the image and pip packages will be installed.

Example:

```
FROM giantswarm/python

RUN python setup.py install

ENTRYPOINT ["python", "-m", "foobar"]
```
