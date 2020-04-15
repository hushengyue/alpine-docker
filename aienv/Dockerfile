FROM swineherd/pyinstaller:3.6.5-3.6

LABEL maintainer="Daniel <daniel.hu@cloudwise.com>"

COPY requirements.txt /requirements.txt
RUN apt-get install python-software-properties -y && \
    add-apt-repository ppa:ubuntu-toolchain-r/test && \
    apt-get update && \
    apt-get install gcc-9 g++-9 -y && \
    update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-9 90 --slave /usr/bin/g++ g++ /usr/bin/g++-9 && \
    pip install --no-cache-dir -r /requirements.txt

