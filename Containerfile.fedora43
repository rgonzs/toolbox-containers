FROM registry.fedoraproject.org/fedora-toolbox:43
ARG KUBE_VERSION="1.34"

RUN dnf install -y neovim zsh kubernetes${KUBE_VERSION}-client ansible sshpass \
    && dnf clean all \
    && rm -rf /var/cache/yum

# add neovim as vim alternative
RUN update-alternatives --install /usr/bin/vim vim /usr/bin/nvim 0
