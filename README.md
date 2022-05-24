# CircleCI Docker Images

These images are based on [CircleCI images](https://hub.docker.com/r/circleci/node/), with added AWS CLI

## Node 14x [`latest` `n14`]

The `n14` tag includes:

- node 14x
- npm 8.10.0
- awscli 2

## Node 12x [`n12`]

The `n12` tag includes:

- node 12x
- npm 8.10
- awscli 2

## Development

### Build Image

```sh
docker build -t nigelng/cci-node-awscli:<tagname> .
```

### Run Image

```sh
docker run -it nigelng/cci-node-awscli:<tagname> bash
```

### Push to DockerHub

```sh
# Push all new tags
docker push --all-tags nigelng/cci-node-awscli

# Push particular tag
docker push --all-tags nigelng/cci-node-awscli:<tagname>
```

## CCI Usage

```yaml
docker:
  - image: nigelng/cci-node-awscli:n14
```
