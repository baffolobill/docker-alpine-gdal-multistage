# How to use it

```
FROM python:3.6-alpine3.8

...

# gdal-2.2.4-r0.apk | gdal-dev-2.2.4-r0.apk | py-gdal-2.2.4-r0.apk
COPY --from=baffolobill/alpine-gdal-multistage:latest /home/packager/packages/x86_64/gdal-2.2.4-r0.apk /tmp/gdal.apk
# COPY --from=baffolobill/alpine-gdal-multistage:latest /home/packager/packages/x86_64/gdal-dev-2.2.4-r0.apk /tmp/gdal-dev.apk
# COPY --from=baffolobill/alpine-gdal-multistage:latest /home/packager/packages/x86_64/py-gdal-2.2.4-r0.apk /tmp/py-gdal.apk

RUN \
    apk add /tmp/gdal.apk --allow-untrusted

...

```
