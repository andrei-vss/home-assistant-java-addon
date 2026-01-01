ARG BUILD_FROM
FROM $BUILD_FROM

RUN apk add --no-cache openjdk17-jre openjdk17

ENV JAVA_HOME=/usr/lib/jvm/java-17-openjdk
ENV PATH="$JAVA_HOME/bin:$PATH"

ARG TEMPIO_VERSION BUILD_ARCH
RUN curl -sSLf -o /usr/bin/tempio \
    "https://github.com/home-assistant/tempio/releases/download/${TEMPIO_VERSION}/tempio_${BUILD_ARCH}"

COPY rootfs /
COPY app.jar /opt/app/app.jar

RUN chmod +x /etc/services.d/java-run/run /etc/services.d/java-run/finish