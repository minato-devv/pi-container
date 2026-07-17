Base image: node:24-bookworm-slim

`fd-find` is installed and symlinked to `/usr/bin/fd`

```bash
container build -t pi-coding-agent:local .

cp models-example.json pi-agent/models.json

PICONFIG=<config directory> container run -it  --rm -v "$PWD:/home/node/workspace" -v "$PICONFIG:/home/node/.pi/agent" pi-coding-agent:local
```
