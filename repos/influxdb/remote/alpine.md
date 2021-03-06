## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:c7f2ef94ddb6d6f5498c08ff821405f87b8e0a8cc457ed9823e97de240bec328
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:00269b4a721b2081c63aefe1c6279ed6556c1a721b5f41f1e737f29a8f0edc34
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17531349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c69353f509f7d26d797a8fdd4f95ad8ddc238a0963792df58291122604dc9792`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 13 Sep 2017 14:32:20 GMT
ADD file:9d67752278c0e5a1298cd2d6603ebaaab2aa342e27ddf191ee0fde138f82698c in / 
# Wed, 13 Sep 2017 14:32:20 GMT
CMD ["/bin/sh"]
# Wed, 13 Sep 2017 15:12:34 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 13 Sep 2017 22:30:12 GMT
RUN apk add --no-cache tzdata bash
# Wed, 13 Sep 2017 22:30:13 GMT
ENV INFLUXDB_VERSION=1.3.5
# Wed, 13 Sep 2017 22:34:45 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar ca-certificates &&     update-ca-certificates &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget -q https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget -q https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 13 Sep 2017 22:34:45 GMT
COPY file:3ee2bc0321c2aa2451df7a508649c3a54f0eebc1ef9b8a24967c58105b4d3160 in /etc/influxdb/influxdb.conf 
# Wed, 13 Sep 2017 22:34:45 GMT
EXPOSE 8086/tcp
# Wed, 13 Sep 2017 22:34:45 GMT
VOLUME [/var/lib/influxdb]
# Thu, 14 Sep 2017 21:42:46 GMT
COPY file:098affa3d1b749dacb263ddacfd86a5de1f598d6ba1f7c789ce482c66ee9c80b in /entrypoint.sh 
# Thu, 14 Sep 2017 21:42:46 GMT
COPY file:cca8e5bdb025c728ca8521b015ace9545c2552d075f4c92d7345294a6f1371c2 in /init-influxdb.sh 
# Thu, 14 Sep 2017 21:42:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 14 Sep 2017 21:42:47 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:019300c8a437a2d60248f27c206795930626dfe7ddc0323d734143bd5eb131a6`  
		Last Modified: Tue, 27 Jun 2017 18:48:47 GMT  
		Size: 2.0 MB (1970271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f86ea3a05bc091d3d70e7de3d61d06e961eaeb967c4e0c6060196f0dcdc42f`  
		Last Modified: Wed, 13 Sep 2017 15:14:01 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8923a00959f4dc85fa50ee5a6a0e8d2aaf46212a75fd83bb66b00c8b831792b`  
		Last Modified: Wed, 13 Sep 2017 22:35:59 GMT  
		Size: 1.5 MB (1483392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fdc84a9d1719ae42fd2b0f4a349ee15d7bc819b330435ba1128c72bbb8d6bb`  
		Last Modified: Wed, 13 Sep 2017 22:36:01 GMT  
		Size: 14.1 MB (14075955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b515c90d63290abe9dba1a660e83aafe3433da2b2c6cbd0ef815fc146d06140f`  
		Last Modified: Wed, 13 Sep 2017 22:35:58 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c24753b7c9ed320d168e74894807d6258956faabc54f8c38470ce9ba9e075701`  
		Last Modified: Thu, 14 Sep 2017 21:43:09 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b51749b67631d4347ba1bcf2a0a84c2af51bd6f696b6b261b4e155fa529f287`  
		Last Modified: Thu, 14 Sep 2017 21:43:09 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
