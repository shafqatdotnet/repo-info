## `jetty:jre8-alpine`

```console
$ docker pull jetty@sha256:125317488d0d9437a16ff8fc576dc432b9f1746afd9a88f20ccb9155724b84bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `jetty:jre8-alpine` - linux; amd64

```console
$ docker pull jetty@sha256:d324459ed07476c4bb2572830e0fa8e63e730714c5fab24bee79a2d1ea4c3f4b
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.4 MB (64408870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:222474a285e55f4a1ee2f3cb4bcaa396f539f43fac1bd871e1d1f187a68e430b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 13 Sep 2017 14:32:25 GMT
ADD file:4583e12bf5caec40b861a3409f2a1624c3f3556cc457edb99c9707f00e779e45 in / 
# Wed, 13 Sep 2017 14:32:26 GMT
CMD ["/bin/sh"]
# Thu, 14 Sep 2017 04:13:40 GMT
ENV LANG=C.UTF-8
# Thu, 14 Sep 2017 04:13:41 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 14 Sep 2017 04:25:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8-openjdk/jre
# Thu, 14 Sep 2017 04:25:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Thu, 14 Sep 2017 04:25:34 GMT
ENV JAVA_VERSION=8u131
# Thu, 14 Sep 2017 04:25:34 GMT
ENV JAVA_ALPINE_VERSION=8.131.11-r2
# Thu, 14 Sep 2017 04:25:42 GMT
RUN set -x 	&& apk add --no-cache 		openjdk8-jre="$JAVA_ALPINE_VERSION" 	&& [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 14 Sep 2017 06:34:23 GMT
RUN addgroup -S jetty && adduser -D -S -H -G jetty jetty && rm -rf /etc/group- /etc/passwd- /etc/shadow-
# Thu, 14 Sep 2017 06:34:23 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 14 Sep 2017 06:34:23 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Thu, 14 Sep 2017 06:34:24 GMT
RUN mkdir -p "$JETTY_HOME"
# Thu, 14 Sep 2017 06:34:24 GMT
WORKDIR /usr/local/jetty
# Wed, 27 Sep 2017 17:32:35 GMT
ENV JETTY_VERSION=9.4.7.v20170914
# Wed, 27 Sep 2017 17:32:39 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.7.v20170914/jetty-home-9.4.7.v20170914.tar.gz
# Wed, 27 Sep 2017 17:32:39 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Wed, 27 Sep 2017 17:32:48 GMT
RUN set -xe 	&& apk add --no-cache --virtual .build-deps gnupg curl 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& rm -rf "$GNUPGHOME" 	&& tar -xvzf jetty.tar.gz 	&& mv jetty-home-$JETTY_VERSION/* ./ 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm jetty.tar.gz* 	&& rm -fr jetty-home-$JETTY_VERSION/ 	&& apk del .build-deps 	&& rm -fr .build-deps 	&& rm -rf /tmp/hsperfdata_root
# Wed, 27 Sep 2017 17:32:48 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 27 Sep 2017 17:32:48 GMT
RUN mkdir -p "$JETTY_BASE"
# Wed, 27 Sep 2017 17:32:52 GMT
WORKDIR /var/lib/jetty
# Wed, 27 Sep 2017 17:32:55 GMT
RUN set -xe 	&& java -jar "$JETTY_HOME/start.jar" --create-startd --add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Wed, 27 Sep 2017 17:32:58 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 27 Sep 2017 17:32:59 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Wed, 27 Sep 2017 17:32:59 GMT
COPY file:b8e6879a89749d0470df589adc6fc0c92de046b29500c0ffa05439a19d44f877 in / 
# Wed, 27 Sep 2017 17:33:00 GMT
USER [jetty]
# Wed, 27 Sep 2017 17:33:00 GMT
EXPOSE 8080/tcp
# Wed, 27 Sep 2017 17:33:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 27 Sep 2017 17:33:00 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
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
	-	`sha256:9431a0557160e1ec384a6cfe37d1225528bd236e486010ffc0b75ce7fe1c1465`  
		Last Modified: Thu, 14 Sep 2017 05:01:46 GMT  
		Size: 54.3 MB (54282902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c06a80de3d5787f6cca2d50523aef3b705e3852fcb9c307864b15507f0ab574c`  
		Last Modified: Thu, 14 Sep 2017 06:37:07 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:735305afaaeb1d7d4aa52cb629fe5146d853c0f13c186ba8537013a812c69dfd`  
		Last Modified: Thu, 14 Sep 2017 06:37:07 GMT  
		Size: 140.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720298d80affa12846d2370447333da06fdd7c6b13da0d4aaa7e3004db2bd8eb`  
		Last Modified: Wed, 27 Sep 2017 17:34:27 GMT  
		Size: 8.1 MB (8130541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61cfb2815f00c6361f4dc92a2e4e3915a077fe2fb17b5f7f805ee68927f9e332`  
		Last Modified: Wed, 27 Sep 2017 17:34:25 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d76824349199d959e2448016894ab5152be2132f554526bf18881d066db10b`  
		Last Modified: Wed, 27 Sep 2017 17:34:25 GMT  
		Size: 2.1 KB (2070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbebf2b5b108ae1ff5c1cab97ce8922af7ff64517f9d12434a3cef4cb161d2f0`  
		Last Modified: Wed, 27 Sep 2017 17:34:25 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef321e856089c1c0849cc4738c83d9401f75ea8cf02772fd04750c3efde6b1ae`  
		Last Modified: Wed, 27 Sep 2017 17:34:25 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
