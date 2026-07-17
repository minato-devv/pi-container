Base image: node:24-bookworm-slim

container build -t pi-coding-agent:local .
container run -it  --rm -v "$PWD:/workspace" -v "pi-agent-home:/root/.pi/agent" pi-coding-agent:local
