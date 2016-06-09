FROM java:8-jdk

ADD scan.cli-macosx-3.0.0.zip /opt &&\
    unzip -q scan.cli-macosx-3.0.0.zip && \
    rm scan.cli-macosx-3.0.0.zip && \

# Export the dependencies directories as a volume
RUN mkdir -p /root/.gradle
VOLUME [ "/root/.gradle" ]

# Create working directory
RUN mkdir -p /code
VOLUME [ "/code" ]
WORKDIR /code

ENTRYPOINT [ "./gradlew" ]
