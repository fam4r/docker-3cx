FROM debian:9

ENV container docker
ENV DEBIAN_FRONTEND noninteractive

# solving annoying debian network problems
RUN echo "nameserver 1.1.1.1" > /etc/resolv.conf \
    && apt-get update -y \
    && apt-get install -y \
        systemd \
    && apt-key adv --fetch-keys http://downloads-global.3cx.com/downloads/3cxpbx/public.key \
    && echo "deb http://downloads-global.3cx.com/downloads/debian stretch main" | tee /etc/apt/sources.list.d/3cxpbx.list \
    && apt-get update -y \
    && apt-get install -y \
        3cxpbx \
        net-tools \
    && rm -rf /var/lib/apt/lists/*

# && wget -O- http://downloads-global.3cx.com/downloads/3cxpbx/public.key | apt-key add - \
