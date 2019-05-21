FROM python:3.6-alpine

LABEL maintainer="Daniel <daniel.hu@cloudwise.com>"

RUN apk update && \
    apk upgrade && \
    apk add --no-cache libstdc++ && \
    apk add --no-cache --virtual=build_deps g++ gfortran && \
    ln -s /usr/include/locale.h /usr/include/xlocale.h && \
    pip install --no-cache-dir pandas numpy fbprophet Cython pystan && \
    rm /usr/include/xlocale.h && \
    apk del build_deps

CMD ["python"]