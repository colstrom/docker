FROM ubuntu:14.04

RUN locale-gen en_US.UTF-8
RUN update-locale LC_ALL=en_US.UTF-8 LANG=en_US.UTF-8 LANGUAGE=en_US.UTF-8

ENV LC_ALL en_US.UTF-8
ENV LANG en_US.UTF-8
ENV LANGUAGE en_US.UTF-8

RUN apt-get update && apt-get install -y \
        bzip2 \
        libyaml-0-2 \
        libssl1.0.0 \
        clang-3.6 \
        libedit-dev \
        make

ADD https://rubinius-binaries-rubinius-com.s3-us-west-2.amazonaws.com/ubuntu/14.04/x86_64/rubinius-3.55.tar.bz2 /tmp/rubinius.tar.bz2
RUN cd /opt && tar xvjf /tmp/rubinius.tar.bz2

ENV PATH /opt/rubinius/3.55/bin:/opt/rubinius/3.55/gems/bin:$PATH

CMD ["bash"]
