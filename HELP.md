# Sample using JReleaser with Spring Shell

export JRELEASER_GITHUB_TOKEN=<PAT>


jreleaser assemble

jreleaser package

## Prepare Ubuntu 18.04

docker run --name jr-ubuntu-1804 -d -t ubuntu:18.04
docker exec -it jr-ubuntu-1804 bash

apt update
apt install -y git
apt install -y curl
apt install -y gcc

## Install brew

/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

(echo; echo 'eval "$(/home/linuxbrew/.linuxbrew/bin/brew shellenv)"') >> /root/.profile
eval "$(/home/linuxbrew/.linuxbrew/bin/brew shellenv)"

brew tap jvalkeal/atestj-tap
