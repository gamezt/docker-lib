FROM alpine:latest
LABEL maintainer="ztgoto"
ENV ETCD_VERSION=v3.4.7
ENV ETCD_HOME=/etcd
WORKDIR ${ETCD_HOME}
RUN apk add -U curl
RUN curl -L https://github.com/etcd-io/etcd/releases/download/${ETCD_VERSION}/etcd-${ETCD_VERSION}-linux-amd64.tar.gz -o ${ETCD_HOME}/etcd-${ETCD_VERSION}-linux-amd64.tar.gz \
&& tar xzvf ${ETCD_HOME}/etcd-${ETCD_VERSION}-linux-amd64.tar.gz -C ${ETCD_HOME} --strip-components=1 \
&& rm -f ${ETCD_HOME}/etcd-${ETCD_VERSION}-linux-amd64.tar.gz

EXPOSE 2379 2380

