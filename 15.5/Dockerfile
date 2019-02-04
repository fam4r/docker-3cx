FROM debian:9

RUN apt-get update -y \
    && apt-get install -y \
        wget \
    && wget -O- http://downloads-global.3cx.com/downloads/3cxpbx/public.key | apt-key add - \
    && echo "deb http://downloads-global.3cx.com/downloads/debian stretch main" | tee /etc/apt/sources.list.d/3cxpbx.list \
    && apt-get update -y \
    && apt-get install -y \
        3cxpbx \
        net-tools \
    && rm -rf /var/lib/apt/lists/*
