FROM alpine:latest
LABEL maintainer="ztgoto"
ARG ETCD_VERSION=v3.4.7

RUN mkdir /etcd \
&& wget https://github.com/etcd-io/etcd/releases/download/${ETCD_VERSION}/etcd-${ETCD_VERSION}-linux-amd64.tar.gz -O /etcd/etcd-${ETCD_VERSION}-linux-amd64.tar.gz \
&& tar xzvf /etcd/etcd-${ETCD_VERSION}-linux-amd64.tar.gz -C /etcd --strip-components=1 \
&& mv /etcd/etcd /etcd/etcdctl /usr/local/bin/ \
&& mkdir -p /etc/etcd/ /var/lib/etcd/ \
&& rm -rf /etcd

EXPOSE 2379 2380

CMD [ "/usr/local/bin/etcd" ]