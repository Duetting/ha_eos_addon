# https://developers.home-assistant.io/docs/add-ons/configuration#add-on-dockerfile
ARG BUILD_FROM
FROM $BUILD_FROM

# Execute during the build of the image
ARG TEMPIO_VERSION BUILD_ARCH
RUN \
    curl -sSLf -o /usr/bin/tempio \
    "https://github.com/home-assistant/tempio/releases/download/${TEMPIO_VERSION}/tempio_${BUILD_ARCH}"

# Copy root filesystem
COPY rootfs /

RUN apt-get update
RUN apt-get install -y python3 python3-pip python3-venv git

ENV VIRTUAL_ENV="/opt/venv"
RUN python3 -m venv ${VIRTUAL_ENV}
ENV PATH="${VIRTUAL_ENV}/bin:${PATH}"

ENV EOS_DIR="/opt/eos"

RUN adduser --system --no-create-home eos \
    && mkdir -p "${EOS_DIR}" \
    && chown eos "${EOS_DIR}"

RUN git clone https://github.com/Akkudoktor-EOS/EOS.git ${EOS_DIR}

WORKDIR ${EOS_DIR}

RUN pip install -Ur requirements.txt

RUN pip install -e .

# use s6-overlay as init system
WORKDIR /
ENTRYPOINT ["/init"]