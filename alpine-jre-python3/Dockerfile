FROM store/oracle/serverjre:8

ENV PYTHONIOENCODING=UTF-8

RUN yum -y update \
    && yum install -y sudo gcc make \
    && yum install -y python36 python36-devel python36-pip \
    && yum install -y graphviz graphviz-devel \
    && ln -s /usr/bin/python3.6 /usr/bin/python3 \
    && yum clean all

CMD ["python3"]