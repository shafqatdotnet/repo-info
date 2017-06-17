## `golang:rc`

```console
$ docker pull golang@sha256:787eb7ef7fcb6e6ff478f5af14381c04c4bb250d956889aac4ab94de3395e1eb
```

-	Platforms:
	-	linux; amd64

### `golang:rc` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.3 MB (259323002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f956aead4d7071c5ae33843d5a6f566174e642f35090d8c1d9b473a4aba2f8a1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 07 Jun 2017 17:49:26 GMT
ADD file:212fe5c6a3f3d10b0f5fc59f2019d5a12f266ff74b289f3ccc87bb878b01a437 in / 
# Wed, 07 Jun 2017 17:49:27 GMT
CMD ["bash"]
# Wed, 07 Jun 2017 19:42:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 07 Jun 2017 19:44:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 08 Jun 2017 05:48:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Jun 2017 17:28:45 GMT
ENV GOLANG_VERSION=1.9beta1
# Fri, 16 Jun 2017 01:02:45 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='85719a2c704ad1352052e185c760d7c65b9d8a18b491287a7e5f6775ccc27d3b' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='26eb517a72bd0e9b1bc7f24ea52ded1991c72e09cd876c9747641c193c734cdc' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='d6877ab02d9133a51925861af2db76faabe33146ed87225450fd56c6535088ab' ;; 		i386) goRelArch='linux-386'; goRelSha256='af9fbef65761c03ee101eb23e1d1a673734c82b50546fed95710a6b04fe52995' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='8708e49428d493d07ce71f09b31b720ff8c8fe469698cd5e9f44f088c1ef75da' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='c16f86dd69bf282ca4bba60a6449130c5c0d988917d0c1f9d62a5e2fd5191a83' ;; 		*) goRelArch='src'; goRelSha256='e42dbd2071aadb28a4d293225b04b6b4215a35a7f04417a0e47ffa38f81d642d'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url"; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		echo >&2; 		echo >&2 'error: UNIMPLEMENTED'; 		echo >&2 'TODO install golang-any from jessie-backports for GOROOT_BOOTSTRAP (and uninstall after build)'; 		echo >&2; 		exit 1; 	fi; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Fri, 16 Jun 2017 01:02:46 GMT
ENV GOPATH=/go
# Fri, 16 Jun 2017 01:02:47 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2017 01:02:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 16 Jun 2017 01:02:50 GMT
WORKDIR /go
# Fri, 16 Jun 2017 01:02:51 GMT
COPY file:f6191f2c86edc9343569339f101facba47e886e33e29d70da6916ca6b1101a53 in /usr/local/bin/ 
```

-	Layers:
	-	`sha256:31a23e80b5c0100547b74b78634277f56239d4207fa7ea4f0540148525dbff03`  
		Last Modified: Wed, 07 Jun 2017 18:09:21 GMT  
		Size: 45.1 MB (45127747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5310eb3880dd8b025df521d43d0c3d3b1cebb727f0c9a297591fd50045e40ee0`  
		Last Modified: Wed, 07 Jun 2017 20:11:52 GMT  
		Size: 11.1 MB (11107732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d00f132dbb64ec781d2d4c943235a1e4cf52dd6ae86aac367e80baf5665cdd9`  
		Last Modified: Wed, 07 Jun 2017 20:12:35 GMT  
		Size: 50.9 MB (50941873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cee0d1bf54ffa777eda4e3d1a5a4cba33b8fa4a588bb515d5e0633591975c89`  
		Last Modified: Fri, 09 Jun 2017 06:24:41 GMT  
		Size: 57.2 MB (57221516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3589d54c372bda5d75e8e9625df7634163233e7415cc42943361bf3f883339f4`  
		Last Modified: Fri, 16 Jun 2017 01:03:46 GMT  
		Size: 94.9 MB (94922653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06893f3d81da12a6f8c2c040e3cae55088b756672c61ca4a31a2a20d206a0bfa`  
		Last Modified: Fri, 16 Jun 2017 01:03:28 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fb426f26b48b27a9bb56df644aa99f8ca537767e18b1a5198cc414801af5362`  
		Last Modified: Fri, 16 Jun 2017 01:03:28 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip