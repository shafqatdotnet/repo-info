<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `swipl`

-	[`swipl:7.5.15`](#swipl7515)
-	[`swipl:latest`](#swipllatest)

## `swipl:7.5.15`

```console
$ docker pull swipl@sha256:942f751fa64ea7e9860c23ab41e78d0d1483025371e5c5a6f475bc34f2f0f8fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `swipl:7.5.15` - linux; amd64

```console
$ docker pull swipl@sha256:5528e123c3d843df126f3989ee209c121f84d01f4f583bce366499de6e2cbbe4
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50982670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ba25ea612793e78526f21f481ed6c56080483f65182715c05021aea7a6524a`
-	Default Command: `["swipl"]`

```dockerfile
# Wed, 13 Sep 2017 08:41:48 GMT
ADD file:2bc9df54d28d9ec75722f6748834a1aea0baf089047e86a541064c282246c300 in / 
# Wed, 13 Sep 2017 08:41:49 GMT
CMD ["bash"]
# Wed, 13 Sep 2017 21:28:38 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Wed, 13 Sep 2017 21:28:51 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libarchive13     libgmp10     libossp-uuid16     libssl1.1     libdb5.3     libpcre3     libedit2     libgeos-c1v5     libspatialindex4v5     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient18 &&     rm -rf /var/lib/apt/lists/*
# Wed, 13 Sep 2017 21:30:22 GMT
RUN SWIPL_VER=7.5.15 &&     SWIPL_CHECKSUM=aca07ce9c564e608586e7ae7b9a56c82ca5dd919cde1a1edf1121efa16bda568 &&     BUILD_DEPS='make gcc wget libarchive-dev libgmp-dev libossp-uuid-dev libpcre3-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev libgeos-dev libspatialindex-dev unixodbc-dev' &&     apt-get update && apt-get install -y --no-install-recommends $BUILD_DEPS &&     mkdir /tmp/src &&     cd /tmp/src &&     wget http://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz &&     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM &&     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM &&     tar -xzf swipl-$SWIPL_VER.tar.gz &&     cd swipl-$SWIPL_VER &&     cp build.templ build &&     sed -i '/PREFIX=$HOME/c\PREFIX=/swipl' build &&     sed -i '/# export DISABLE_PKGS/c\export DISABLE_PKGS="jpl xpce"' build &&     sed -i '/# export EXTRA_PKGS/c\export EXTRA_PKGS="db space"' build &&     chmod u+x build && ./build &&     apt-get purge -y --auto-remove $BUILD_DEPS &&     cd /usr/bin && rm -rf /tmp/src && ln -s /swipl/bin/swipl swipl && rm -rf /var/lib/apt/lists/*
# Wed, 13 Sep 2017 21:30:23 GMT
ENV LANG=C.UTF-8
# Wed, 13 Sep 2017 21:30:23 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:afeb2bfd31c0760573e7262de6ae67a84da0e0a1c3e8157bbddd41a501b18a5c`  
		Last Modified: Thu, 07 Sep 2017 23:21:35 GMT  
		Size: 22.5 MB (22488057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67aa1f6eaa9c07a4bbe9bff22dcf3000f0a8361615de82ffbe8d4db9afea29d8`  
		Last Modified: Wed, 13 Sep 2017 21:30:39 GMT  
		Size: 22.0 MB (22014782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:186f3c3f81eb186c68631fdd4724c0aa22a60969ff2b1b823259e821a448362b`  
		Last Modified: Wed, 13 Sep 2017 21:30:37 GMT  
		Size: 6.5 MB (6479831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `swipl:latest`

```console
$ docker pull swipl@sha256:942f751fa64ea7e9860c23ab41e78d0d1483025371e5c5a6f475bc34f2f0f8fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `swipl:latest` - linux; amd64

```console
$ docker pull swipl@sha256:5528e123c3d843df126f3989ee209c121f84d01f4f583bce366499de6e2cbbe4
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50982670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ba25ea612793e78526f21f481ed6c56080483f65182715c05021aea7a6524a`
-	Default Command: `["swipl"]`

```dockerfile
# Wed, 13 Sep 2017 08:41:48 GMT
ADD file:2bc9df54d28d9ec75722f6748834a1aea0baf089047e86a541064c282246c300 in / 
# Wed, 13 Sep 2017 08:41:49 GMT
CMD ["bash"]
# Wed, 13 Sep 2017 21:28:38 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Wed, 13 Sep 2017 21:28:51 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libarchive13     libgmp10     libossp-uuid16     libssl1.1     libdb5.3     libpcre3     libedit2     libgeos-c1v5     libspatialindex4v5     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient18 &&     rm -rf /var/lib/apt/lists/*
# Wed, 13 Sep 2017 21:30:22 GMT
RUN SWIPL_VER=7.5.15 &&     SWIPL_CHECKSUM=aca07ce9c564e608586e7ae7b9a56c82ca5dd919cde1a1edf1121efa16bda568 &&     BUILD_DEPS='make gcc wget libarchive-dev libgmp-dev libossp-uuid-dev libpcre3-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev libgeos-dev libspatialindex-dev unixodbc-dev' &&     apt-get update && apt-get install -y --no-install-recommends $BUILD_DEPS &&     mkdir /tmp/src &&     cd /tmp/src &&     wget http://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz &&     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM &&     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM &&     tar -xzf swipl-$SWIPL_VER.tar.gz &&     cd swipl-$SWIPL_VER &&     cp build.templ build &&     sed -i '/PREFIX=$HOME/c\PREFIX=/swipl' build &&     sed -i '/# export DISABLE_PKGS/c\export DISABLE_PKGS="jpl xpce"' build &&     sed -i '/# export EXTRA_PKGS/c\export EXTRA_PKGS="db space"' build &&     chmod u+x build && ./build &&     apt-get purge -y --auto-remove $BUILD_DEPS &&     cd /usr/bin && rm -rf /tmp/src && ln -s /swipl/bin/swipl swipl && rm -rf /var/lib/apt/lists/*
# Wed, 13 Sep 2017 21:30:23 GMT
ENV LANG=C.UTF-8
# Wed, 13 Sep 2017 21:30:23 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:afeb2bfd31c0760573e7262de6ae67a84da0e0a1c3e8157bbddd41a501b18a5c`  
		Last Modified: Thu, 07 Sep 2017 23:21:35 GMT  
		Size: 22.5 MB (22488057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67aa1f6eaa9c07a4bbe9bff22dcf3000f0a8361615de82ffbe8d4db9afea29d8`  
		Last Modified: Wed, 13 Sep 2017 21:30:39 GMT  
		Size: 22.0 MB (22014782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:186f3c3f81eb186c68631fdd4724c0aa22a60969ff2b1b823259e821a448362b`  
		Last Modified: Wed, 13 Sep 2017 21:30:37 GMT  
		Size: 6.5 MB (6479831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
