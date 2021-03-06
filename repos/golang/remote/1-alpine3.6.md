## `golang:1-alpine3.6`

```console
$ docker pull golang@sha256:e91ddbf20f44daeba9a9eca328bc8dbaccf790d26d017dfc572bc003f556e42d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `golang:1-alpine3.6` - linux; amd64

```console
$ docker pull golang@sha256:02059e88cd354dfa5ad4cd3b1f5095fc50466772e9a14cf04063d59b3dca0e6c
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82915242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed119d8f7db5d637bcdaab97e8f2d54c964135b469b199e8fa1a981437ea9d5b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 13 Sep 2017 14:32:25 GMT
ADD file:4583e12bf5caec40b861a3409f2a1624c3f3556cc457edb99c9707f00e779e45 in / 
# Wed, 13 Sep 2017 14:32:26 GMT
CMD ["/bin/sh"]
# Thu, 14 Sep 2017 01:36:41 GMT
RUN apk add --no-cache ca-certificates
# Thu, 14 Sep 2017 01:36:41 GMT
ENV GOLANG_VERSION=1.9
# Thu, 14 Sep 2017 01:36:41 GMT
COPY file:9c751f4a8b882686654a3b1ed338206ee5d076457c178547f59b35159e17a438 in /go-alpine-patches/ 
# Thu, 14 Sep 2017 01:37:47 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GO386="$(go env GO386)" 		GOARM="$(go env GOARM)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo 'a4ab229028ed167ba1986825751463605264e44868362ca8e7accc8be057e993 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	for p in /go-alpine-patches/*.patch; do 		[ -f "$p" ] || continue; 		patch -p2 -i "$p"; 	done; 	./make.bash; 		rm -rf /go-alpine-patches; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Thu, 14 Sep 2017 01:37:47 GMT
ENV GOPATH=/go
# Thu, 14 Sep 2017 01:37:47 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Sep 2017 01:37:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 14 Sep 2017 01:37:48 GMT
WORKDIR /go
# Thu, 14 Sep 2017 01:37:48 GMT
COPY file:ea7c9f4702f94a0df05f60648914e97f7876c4a7c5163e7870dd98fa896ff722 in /usr/local/bin/ 
```

-	Layers:
	-	`sha256:88286f41530e93dffd4b964e1db22ce4939fffa4a4c665dab8591fbab03d4926`  
		Last Modified: Tue, 27 Jun 2017 18:49:37 GMT  
		Size: 2.0 MB (1990402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f27971ac2354948abc2d3feae117482b43cedca6349218adb31ff5c234312c4`  
		Last Modified: Thu, 14 Sep 2017 01:42:33 GMT  
		Size: 351.4 KB (351354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91367c599182a81c70b9126024ceb75f258072a836df1ab3b044bcccc244dd3a`  
		Last Modified: Thu, 14 Sep 2017 01:42:30 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8577260f1836780402a8e3ee4ab30eb1d231aa92bddca883785f6a0adeb2765b`  
		Last Modified: Thu, 14 Sep 2017 01:42:54 GMT  
		Size: 80.6 MB (80571514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b99bfbf214e93ca5f973d94dac0b05924634b2cd46e5ba000cccc24811dc049`  
		Last Modified: Thu, 14 Sep 2017 01:42:30 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e21738584314b298cba18784922fac1c306c4336bb6b531e166c944bd9d7dee8`  
		Last Modified: Thu, 14 Sep 2017 01:42:30 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
