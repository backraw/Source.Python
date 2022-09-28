FROM ubuntu:bionic-20220902

RUN apt-get update && \
    DEBIAN_FRONTEND=noninteractive apt-get install --no-install-recommends -y \
        cmake \
        make \
        gcc-4.8 \
        g++-4.8 \
        gcc-4.8-multilib \
        g++-4.8-multilib \
        git \
        ca-certificates \
    && \
        apt-get clean && \
        rm -rf /var/cache/apt/lists/* \
    && \
        update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-4.8 1 && \
        update-alternatives --install /usr/bin/g++ g++ /usr/bin/g++-4.8 1 \
    && \
        ln -sf /usr/include/asm-generic /usr/include/asm \
    && \
        git config --global --add safe.directory /tmp/source-python
