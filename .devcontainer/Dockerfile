# See here for image contents: https://github.com/microsoft/vscode-dev-containers/tree/v0.177.0/containers/go/.devcontainer/base.Dockerfile

ARG VARIANT="1.16"
FROM mcr.microsoft.com/vscode/devcontainers/go:0-${VARIANT}

RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
	&& curl -fsSL https://apt.releases.hashicorp.com/gpg | sudo apt-key add - \
	&& apt-get -y install software-properties-common \
	&& sudo apt-add-repository "deb [arch=amd64] https://apt.releases.hashicorp.com buster main" \
	&& apt-get update \
	&& sudo apt -y install terraform

# [Optional] Uncomment this section to install additional OS packages.
#     && apt-get -y install --no-install-recommends <your-package-list-here>

# [Optional] Uncomment the next line to use go get to install anything else you need
# RUN go get -x <your-dependency-or-tool>
