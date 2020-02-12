# Based on rocker/r-base
# https://github.com/rocker-org/rocker/tree/master/r-base

FROM debian:buster-20200130-slim

LABEL maintainer="Erik Howard <erikhoward@pm.me>"

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update \
    && apt-get install -y --no-install-recommends \
        apt-transport-https \
        ca-certificates \
        dirmngr \
        file \
        fonts-texgyre \
        g++ \
        gfortran \
        gnupg \
        gsfonts \
        libblas-dev \
        libbz2-1.0 \
        libcurl4 \
        libopenblas-dev \
        libpangocairo-1.0-0 \
        libpcre3 \
        libpng16-16 \
        libreadline7 \
        libtiff5 \
        liblzma5 \
        less \
        locales \
        make \
        unzip \
        vim-tiny \
        wget \
        zlib1g \
        software-properties-common

# Configure default locale
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen \
    && locale-gen en_US.utf8 \
    && /usr/sbin/update-locale LANG=en_US.UTF-8

RUN apt-key adv --keyserver keys.gnupg.net --recv-key 'E19F5F87128899B192B1A2C2AD5F960A256A04AF'
RUN add-apt-repository 'deb http://cloud.r-project.org/bin/linux/debian buster-cran35/'

ENV R_BASE_VERSION 3.6.2

RUN apt-get update \
    && apt-get install -y --no-install-recommends \
        littler \
        r-cran-littler \
        r-base=${R_BASE_VERSION}-* \
        r-base-dev=${R_BASE_VERSION}-* \
        r-recommended=${R_BASE_VERSION}-* \
    && ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r \
    && ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r \
    && ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r \
    && ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r \
    && install.r docopt \
    && rm -rf /tmp/downloaded_packages/ /tmp/*.rds \
    && rm -rf /var/lib/apt/lists/*

CMD ["R"]
