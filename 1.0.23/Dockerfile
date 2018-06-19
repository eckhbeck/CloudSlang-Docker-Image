FROM java:openjdk-8-jre

MAINTAINER CloudSlang

RUN groupadd -r cslang && useradd -r -g cslang cslang

RUN mkdir -p /usr/cslang \
  && cd /usr/cslang \
  && wget "https://github.com/CloudSlang/cloud-slang/releases/download/cloudslang-1.0.23/cslang-cli-with-content.tar.gz" \
  && tar xvf cslang-cli-with-content.tar.gz \
  && rm cslang-cli-with-content.tar.gz

WORKDIR /usr/cslang/cslang-cli/bin/

ENTRYPOINT ["sh","cslang"]
