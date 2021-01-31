

An Alpine-based Docker image for working with both curl and jq.

Usage
Both of the following docker run variations will succeed.

Using jq as the Docker entrypoint
docker run \
  --rm \
  -v $(pwd):/home \
  Dp/node-curl-jq '.[]' /home/test.json
Providing a command to the container
docker run \
  --rm \
  -v $(pwd):/home \
  Dp/node-curl-jq \
  /bin/sh -c "cat /home/test.json | jq '.[]'"
