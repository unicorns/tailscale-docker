# Tailscale in Docker

## Getting Started

```bash
# First build the tailscale container:
(source .env; docker build -t tailscale:${TAILSCALE_TAG} "${TAILSCALE_PATH}")
# Start services
docker-compose up
# Start tailscale service
docker-compose run tailscale tailscale up
# Now the tailscale service is accessible in the tailscale container and the dev container
docker-compose run dev ping <another_host_on_tailscale>
```

## Configuration

Configuration for which tailscale version to use, etc. are stored in `.env` and can be overwritten using environment variables.

## Credits

This repo is derived from the discussion [here](https://github.com/tailscale/tailscale/issues/504).

