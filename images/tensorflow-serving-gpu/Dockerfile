FROM tensorflow/serving:2.1.0-gpu

RUN apt-get update -qq && apt-get install -y --no-install-recommends -q \
        libnvinfer6=6.0.1-1+cuda10.1 \
        libnvinfer-plugin6=6.0.1-1+cuda10.1 \
    && apt-get clean -qq && rm -rf /var/lib/apt/lists/*

RUN mkdir /etc/tfs && echo "model_config_list {}" > /etc/tfs/model_config_server.conf
