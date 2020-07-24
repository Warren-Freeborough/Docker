FROM alpine

RUN mkdir data
# install git
RUN apk --update add git less openssh && \
rm -rf /var/lib/apt/lists/* && \
rm /var/cache/apk/*

#Dependencies 
RUN apk update
RUN apk add autoconf automake make gcc musl-dev perl bash zlib-dev bzip2-dev xz-dev curl-dev libressl-dev gsl-dev perl-dev
# Download and install 
RUN git clone git://github.com/samtools/htslib.git 
RUN git clone git://github.com/samtools/bcftools.git &&\
cd bcftools &&\
make&&\
make install 
RUN export BCFTOOLS_PLUGINS=/path/to/bcftools/plugins

