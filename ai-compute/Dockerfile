FROM swineherd/pyinstaller:3.6.5-3.6

LABEL maintainer="Daniel <daniel.hu@cloudwise.com>"

COPY requirements.txt /requirements.txt
COPY pandahouse /pandahouse

RUN apt-get install libsnappy-dev -y && \
    pip install --no-cache-dir -r /requirements.txt && \
    rm -rf /root/.pyenv/versions/3.6.5/lib/python3.6/site-packages/pandahouse && \
    mv /pandahouse /root/.pyenv/versions/3.6.5/lib/python3.6/site-packages/

