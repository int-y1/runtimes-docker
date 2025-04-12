FROM dmoj/runtimes-tier1

RUN apt-get update && \
    apt-get install -y --no-install-recommends \
        jq apt-transport-https dirmngr gnupg ca-certificates xz-utils \
        $([ "$(arch)" = x86_64 ] && echo libc6-dev-i386) \
        golang-go racket && \
    apt-get clean && rm -rf /var/lib/apt/lists/*

RUN go version

ENV PATH="/opt/dlang/linux/bin64:/home/judge/.cargo/bin:/opt/pypy2/bin:/opt/pypy3/bin:/opt/dart-sdk/bin:${PATH}"
