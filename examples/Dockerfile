FROM intelsdi/snap:alpine_test

ENV CI_URL='https://s3-us-west-2.amazonaws.com/snap.ci.snap-telemetry.io
ENV PLUGIN_PUB_FILE_VER='latest'
ENV TASK='psutil-file.json'

ADD  ${CI_URL}/plugins/snap-plugin-publisher-file/${PLUGIN_PUB_FILE_VER}/linux/x86_64/snap-plugin-publisher-file /opt/snap/plugin/snap-plugin-publisher-file

COPY build/linux/x86_64/snap-plugin-collector-psutil /opt/snap/plugin/snap-plugin-collector-psutil
COPY examples/tasks/${TASK} /opt/snap/plugin/${TASK}
