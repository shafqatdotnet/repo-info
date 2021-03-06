## `orientdb:latest`

```console
$ docker pull orientdb@sha256:38d4bbb91d12acb34389c012a77f31d0c91a52e94abe53204c9f6ca57911ff91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `orientdb:latest` - linux; amd64

```console
$ docker pull orientdb@sha256:d8534af9e4699702d37cc4746c072c88a43dc412451015f025d2e0f8eef9614b
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (116986645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a85aca354e54ce2ccf255a7dc33950f701ecdac8cb462ab1824f28253ef58e2d`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 13 Sep 2017 14:32:25 GMT
ADD file:4583e12bf5caec40b861a3409f2a1624c3f3556cc457edb99c9707f00e779e45 in / 
# Wed, 13 Sep 2017 14:32:26 GMT
CMD ["/bin/sh"]
# Thu, 14 Sep 2017 04:13:40 GMT
ENV LANG=C.UTF-8
# Thu, 14 Sep 2017 04:13:41 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 14 Sep 2017 04:21:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8-openjdk
# Thu, 14 Sep 2017 04:21:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Thu, 14 Sep 2017 04:21:31 GMT
ENV JAVA_VERSION=8u131
# Thu, 14 Sep 2017 04:21:31 GMT
ENV JAVA_ALPINE_VERSION=8.131.11-r2
# Thu, 14 Sep 2017 04:21:39 GMT
RUN set -x 	&& apk add --no-cache 		openjdk8="$JAVA_ALPINE_VERSION" 	&& [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 14 Sep 2017 06:40:32 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 14 Sep 2017 06:40:43 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 26 Sep 2017 17:44:10 GMT
ENV ORIENTDB_VERSION=2.2.28
# Tue, 26 Sep 2017 17:44:10 GMT
ENV ORIENTDB_DOWNLOAD_MD5=631c866d91c43efa80354b1949c2502d
# Tue, 26 Sep 2017 17:44:10 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=8d773792d534c50c3c90657cc02a0d8ffa436f3a
# Tue, 26 Sep 2017 17:44:10 GMT
ENV ORIENTDB_DOWNLOAD_URL=http://central.maven.org/maven2/com/orientechnologies/orientdb-community/2.2.28/orientdb-community-2.2.28.tar.gz
# Tue, 26 Sep 2017 17:44:14 GMT
RUN apk add --update tar curl     && rm -rf /var/cache/apk/*
# Tue, 26 Sep 2017 17:44:17 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Tue, 26 Sep 2017 17:44:17 GMT
ENV PATH=/orientdb/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Tue, 26 Sep 2017 17:44:17 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 26 Sep 2017 17:44:17 GMT
WORKDIR /orientdb
# Tue, 26 Sep 2017 17:44:18 GMT
EXPOSE 2424/tcp
# Tue, 26 Sep 2017 17:44:18 GMT
EXPOSE 2480/tcp
# Tue, 26 Sep 2017 17:44:18 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:88286f41530e93dffd4b964e1db22ce4939fffa4a4c665dab8591fbab03d4926`  
		Last Modified: Tue, 27 Jun 2017 18:49:37 GMT  
		Size: 2.0 MB (1990402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720349d0916a74fb5124be4a8a2bf898de431927e1caec15cc956c8a7fb33d14`  
		Last Modified: Thu, 14 Sep 2017 04:50:44 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42a4b3080d3cc157970baf6edf6194df12fa0a9dc61d2c1525781ae4af65213c`  
		Last Modified: Thu, 14 Sep 2017 04:59:04 GMT  
		Size: 70.1 MB (70051361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5cbf95a9a95f072beac83db8315f1298bf6835f32253cbb25e21cb78e59d02d`  
		Last Modified: Tue, 26 Sep 2017 17:44:37 GMT  
		Size: 649.4 KB (649436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a15e951399d4e5e3fc1a426eb135eb1f660e32694529dd5f3f9de3fdfaef04e4`  
		Last Modified: Tue, 26 Sep 2017 17:44:42 GMT  
		Size: 44.3 MB (44295206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
