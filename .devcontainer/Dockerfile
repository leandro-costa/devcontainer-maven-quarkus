FROM maven:3.9.4-eclipse-temurin-20
RUN apt-get update && \ 
    apt-get install -y zip unzip git xvfb libx11-6 libx11-xcb1 libxext6 libxrender1 libxtst6 libxi6 libfreetype6 libgtk-3-0 && \
    # Clean the packages and install script in /var/cache/apt/archives/
    apt-get clean && \
    # Remove the package lists (created by apt-get update)
    rm -rf /var/lib/apt/lists/*

RUN curl -s "https://get.sdkman.io" | bash
RUN bash -c "source $HOME/.sdkman/bin/sdkman-init.sh && sdk install quarkus"
