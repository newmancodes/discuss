FROM mcr.microsoft.com/devcontainers/javascript-node:1-22-bookworm

RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install --no-install-recommends elixir erlang erlang-dev erlang-xmerl erlang-dialyzer inotify-tools

USER node

RUN mix local.hex --force
RUN mix local.rebar --force
RUN mix archive.install hex phx_new --force

# [Optional] Uncomment if you want to install an additional version of node using nvm
# ARG EXTRA_NODE_VERSION=10
# RUN su node -c "source /usr/local/share/nvm/nvm.sh && nvm install ${EXTRA_NODE_VERSION}"

# [Optional] Uncomment if you want to install more global node modules
# RUN su node -c "npm install -g <your-package-list-here>"
