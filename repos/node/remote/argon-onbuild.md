## `node:argon-onbuild`

```console
$ docker pull node@sha256:858453c438fc4b3f043c3e5f8e953d98b0fe88f41ff56f3777985f7b8998a4e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `node:argon-onbuild` - linux; amd64

```console
$ docker pull node@sha256:b4e5de700bdec82728fcc20250be9bec8da39235d0a11850e5d15d6e3503735c
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.2 MB (263179584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90f1c02b11ed1950754aac3087f54fe86cd698a593a641b9fd9be0b83bd8f7bc`
-	Default Command: `["npm","start"]`

```dockerfile
# Wed, 13 Sep 2017 08:40:43 GMT
ADD file:d7333b3e0bc6479d2faed32e06d85f1975e5b23e13e75555aeed0f639770413b in / 
# Wed, 13 Sep 2017 08:40:43 GMT
CMD ["bash"]
# Wed, 13 Sep 2017 12:32:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Sep 2017 12:32:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Sep 2017 12:33:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Sep 2017 12:34:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 13 Sep 2017 20:05:31 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 13 Sep 2017 20:05:35 GMT
RUN set -ex   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     56730D5401028683275BD23C23EFEFE93C4CFFFE   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done
# Wed, 13 Sep 2017 20:05:35 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Wed, 13 Sep 2017 20:38:53 GMT
ENV NODE_VERSION=4.8.4
# Wed, 13 Sep 2017 20:38:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Wed, 13 Sep 2017 20:38:57 GMT
ENV YARN_VERSION=0.24.4
# Wed, 13 Sep 2017 20:39:13 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt/yarn   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/yarn --strip-components=1   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Wed, 13 Sep 2017 20:39:13 GMT
CMD ["node"]
# Wed, 13 Sep 2017 20:46:40 GMT
RUN mkdir -p /usr/src/app
# Wed, 13 Sep 2017 20:46:40 GMT
WORKDIR /usr/src/app
# Wed, 13 Sep 2017 20:46:40 GMT
ONBUILD ARG NODE_ENV
# Wed, 13 Sep 2017 20:46:41 GMT
ONBUILD ENV NODE_ENV $NODE_ENV
# Wed, 13 Sep 2017 20:46:41 GMT
ONBUILD COPY package.json /usr/src/app/
# Wed, 13 Sep 2017 20:46:41 GMT
ONBUILD RUN npm install && npm cache clean --force
# Wed, 13 Sep 2017 20:46:41 GMT
ONBUILD COPY . /usr/src/app
# Wed, 13 Sep 2017 20:46:41 GMT
CMD ["npm" "start"]
```

-	Layers:
	-	`sha256:aa18ad1a0d334d80981104c599fa8cef9264552a265b1197af11274beba767cf`  
		Last Modified: Thu, 07 Sep 2017 23:11:06 GMT  
		Size: 52.6 MB (52595547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a33158a1367c7c4103c89ae66e8f4fdec4ada6a39d4648cf254b32296d6668`  
		Last Modified: Wed, 13 Sep 2017 12:54:21 GMT  
		Size: 19.3 MB (19263717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67323742a64d3540e24632f6d77dfb02e72301c00d1e9a3c28e0ef15478fff9`  
		Last Modified: Wed, 13 Sep 2017 12:54:47 GMT  
		Size: 43.2 MB (43227774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b45e832c38de44fbab83d5fcf9cbf66d069a51e6462d89ccc050051f25926d`  
		Last Modified: Wed, 13 Sep 2017 12:55:22 GMT  
		Size: 134.7 MB (134684500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f83e14495c19e0bb1c7187b76571e3c6a2125dae2926678da165cfc6c7da0670`  
		Last Modified: Wed, 13 Sep 2017 20:47:50 GMT  
		Size: 4.4 KB (4423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41fea39113bff896d196a20e0d032c7535e6a6239b3ce1d9c7749a092794c50e`  
		Last Modified: Wed, 13 Sep 2017 20:47:50 GMT  
		Size: 119.2 KB (119150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:987d370e5cb9ff61b42888c94e84751a670a0651835e9b6f819c6e5a51859cb4`  
		Last Modified: Wed, 13 Sep 2017 20:53:04 GMT  
		Size: 12.4 MB (12383622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac2ecf3399179c624f27ef031cd8e3c38c5a3ad8c12011abb837b50e4154ae69`  
		Last Modified: Wed, 13 Sep 2017 20:53:00 GMT  
		Size: 900.7 KB (900722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f77e731c71cfa9574e10b92145170c43f066320dfb49190f0ec5317554c7dbd1`  
		Last Modified: Wed, 13 Sep 2017 20:53:46 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `node:argon-onbuild` - linux; arm variant v7

```console
$ docker pull node@sha256:ac7c9be3f66a2ef9cc49ed10a4b904325fea0cc5971c25f2eebe52b5dbbc9ad5
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233168928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42a1bd7a42c716962cd85123d776a7c1e3bdcc2da3250adfe9aaaaf59f7e58e5`
-	Default Command: `["npm","start"]`

```dockerfile
# Sat, 09 Sep 2017 01:40:17 GMT
ADD file:ef59ce7fe68882b1b44bc3c4a5e9e465561cb257fb63f8c2b3c247abb012486b in / 
# Sat, 09 Sep 2017 01:40:18 GMT
CMD ["bash"]
# Tue, 19 Sep 2017 00:33:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Sep 2017 00:33:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 19 Sep 2017 00:45:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Sep 2017 00:59:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 27 Sep 2017 02:06:11 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 27 Sep 2017 02:06:13 GMT
RUN set -ex   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     56730D5401028683275BD23C23EFEFE93C4CFFFE   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done
# Wed, 27 Sep 2017 02:06:13 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Wed, 27 Sep 2017 02:09:23 GMT
ENV NODE_VERSION=4.8.4
# Wed, 27 Sep 2017 02:09:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Wed, 27 Sep 2017 02:09:27 GMT
ENV YARN_VERSION=0.24.4
# Wed, 27 Sep 2017 02:09:30 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt/yarn   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/yarn --strip-components=1   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Wed, 27 Sep 2017 02:09:30 GMT
CMD ["node"]
# Wed, 27 Sep 2017 02:09:35 GMT
RUN mkdir -p /usr/src/app
# Wed, 27 Sep 2017 02:09:35 GMT
WORKDIR /usr/src/app
# Wed, 27 Sep 2017 02:09:35 GMT
ONBUILD ARG NODE_ENV
# Wed, 27 Sep 2017 02:09:35 GMT
ONBUILD ENV NODE_ENV $NODE_ENV
# Wed, 27 Sep 2017 02:09:36 GMT
ONBUILD COPY package.json /usr/src/app/
# Wed, 27 Sep 2017 02:09:36 GMT
ONBUILD RUN npm install && npm cache clean --force
# Wed, 27 Sep 2017 02:09:36 GMT
ONBUILD COPY . /usr/src/app
# Wed, 27 Sep 2017 02:09:36 GMT
CMD ["npm" "start"]
```

-	Layers:
	-	`sha256:e925dd4ffa2a7ffdc23dbce8d2b25866e687204da4ed5a664a51d787e32366d4`  
		Last Modified: Sat, 09 Sep 2017 01:50:36 GMT  
		Size: 48.7 MB (48682076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9bfbf7dfc788cb4ca7c7d227e3465a4e211416e4c7f0e008f3ae90db3dd0bb1`  
		Last Modified: Tue, 19 Sep 2017 02:40:07 GMT  
		Size: 18.3 MB (18262683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015138dd660daf8e5560cc269a592e9abf2796753a8c7d62949428056b7d1917`  
		Last Modified: Tue, 19 Sep 2017 02:40:50 GMT  
		Size: 39.7 MB (39689147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d88b2b5023e5b605d9611426b7cc69289141483394d1d1de9ab3773fcb770ffd`  
		Last Modified: Tue, 19 Sep 2017 02:42:03 GMT  
		Size: 113.8 MB (113804084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deae817d6d1e9419731b41c13415d25f5eb9576a8e186b73d3b94f5e8700fbc8`  
		Last Modified: Wed, 27 Sep 2017 07:20:01 GMT  
		Size: 4.4 KB (4442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767ba576e67d4444631ff89becca10dd658872ef2c062f4601dcb2142fb3e6e2`  
		Last Modified: Wed, 27 Sep 2017 07:20:01 GMT  
		Size: 119.2 KB (119183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a889f014528170dbea5c2101c5c61fb81a8e663a25ee00f9fb7e27dd6db1e35c`  
		Last Modified: Wed, 27 Sep 2017 07:22:48 GMT  
		Size: 11.7 MB (11704755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ec6b0393d973608df5bf68d90b541da6743689988ec8bd2bdeb85655f95b68`  
		Last Modified: Wed, 27 Sep 2017 07:22:45 GMT  
		Size: 902.4 KB (902393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15348d37f55e89ca26e5670ce05964c9d35c2566bcdb03737de49be76960bcc2`  
		Last Modified: Wed, 27 Sep 2017 07:23:01 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `node:argon-onbuild` - linux; arm64 variant v8

```console
$ docker pull node@sha256:f23dc126c93b3c148905970f0a57a2e684ffb98ac46536f2f64ef26aa35a144f
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.7 MB (238724265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2051f73d9882bdac5dddb28809c71a7969447ae0d794a0d5daa8258900170850`
-	Default Command: `["npm","start"]`

```dockerfile
# Fri, 08 Sep 2017 17:23:41 GMT
ADD file:9f576a63a5e03994904e585c35fbeef6a2c96c41d8f696705c033f3ca69b6a2b in / 
# Fri, 08 Sep 2017 17:23:42 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 18:32:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 08 Sep 2017 18:32:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 08 Sep 2017 18:34:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 08 Sep 2017 18:42:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 Sep 2017 23:15:11 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 14 Sep 2017 23:15:16 GMT
RUN set -ex   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     56730D5401028683275BD23C23EFEFE93C4CFFFE   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done
# Thu, 14 Sep 2017 23:15:17 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Thu, 14 Sep 2017 23:20:26 GMT
ENV NODE_VERSION=4.8.4
# Thu, 14 Sep 2017 23:20:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Thu, 14 Sep 2017 23:20:35 GMT
ENV YARN_VERSION=0.24.4
# Thu, 14 Sep 2017 23:20:40 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt/yarn   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/yarn --strip-components=1   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Thu, 14 Sep 2017 23:20:40 GMT
CMD ["node"]
# Thu, 14 Sep 2017 23:20:59 GMT
RUN mkdir -p /usr/src/app
# Thu, 14 Sep 2017 23:21:00 GMT
WORKDIR /usr/src/app
# Thu, 14 Sep 2017 23:21:01 GMT
ONBUILD ARG NODE_ENV
# Thu, 14 Sep 2017 23:21:01 GMT
ONBUILD ENV NODE_ENV $NODE_ENV
# Thu, 14 Sep 2017 23:21:02 GMT
ONBUILD COPY package.json /usr/src/app/
# Thu, 14 Sep 2017 23:21:03 GMT
ONBUILD RUN npm install && npm cache clean --force
# Thu, 14 Sep 2017 23:21:03 GMT
ONBUILD COPY . /usr/src/app
# Thu, 14 Sep 2017 23:21:04 GMT
CMD ["npm" "start"]
```

-	Layers:
	-	`sha256:e91a355b0d3ff86add037a3f24718b760d8eb3f346f998e5116375ddce9eae19`  
		Last Modified: Fri, 08 Sep 2017 17:34:56 GMT  
		Size: 49.9 MB (49929457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e054bfb02234c6e2b5305981d365c3b31101ec460b0d90df3b099305c03196`  
		Last Modified: Thu, 14 Sep 2017 22:01:15 GMT  
		Size: 18.7 MB (18737603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:498121800d24d5e5d3f5d851e16ca4b4b663cabd018a246961dca07ae046f06b`  
		Last Modified: Thu, 14 Sep 2017 22:01:47 GMT  
		Size: 41.0 MB (40988522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39f6cc0761da5c1bc61d59c5cbe9188f22bc173d6f1038d6cccf1292f0b79594`  
		Last Modified: Thu, 14 Sep 2017 22:02:40 GMT  
		Size: 115.6 MB (115645790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e1c39f6211afa1ec35415a706445f6f61932d2a6e3cc38ea4c8b64d0ae93214`  
		Last Modified: Thu, 14 Sep 2017 23:22:52 GMT  
		Size: 4.4 KB (4430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d483c0d001abebdcac8fc0fd63a2d9ff8886f54b13738ca199e2ad80d9706ba`  
		Last Modified: Thu, 14 Sep 2017 23:22:53 GMT  
		Size: 119.1 KB (119147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2335953e1e987cc9e125613f01a0c39bbc30ba0dcea4ed5c5d4ab71c24d580c`  
		Last Modified: Thu, 14 Sep 2017 23:29:19 GMT  
		Size: 12.4 MB (12396823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4877bff69b8bce4b9dbae0416030dab0e665a51a8e41c558e13b018cd923e93`  
		Last Modified: Thu, 14 Sep 2017 23:29:14 GMT  
		Size: 902.4 KB (902361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb7469d259bf15f125e5cee5e6642c2ee89bb8d5f41c83d124e53dee2ba22b0`  
		Last Modified: Thu, 14 Sep 2017 23:29:57 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `node:argon-onbuild` - linux; ppc64le

```console
$ docker pull node@sha256:4e2fe72b75868f3fc0f2b71aa6cf5e36923f6ea93f6ed11ef8643f3c2f818925
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.7 MB (249658608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e459b46f06ec5b51bfbe5017619ebe1f89bf155f64f5ca643c4f7b2ff31a0a2e`
-	Default Command: `["npm","start"]`

```dockerfile
# Fri, 08 Sep 2017 00:32:21 GMT
ADD file:483b3245941140ac32394a804364a1a9bd5dfdf1b4475238b61068cc7252ac08 in / 
# Fri, 08 Sep 2017 00:32:21 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 01:03:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 08 Sep 2017 01:03:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 08 Sep 2017 01:04:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 08 Sep 2017 01:05:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 Sep 2017 23:08:37 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 14 Sep 2017 23:09:02 GMT
RUN set -ex   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     56730D5401028683275BD23C23EFEFE93C4CFFFE   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done
# Thu, 14 Sep 2017 23:09:13 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Thu, 14 Sep 2017 23:17:53 GMT
ENV NODE_VERSION=4.8.4
# Thu, 14 Sep 2017 23:18:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Thu, 14 Sep 2017 23:18:04 GMT
ENV YARN_VERSION=0.24.4
# Thu, 14 Sep 2017 23:18:11 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt/yarn   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/yarn --strip-components=1   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Thu, 14 Sep 2017 23:18:14 GMT
CMD ["node"]
# Thu, 14 Sep 2017 23:18:29 GMT
RUN mkdir -p /usr/src/app
# Thu, 14 Sep 2017 23:18:31 GMT
WORKDIR /usr/src/app
# Thu, 14 Sep 2017 23:18:33 GMT
ONBUILD ARG NODE_ENV
# Thu, 14 Sep 2017 23:18:35 GMT
ONBUILD ENV NODE_ENV $NODE_ENV
# Thu, 14 Sep 2017 23:18:37 GMT
ONBUILD COPY package.json /usr/src/app/
# Thu, 14 Sep 2017 23:18:39 GMT
ONBUILD RUN npm install && npm cache clean --force
# Thu, 14 Sep 2017 23:18:40 GMT
ONBUILD COPY . /usr/src/app
# Thu, 14 Sep 2017 23:18:42 GMT
CMD ["npm" "start"]
```

-	Layers:
	-	`sha256:d4a5434e09b7ac8431060d347d6ef1233ae07514878fb2aff4085bcf441c29f3`  
		Last Modified: Fri, 08 Sep 2017 00:36:52 GMT  
		Size: 51.8 MB (51809570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48596af2c38701f94440e222bf8f3d4b2da85e2982c97ae15186eba523249e0b`  
		Last Modified: Thu, 14 Sep 2017 22:21:02 GMT  
		Size: 19.2 MB (19199596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb50d2f41608755ef40ba4bd126fcb6e790d99a751079c32edae61c9ebad7a9`  
		Last Modified: Thu, 14 Sep 2017 22:21:29 GMT  
		Size: 42.7 MB (42728149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ade55670af5d621ffaed3b528ca5af97655b36bfbe022557861d40a4f00be68`  
		Last Modified: Thu, 14 Sep 2017 22:22:15 GMT  
		Size: 122.7 MB (122728339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9130116f09fbee7119a1f60781edca63f523f17f68b96b02f92876de828bc3e0`  
		Last Modified: Thu, 14 Sep 2017 23:21:02 GMT  
		Size: 4.5 KB (4462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f1b17b448c3228dbbcb238225e06b01f9628422332c123d47946e3517b1d923`  
		Last Modified: Thu, 14 Sep 2017 23:21:02 GMT  
		Size: 119.2 KB (119188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f44c5a4f9a9ea1ba94e0b0a5c76db4983b1ad49c2c97b6c3da1aed05426d0783`  
		Last Modified: Thu, 14 Sep 2017 23:28:30 GMT  
		Size: 12.2 MB (12166753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:150ebd07e22f241f369d710b4b23a0c8b6353f54b705330d652f40eb8ac14480`  
		Last Modified: Thu, 14 Sep 2017 23:28:24 GMT  
		Size: 902.4 KB (902387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ac1a0c7073081be0e6b34f6d60ede9258d41d58aa7e337857d551f76e6381e`  
		Last Modified: Thu, 14 Sep 2017 23:29:13 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
