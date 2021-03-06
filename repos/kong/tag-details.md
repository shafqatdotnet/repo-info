<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kong`

-	[`kong:0.10`](#kong010)
-	[`kong:0.10.3`](#kong0103)
-	[`kong:0.11`](#kong011)
-	[`kong:0.11.0`](#kong0110)
-	[`kong:0.11.0-alpine`](#kong0110-alpine)
-	[`kong:0.11-alpine`](#kong011-alpine)
-	[`kong:0.9`](#kong09)
-	[`kong:0.9.9`](#kong099)
-	[`kong:latest`](#konglatest)

## `kong:0.10`

```console
$ docker pull kong@sha256:21906cabdbd11e6fef944dbae4527eaf13a7078890cfe5d9c1ae0cd08496da72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:0.10` - linux; amd64

```console
$ docker pull kong@sha256:3076c2cfe270f84d22044119bb566ff5804abb119694d46c8583861f493b2a3f
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 MB (126726264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:894c11ab03427875c32bdaca48c6fb83eccbc82fc66728eb3164fb6db8e5f801`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","start"]`

```dockerfile
# Thu, 14 Sep 2017 15:13:25 GMT
ADD file:1ed4d1a29d09a636dd6c60c6187679adb26c877b6be6968e14272e75ad240073 in / 
# Thu, 14 Sep 2017 15:13:25 GMT
LABEL name=CentOS Base Image vendor=CentOS license=GPLv2 build-date=20170911
# Thu, 14 Sep 2017 15:13:25 GMT
CMD ["/bin/bash"]
# Thu, 14 Sep 2017 15:30:07 GMT
MAINTAINER Marco Palladino, marco@mashape.com
# Thu, 14 Sep 2017 15:30:23 GMT
ENV KONG_VERSION=0.10.3
# Thu, 14 Sep 2017 15:30:40 GMT
RUN yum install -y wget https://github.com/Mashape/kong/releases/download/$KONG_VERSION/kong-$KONG_VERSION.el7.noarch.rpm &&     yum clean all
# Thu, 14 Sep 2017 15:30:44 GMT
RUN wget -O /usr/local/bin/dumb-init https://github.com/Yelp/dumb-init/releases/download/v1.1.3/dumb-init_1.1.3_amd64 &&     chmod +x /usr/local/bin/dumb-init
# Thu, 14 Sep 2017 15:30:44 GMT
COPY file:e806c057c1c71a8dd5e684244eed51d4ff17ca43efe7233573320a3bf8dda3a4 in /docker-entrypoint.sh 
# Thu, 14 Sep 2017 15:30:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Sep 2017 15:30:44 GMT
EXPOSE 7946/tcp 8000/tcp 8001/tcp 8443/tcp
# Thu, 14 Sep 2017 15:30:44 GMT
CMD ["kong" "start"]
```

-	Layers:
	-	`sha256:d9aaf4d82f249dc101a6638ff5177fe926cdebfa6c42d874dfa5029533da0e72`  
		Last Modified: Thu, 14 Sep 2017 15:14:02 GMT  
		Size: 73.4 MB (73386947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:052d933f5529bdc57f67ca10dacdbdec8abeeccb1488e5caa27f1c08fe766b29`  
		Last Modified: Thu, 14 Sep 2017 15:31:53 GMT  
		Size: 53.3 MB (53313558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e32cb8391770142af04332c6ccd0c58f14a6804cbbcc72fff5c30a317135f8e`  
		Last Modified: Thu, 14 Sep 2017 15:31:45 GMT  
		Size: 25.5 KB (25540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e42934f4f03a5fdbe0410d5e51851c093624383b08f43bfec9c7415e322225ce`  
		Last Modified: Thu, 14 Sep 2017 15:31:45 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:0.10.3`

```console
$ docker pull kong@sha256:21906cabdbd11e6fef944dbae4527eaf13a7078890cfe5d9c1ae0cd08496da72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:0.10.3` - linux; amd64

```console
$ docker pull kong@sha256:3076c2cfe270f84d22044119bb566ff5804abb119694d46c8583861f493b2a3f
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 MB (126726264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:894c11ab03427875c32bdaca48c6fb83eccbc82fc66728eb3164fb6db8e5f801`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","start"]`

```dockerfile
# Thu, 14 Sep 2017 15:13:25 GMT
ADD file:1ed4d1a29d09a636dd6c60c6187679adb26c877b6be6968e14272e75ad240073 in / 
# Thu, 14 Sep 2017 15:13:25 GMT
LABEL name=CentOS Base Image vendor=CentOS license=GPLv2 build-date=20170911
# Thu, 14 Sep 2017 15:13:25 GMT
CMD ["/bin/bash"]
# Thu, 14 Sep 2017 15:30:07 GMT
MAINTAINER Marco Palladino, marco@mashape.com
# Thu, 14 Sep 2017 15:30:23 GMT
ENV KONG_VERSION=0.10.3
# Thu, 14 Sep 2017 15:30:40 GMT
RUN yum install -y wget https://github.com/Mashape/kong/releases/download/$KONG_VERSION/kong-$KONG_VERSION.el7.noarch.rpm &&     yum clean all
# Thu, 14 Sep 2017 15:30:44 GMT
RUN wget -O /usr/local/bin/dumb-init https://github.com/Yelp/dumb-init/releases/download/v1.1.3/dumb-init_1.1.3_amd64 &&     chmod +x /usr/local/bin/dumb-init
# Thu, 14 Sep 2017 15:30:44 GMT
COPY file:e806c057c1c71a8dd5e684244eed51d4ff17ca43efe7233573320a3bf8dda3a4 in /docker-entrypoint.sh 
# Thu, 14 Sep 2017 15:30:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Sep 2017 15:30:44 GMT
EXPOSE 7946/tcp 8000/tcp 8001/tcp 8443/tcp
# Thu, 14 Sep 2017 15:30:44 GMT
CMD ["kong" "start"]
```

-	Layers:
	-	`sha256:d9aaf4d82f249dc101a6638ff5177fe926cdebfa6c42d874dfa5029533da0e72`  
		Last Modified: Thu, 14 Sep 2017 15:14:02 GMT  
		Size: 73.4 MB (73386947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:052d933f5529bdc57f67ca10dacdbdec8abeeccb1488e5caa27f1c08fe766b29`  
		Last Modified: Thu, 14 Sep 2017 15:31:53 GMT  
		Size: 53.3 MB (53313558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e32cb8391770142af04332c6ccd0c58f14a6804cbbcc72fff5c30a317135f8e`  
		Last Modified: Thu, 14 Sep 2017 15:31:45 GMT  
		Size: 25.5 KB (25540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e42934f4f03a5fdbe0410d5e51851c093624383b08f43bfec9c7415e322225ce`  
		Last Modified: Thu, 14 Sep 2017 15:31:45 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:0.11`

```console
$ docker pull kong@sha256:d24e86684ec127afed3e28fad3a7802d3f9fd4f8fcc7b3cada8e6614ddc53a24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:0.11` - linux; amd64

```console
$ docker pull kong@sha256:a13ce3786145ff2d55032557a054403cd40e1f16e07d794493d3913a2e01ea15
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122416043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:604ef970973d69d882d5440922099b9dada0023df3c8772caa483163c2b8f38c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/local\/openresty\/nginx\/sbin\/nginx","-c","\/usr\/local\/kong\/nginx.conf","-p","\/usr\/local\/kong\/"]`

```dockerfile
# Thu, 14 Sep 2017 15:13:25 GMT
ADD file:1ed4d1a29d09a636dd6c60c6187679adb26c877b6be6968e14272e75ad240073 in / 
# Thu, 14 Sep 2017 15:13:25 GMT
LABEL name=CentOS Base Image vendor=CentOS license=GPLv2 build-date=20170911
# Thu, 14 Sep 2017 15:13:25 GMT
CMD ["/bin/bash"]
# Thu, 14 Sep 2017 15:30:07 GMT
MAINTAINER Marco Palladino, marco@mashape.com
# Thu, 14 Sep 2017 15:30:07 GMT
ENV KONG_VERSION=0.11.0
# Thu, 14 Sep 2017 15:30:20 GMT
RUN yum install -y wget https://bintray.com/kong/kong-community-edition-rpm/download_file?file_path=dists%2Fkong-community-edition-$KONG_VERSION.el7.noarch.rpm &&     yum clean all
# Thu, 14 Sep 2017 15:30:20 GMT
COPY file:0ce55305f95ddcb78ffb96b9502c795c4dd1040025f4ec7c3e19e4b889022b90 in /docker-entrypoint.sh 
# Thu, 14 Sep 2017 15:30:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Sep 2017 15:30:20 GMT
EXPOSE 8000/tcp 8001/tcp 8443/tcp 8444/tcp
# Thu, 14 Sep 2017 15:30:21 GMT
STOPSIGNAL [SIGTERM]
# Thu, 14 Sep 2017 15:30:21 GMT
CMD ["/usr/local/openresty/nginx/sbin/nginx" "-c" "/usr/local/kong/nginx.conf" "-p" "/usr/local/kong/"]
```

-	Layers:
	-	`sha256:d9aaf4d82f249dc101a6638ff5177fe926cdebfa6c42d874dfa5029533da0e72`  
		Last Modified: Thu, 14 Sep 2017 15:14:02 GMT  
		Size: 73.4 MB (73386947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f2d122a51b684cb1b4cd1f0bcdb497b78319439f9bc7e555c7699584cc67f17`  
		Last Modified: Thu, 14 Sep 2017 15:31:27 GMT  
		Size: 49.0 MB (49028772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b197bb47cac3bd9974e45eb8c91bfb922190480ce82ceba41f5f60275016a8aa`  
		Last Modified: Thu, 14 Sep 2017 15:31:17 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:0.11.0`

```console
$ docker pull kong@sha256:d24e86684ec127afed3e28fad3a7802d3f9fd4f8fcc7b3cada8e6614ddc53a24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:0.11.0` - linux; amd64

```console
$ docker pull kong@sha256:a13ce3786145ff2d55032557a054403cd40e1f16e07d794493d3913a2e01ea15
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122416043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:604ef970973d69d882d5440922099b9dada0023df3c8772caa483163c2b8f38c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/local\/openresty\/nginx\/sbin\/nginx","-c","\/usr\/local\/kong\/nginx.conf","-p","\/usr\/local\/kong\/"]`

```dockerfile
# Thu, 14 Sep 2017 15:13:25 GMT
ADD file:1ed4d1a29d09a636dd6c60c6187679adb26c877b6be6968e14272e75ad240073 in / 
# Thu, 14 Sep 2017 15:13:25 GMT
LABEL name=CentOS Base Image vendor=CentOS license=GPLv2 build-date=20170911
# Thu, 14 Sep 2017 15:13:25 GMT
CMD ["/bin/bash"]
# Thu, 14 Sep 2017 15:30:07 GMT
MAINTAINER Marco Palladino, marco@mashape.com
# Thu, 14 Sep 2017 15:30:07 GMT
ENV KONG_VERSION=0.11.0
# Thu, 14 Sep 2017 15:30:20 GMT
RUN yum install -y wget https://bintray.com/kong/kong-community-edition-rpm/download_file?file_path=dists%2Fkong-community-edition-$KONG_VERSION.el7.noarch.rpm &&     yum clean all
# Thu, 14 Sep 2017 15:30:20 GMT
COPY file:0ce55305f95ddcb78ffb96b9502c795c4dd1040025f4ec7c3e19e4b889022b90 in /docker-entrypoint.sh 
# Thu, 14 Sep 2017 15:30:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Sep 2017 15:30:20 GMT
EXPOSE 8000/tcp 8001/tcp 8443/tcp 8444/tcp
# Thu, 14 Sep 2017 15:30:21 GMT
STOPSIGNAL [SIGTERM]
# Thu, 14 Sep 2017 15:30:21 GMT
CMD ["/usr/local/openresty/nginx/sbin/nginx" "-c" "/usr/local/kong/nginx.conf" "-p" "/usr/local/kong/"]
```

-	Layers:
	-	`sha256:d9aaf4d82f249dc101a6638ff5177fe926cdebfa6c42d874dfa5029533da0e72`  
		Last Modified: Thu, 14 Sep 2017 15:14:02 GMT  
		Size: 73.4 MB (73386947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f2d122a51b684cb1b4cd1f0bcdb497b78319439f9bc7e555c7699584cc67f17`  
		Last Modified: Thu, 14 Sep 2017 15:31:27 GMT  
		Size: 49.0 MB (49028772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b197bb47cac3bd9974e45eb8c91bfb922190480ce82ceba41f5f60275016a8aa`  
		Last Modified: Thu, 14 Sep 2017 15:31:17 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:0.11.0-alpine`

```console
$ docker pull kong@sha256:9e472cf80d6f882feadc20f30b6538a535cbe2071270af9e098f443188b27425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:0.11.0-alpine` - linux; amd64

```console
$ docker pull kong@sha256:0a96e8b14a3385bb4e3250fe0335624943be31fa37aef9ac8fa301ec71470876
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.6 MB (29643439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d53207c4f9f5cc1cb23f98f8de4f109d3f28e4b0f0a89aefa0485ad3a5d2c7ed`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/local\/openresty\/nginx\/sbin\/nginx","-c","\/usr\/local\/kong\/nginx.conf","-p","\/usr\/local\/kong\/"]`

```dockerfile
# Wed, 13 Sep 2017 14:32:25 GMT
ADD file:4583e12bf5caec40b861a3409f2a1624c3f3556cc457edb99c9707f00e779e45 in / 
# Wed, 13 Sep 2017 14:32:26 GMT
CMD ["/bin/sh"]
# Wed, 13 Sep 2017 15:08:07 GMT
MAINTAINER Marco Palladino, marco@mashape.com
# Wed, 13 Sep 2017 15:08:07 GMT
ENV KONG_VERSION=0.11.0
# Wed, 13 Sep 2017 15:08:07 GMT
ENV KONG_SHA256=34cfd44f61a4da5d39ad7b59bad7b4790451065ff8c8c3d000b6258ab6961949
# Wed, 13 Sep 2017 15:08:14 GMT
RUN apk update 	&& apk add --virtual .build-deps wget tar ca-certificates 	&& apk add libgcc openssl pcre perl 	&& wget -O kong.tar.gz "https://bintray.com/kong/kong-community-edition-alpine-tar/download_file?file_path=kong-community-edition-$KONG_VERSION.apk.tar.gz" 	&& echo "$KONG_SHA256 *kong.tar.gz" | sha256sum -c - 	&& tar -xzf kong.tar.gz -C /tmp 	&& rm -f kong.tar.gz 	&& cp -R /tmp/usr / 	&& rm -rf /tmp/usr 	&& apk del .build-deps 	&& rm -rf /var/cache/apk/*
# Wed, 13 Sep 2017 15:08:14 GMT
COPY file:0ce55305f95ddcb78ffb96b9502c795c4dd1040025f4ec7c3e19e4b889022b90 in /docker-entrypoint.sh 
# Wed, 13 Sep 2017 15:08:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 Sep 2017 15:08:15 GMT
EXPOSE 8000/tcp 8001/tcp 8443/tcp 8444/tcp
# Wed, 13 Sep 2017 15:08:15 GMT
STOPSIGNAL [SIGTERM]
# Wed, 13 Sep 2017 15:08:15 GMT
CMD ["/usr/local/openresty/nginx/sbin/nginx" "-c" "/usr/local/kong/nginx.conf" "-p" "/usr/local/kong/"]
```

-	Layers:
	-	`sha256:88286f41530e93dffd4b964e1db22ce4939fffa4a4c665dab8591fbab03d4926`  
		Last Modified: Tue, 27 Jun 2017 18:49:37 GMT  
		Size: 2.0 MB (1990402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302f074c33811ca33103ba205e854540e7ba02a9a405e5c5097ed4b7136f94a5`  
		Last Modified: Wed, 13 Sep 2017 15:09:45 GMT  
		Size: 27.7 MB (27652712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f620b320e5faa10de01c3eb15293ac4821821c981b9ba5fbafe315a4215833f9`  
		Last Modified: Wed, 13 Sep 2017 15:09:39 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:0.11-alpine`

```console
$ docker pull kong@sha256:9e472cf80d6f882feadc20f30b6538a535cbe2071270af9e098f443188b27425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:0.11-alpine` - linux; amd64

```console
$ docker pull kong@sha256:0a96e8b14a3385bb4e3250fe0335624943be31fa37aef9ac8fa301ec71470876
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.6 MB (29643439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d53207c4f9f5cc1cb23f98f8de4f109d3f28e4b0f0a89aefa0485ad3a5d2c7ed`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/local\/openresty\/nginx\/sbin\/nginx","-c","\/usr\/local\/kong\/nginx.conf","-p","\/usr\/local\/kong\/"]`

```dockerfile
# Wed, 13 Sep 2017 14:32:25 GMT
ADD file:4583e12bf5caec40b861a3409f2a1624c3f3556cc457edb99c9707f00e779e45 in / 
# Wed, 13 Sep 2017 14:32:26 GMT
CMD ["/bin/sh"]
# Wed, 13 Sep 2017 15:08:07 GMT
MAINTAINER Marco Palladino, marco@mashape.com
# Wed, 13 Sep 2017 15:08:07 GMT
ENV KONG_VERSION=0.11.0
# Wed, 13 Sep 2017 15:08:07 GMT
ENV KONG_SHA256=34cfd44f61a4da5d39ad7b59bad7b4790451065ff8c8c3d000b6258ab6961949
# Wed, 13 Sep 2017 15:08:14 GMT
RUN apk update 	&& apk add --virtual .build-deps wget tar ca-certificates 	&& apk add libgcc openssl pcre perl 	&& wget -O kong.tar.gz "https://bintray.com/kong/kong-community-edition-alpine-tar/download_file?file_path=kong-community-edition-$KONG_VERSION.apk.tar.gz" 	&& echo "$KONG_SHA256 *kong.tar.gz" | sha256sum -c - 	&& tar -xzf kong.tar.gz -C /tmp 	&& rm -f kong.tar.gz 	&& cp -R /tmp/usr / 	&& rm -rf /tmp/usr 	&& apk del .build-deps 	&& rm -rf /var/cache/apk/*
# Wed, 13 Sep 2017 15:08:14 GMT
COPY file:0ce55305f95ddcb78ffb96b9502c795c4dd1040025f4ec7c3e19e4b889022b90 in /docker-entrypoint.sh 
# Wed, 13 Sep 2017 15:08:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 Sep 2017 15:08:15 GMT
EXPOSE 8000/tcp 8001/tcp 8443/tcp 8444/tcp
# Wed, 13 Sep 2017 15:08:15 GMT
STOPSIGNAL [SIGTERM]
# Wed, 13 Sep 2017 15:08:15 GMT
CMD ["/usr/local/openresty/nginx/sbin/nginx" "-c" "/usr/local/kong/nginx.conf" "-p" "/usr/local/kong/"]
```

-	Layers:
	-	`sha256:88286f41530e93dffd4b964e1db22ce4939fffa4a4c665dab8591fbab03d4926`  
		Last Modified: Tue, 27 Jun 2017 18:49:37 GMT  
		Size: 2.0 MB (1990402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302f074c33811ca33103ba205e854540e7ba02a9a405e5c5097ed4b7136f94a5`  
		Last Modified: Wed, 13 Sep 2017 15:09:45 GMT  
		Size: 27.7 MB (27652712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f620b320e5faa10de01c3eb15293ac4821821c981b9ba5fbafe315a4215833f9`  
		Last Modified: Wed, 13 Sep 2017 15:09:39 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:0.9`

```console
$ docker pull kong@sha256:be342fa319f0cd989eb6df6dc10194b31b7bb7653a6630da8d073cfa85196a58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:0.9` - linux; amd64

```console
$ docker pull kong@sha256:b27b6c30c9b9ac11fd74f99defe2cee843ebd322429b7b74b318dfdb20cd358c
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126475473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3456bd2afcb52394db1fcd13d30beaff0f783faa39e484b166960a8efc36bb4e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","start"]`

```dockerfile
# Thu, 14 Sep 2017 15:13:25 GMT
ADD file:1ed4d1a29d09a636dd6c60c6187679adb26c877b6be6968e14272e75ad240073 in / 
# Thu, 14 Sep 2017 15:13:25 GMT
LABEL name=CentOS Base Image vendor=CentOS license=GPLv2 build-date=20170911
# Thu, 14 Sep 2017 15:13:25 GMT
CMD ["/bin/bash"]
# Thu, 14 Sep 2017 15:30:07 GMT
MAINTAINER Marco Palladino, marco@mashape.com
# Thu, 14 Sep 2017 15:30:47 GMT
ENV KONG_VERSION=0.9.9
# Thu, 14 Sep 2017 15:31:04 GMT
RUN yum install -y wget https://github.com/Mashape/kong/releases/download/$KONG_VERSION/kong-$KONG_VERSION.el7.noarch.rpm &&     yum clean all
# Thu, 14 Sep 2017 15:31:07 GMT
RUN wget -O /usr/local/bin/dumb-init https://github.com/Yelp/dumb-init/releases/download/v1.1.3/dumb-init_1.1.3_amd64 &&     chmod +x /usr/local/bin/dumb-init
# Thu, 14 Sep 2017 15:31:07 GMT
COPY file:e806c057c1c71a8dd5e684244eed51d4ff17ca43efe7233573320a3bf8dda3a4 in /docker-entrypoint.sh 
# Thu, 14 Sep 2017 15:31:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Sep 2017 15:31:07 GMT
EXPOSE 7946/tcp 8000/tcp 8001/tcp 8443/tcp
# Thu, 14 Sep 2017 15:31:07 GMT
CMD ["kong" "start"]
```

-	Layers:
	-	`sha256:d9aaf4d82f249dc101a6638ff5177fe926cdebfa6c42d874dfa5029533da0e72`  
		Last Modified: Thu, 14 Sep 2017 15:14:02 GMT  
		Size: 73.4 MB (73386947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77cca0fdde081046fa9bdca35e121ae68b104f4bb3532aa08f7bae8c84d922be`  
		Last Modified: Thu, 14 Sep 2017 15:32:15 GMT  
		Size: 53.1 MB (53062767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2159e439b5f69ab0fce1510ba091364026acf172bb20afcff493b5cde0dbb03c`  
		Last Modified: Thu, 14 Sep 2017 15:32:07 GMT  
		Size: 25.5 KB (25540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e6505f2d152811c726bd8722f300c0889495747d7e41ac72c72852f3d65755`  
		Last Modified: Thu, 14 Sep 2017 15:32:07 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:0.9.9`

```console
$ docker pull kong@sha256:be342fa319f0cd989eb6df6dc10194b31b7bb7653a6630da8d073cfa85196a58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:0.9.9` - linux; amd64

```console
$ docker pull kong@sha256:b27b6c30c9b9ac11fd74f99defe2cee843ebd322429b7b74b318dfdb20cd358c
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126475473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3456bd2afcb52394db1fcd13d30beaff0f783faa39e484b166960a8efc36bb4e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","start"]`

```dockerfile
# Thu, 14 Sep 2017 15:13:25 GMT
ADD file:1ed4d1a29d09a636dd6c60c6187679adb26c877b6be6968e14272e75ad240073 in / 
# Thu, 14 Sep 2017 15:13:25 GMT
LABEL name=CentOS Base Image vendor=CentOS license=GPLv2 build-date=20170911
# Thu, 14 Sep 2017 15:13:25 GMT
CMD ["/bin/bash"]
# Thu, 14 Sep 2017 15:30:07 GMT
MAINTAINER Marco Palladino, marco@mashape.com
# Thu, 14 Sep 2017 15:30:47 GMT
ENV KONG_VERSION=0.9.9
# Thu, 14 Sep 2017 15:31:04 GMT
RUN yum install -y wget https://github.com/Mashape/kong/releases/download/$KONG_VERSION/kong-$KONG_VERSION.el7.noarch.rpm &&     yum clean all
# Thu, 14 Sep 2017 15:31:07 GMT
RUN wget -O /usr/local/bin/dumb-init https://github.com/Yelp/dumb-init/releases/download/v1.1.3/dumb-init_1.1.3_amd64 &&     chmod +x /usr/local/bin/dumb-init
# Thu, 14 Sep 2017 15:31:07 GMT
COPY file:e806c057c1c71a8dd5e684244eed51d4ff17ca43efe7233573320a3bf8dda3a4 in /docker-entrypoint.sh 
# Thu, 14 Sep 2017 15:31:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Sep 2017 15:31:07 GMT
EXPOSE 7946/tcp 8000/tcp 8001/tcp 8443/tcp
# Thu, 14 Sep 2017 15:31:07 GMT
CMD ["kong" "start"]
```

-	Layers:
	-	`sha256:d9aaf4d82f249dc101a6638ff5177fe926cdebfa6c42d874dfa5029533da0e72`  
		Last Modified: Thu, 14 Sep 2017 15:14:02 GMT  
		Size: 73.4 MB (73386947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77cca0fdde081046fa9bdca35e121ae68b104f4bb3532aa08f7bae8c84d922be`  
		Last Modified: Thu, 14 Sep 2017 15:32:15 GMT  
		Size: 53.1 MB (53062767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2159e439b5f69ab0fce1510ba091364026acf172bb20afcff493b5cde0dbb03c`  
		Last Modified: Thu, 14 Sep 2017 15:32:07 GMT  
		Size: 25.5 KB (25540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e6505f2d152811c726bd8722f300c0889495747d7e41ac72c72852f3d65755`  
		Last Modified: Thu, 14 Sep 2017 15:32:07 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:latest`

```console
$ docker pull kong@sha256:d24e86684ec127afed3e28fad3a7802d3f9fd4f8fcc7b3cada8e6614ddc53a24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:latest` - linux; amd64

```console
$ docker pull kong@sha256:a13ce3786145ff2d55032557a054403cd40e1f16e07d794493d3913a2e01ea15
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122416043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:604ef970973d69d882d5440922099b9dada0023df3c8772caa483163c2b8f38c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/local\/openresty\/nginx\/sbin\/nginx","-c","\/usr\/local\/kong\/nginx.conf","-p","\/usr\/local\/kong\/"]`

```dockerfile
# Thu, 14 Sep 2017 15:13:25 GMT
ADD file:1ed4d1a29d09a636dd6c60c6187679adb26c877b6be6968e14272e75ad240073 in / 
# Thu, 14 Sep 2017 15:13:25 GMT
LABEL name=CentOS Base Image vendor=CentOS license=GPLv2 build-date=20170911
# Thu, 14 Sep 2017 15:13:25 GMT
CMD ["/bin/bash"]
# Thu, 14 Sep 2017 15:30:07 GMT
MAINTAINER Marco Palladino, marco@mashape.com
# Thu, 14 Sep 2017 15:30:07 GMT
ENV KONG_VERSION=0.11.0
# Thu, 14 Sep 2017 15:30:20 GMT
RUN yum install -y wget https://bintray.com/kong/kong-community-edition-rpm/download_file?file_path=dists%2Fkong-community-edition-$KONG_VERSION.el7.noarch.rpm &&     yum clean all
# Thu, 14 Sep 2017 15:30:20 GMT
COPY file:0ce55305f95ddcb78ffb96b9502c795c4dd1040025f4ec7c3e19e4b889022b90 in /docker-entrypoint.sh 
# Thu, 14 Sep 2017 15:30:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Sep 2017 15:30:20 GMT
EXPOSE 8000/tcp 8001/tcp 8443/tcp 8444/tcp
# Thu, 14 Sep 2017 15:30:21 GMT
STOPSIGNAL [SIGTERM]
# Thu, 14 Sep 2017 15:30:21 GMT
CMD ["/usr/local/openresty/nginx/sbin/nginx" "-c" "/usr/local/kong/nginx.conf" "-p" "/usr/local/kong/"]
```

-	Layers:
	-	`sha256:d9aaf4d82f249dc101a6638ff5177fe926cdebfa6c42d874dfa5029533da0e72`  
		Last Modified: Thu, 14 Sep 2017 15:14:02 GMT  
		Size: 73.4 MB (73386947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f2d122a51b684cb1b4cd1f0bcdb497b78319439f9bc7e555c7699584cc67f17`  
		Last Modified: Thu, 14 Sep 2017 15:31:27 GMT  
		Size: 49.0 MB (49028772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b197bb47cac3bd9974e45eb8c91bfb922190480ce82ceba41f5f60275016a8aa`  
		Last Modified: Thu, 14 Sep 2017 15:31:17 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
