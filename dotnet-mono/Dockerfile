FROM alpine:3.3

#
# docker run -it --name dotnet-teste -t drr00t/mono-base:4.2.2.30-r1 /bin/sh
#
#


RUN echo "@testing http://dl-4.alpinelinux.org/alpine/edge/testing" >> /etc/apk/repositories \
    && apk add --update mono@testing  \
    && rm -rf /var/cache/apk/* \
    && mozroots --import --sync \
    && rm -rf /tmp/* \
    && rm -rf /var/cache/apk/*

RUN mkdir -p /opt/dotnet/apps \
    && cd /opt/dotnet/apps

ADD https://dist.nuget.org/win-x86-commandline/latest/nuget.exe /opt/dotnet/apps/nuget.exe

#mono nuget.exe install fake


