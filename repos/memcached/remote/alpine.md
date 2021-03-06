## `memcached:alpine`

```console
$ docker pull memcached@sha256:e0c1507744732ca960e1dbc61b6dc875c10747df89686a3e054ed2e460152dbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `memcached:alpine` - linux; amd64

```console
$ docker pull memcached@sha256:ddc1c87ea6492c876090bb00621081396739849a2a3431a1ad50dd97620c7b26
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3724751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b07c181167cf8ce9e7637254d4c9d89d1d06bbb76e4e3def6516cffecdbd8ee8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Sep 2017 14:32:25 GMT
ADD file:4583e12bf5caec40b861a3409f2a1624c3f3556cc457edb99c9707f00e779e45 in / 
# Wed, 13 Sep 2017 14:32:26 GMT
CMD ["/bin/sh"]
# Tue, 19 Sep 2017 01:41:38 GMT
RUN adduser -D memcache
# Tue, 19 Sep 2017 01:41:38 GMT
ENV MEMCACHED_VERSION=1.5.1
# Tue, 19 Sep 2017 01:41:38 GMT
ENV MEMCACHED_SHA1=e5b7e4e562eb99fdfa67d71697cc6744d3e9663f
# Tue, 26 Sep 2017 00:34:44 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		libressl 		linux-headers 		make 		perl 		perl-utils 		tar 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --virtual .memcached-rundeps $runDeps 	&& apk del .build-deps 		&& memcached -V
# Tue, 26 Sep 2017 00:34:45 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Tue, 26 Sep 2017 00:34:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 26 Sep 2017 00:34:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Sep 2017 00:34:46 GMT
USER [memcache]
# Tue, 26 Sep 2017 00:34:46 GMT
EXPOSE 11211/tcp
# Tue, 26 Sep 2017 00:34:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:88286f41530e93dffd4b964e1db22ce4939fffa4a4c665dab8591fbab03d4926`  
		Last Modified: Tue, 27 Jun 2017 18:49:37 GMT  
		Size: 2.0 MB (1990402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5342366c11be2dc0ad25a1e84eedb96da23a1d63c55378df80d256b737b91664`  
		Last Modified: Tue, 19 Sep 2017 01:45:30 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ff1fef820cf8902240b14b41e441d646f950ee1335d35b5ea39904a15e330b`  
		Last Modified: Tue, 26 Sep 2017 00:34:58 GMT  
		Size: 1.7 MB (1732701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1e0218d82caf4a81831f4036c998e7ea1717bb29271bb1b6764eb6087c8b578`  
		Last Modified: Tue, 26 Sep 2017 00:34:57 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f32269145f02cb77136b545ee3234d319e783bca5f1e4091bdbad0be45c573`  
		Last Modified: Tue, 26 Sep 2017 00:34:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
