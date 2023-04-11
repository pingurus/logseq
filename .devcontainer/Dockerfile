FROM openjdk:11

RUN curl -sL https://deb.nodesource.com/setup_16.x | bash - && \
    apt-get install -y nodejs

RUN apt-get update && apt-get install ca-certificates && \
    wget --no-check-certificate -qO - https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add - && \
    echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list && \
    apt-get update && \
    apt-get install -y yarn

RUN curl -sL https://download.clojure.org/install/linux-install-1.10.1.727.sh | bash

RUN apt-get install --no-install-recommends zip

RUN apt-get install --no-install-recommends -y libgtk-3-dev libxshmfence-dev libnss3 libdrm-dev libasound2-dev

RUN apt-get install build-essential