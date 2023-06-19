# Set up Docker in a Multipass VM

## Set up multipass

> Note: Disable VPN

### 1. [Multipass tutorial for MacOS (M1 Pro)](https://multipass.run/docs/mac-tutorial)

### 2. Install multipass

```bash 
# install multipass CLI and multipassd daemon
brew install --cask multipass
```

### 3. [Multipass Blueprints (Definitions)]( https://github.com/canonical/multipass-blueprints)

Some environments require a lot of configuration and setup. Multipass Blueprints are instances with a deep level of customization.

```bash
# find the images and blueprints
multipass find

# launch a ubuntu focal instance with custom configurations
multipass launch lts --name learn-docker --cpus 4 --disk 50G --memory 8G

# multipassd daemon logs on macOS
tail -f /Library/Logs/Multipass/multipassd.log

# List available instances
multipass list

# SSH to the instance
multipass shell learn-docker

# Delete a Multipass Instance
multipass delete learn-docker
multipass purge

# Uninstall Multipass
brew uninstall multipass
OR
brew uninstall --zap multipass # to destroy all data
```

## Set up latest stable Docker Engine

### 1. [Install Docker Engine on Ubuntu](https://docs.docker.com/engine/install/ubuntu/)