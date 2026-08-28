FROM mcr.microsoft.com/devcontainers/base:ubuntu

ARG SBT_VERSION=1.10.11

RUN apt-get update \
    && apt-get install -y --no-install-recommends curl openjdk-17-jdk \
    && curl -fsSL "https://github.com/sbt/sbt/releases/download/v${SBT_VERSION}/sbt-${SBT_VERSION}.tgz" \
        | tar -xz -C /opt \
    && ln -s /opt/sbt/bin/sbt /usr/local/bin/sbt \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*