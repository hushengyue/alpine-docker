FROM swineherd/pyinstaller:3.6.5-3.6

LABEL maintainer="Daniel <daniel.hu@cloudwise.com>"

COPY requirements.txt /requirements.txt
RUN apt-get install libsnappy-dev -y && \
    pip install --no-cache-dir -r /requirements.txt

