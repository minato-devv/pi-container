Base image: node:24-bookworm-slim
`fd-find` is installed and symlinked to `/usr/bin/fd`

container build -t pi-coding-agent:local .
container v create pi-agent-home
container run -it  --rm -v "$PWD:/workspace" -v "pi-agent-home:/root/.pi/agent" pi-coding-agent:local
