FROM inwt/r-base:latest

RUN apt-get -y update \
    && apt-get install -y --no-install-recommends \
        openjdk-8-jdk \
        libbz2-dev \
        liblzma-dev \
        libpcre3-dev \
        libmariadb-client-lgpl-dev \
    && apt-get autoremove -y \
    && apt-get autoclean -y \
    && rm -rf /var/lib/apt/lists/* \
    && R CMD javareconf \
    && installPackage \
        data.table \
        dplyr \
        futile.logger \
        gbm \
        ggplot2 \
        gridExtra \
        lme4 \
        mgcv \
        rJava \
        RMySQL \
        tidyr \
    && installGithub \
        INWT/dbtools \
        INWT/mctools \
    && rm -rf /tmp/downloaded_packages/*
