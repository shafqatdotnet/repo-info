## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:63c3dcaf680ddb23be747bfaa73b2e98b4f00bb029714947f17d9e189bf0d81c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:df0fd2dacca5540846222c2dfef10994606b70c9ec22015270fa6588a537f7a6
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.7 MB (147715630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:896a34dc4c18dc6aa52de17ab05579521e9646cf683a33d502ce746e573357ae`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

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
# Thu, 14 Sep 2017 06:36:37 GMT
RUN apk add --no-cache --quiet     bash     curl
# Thu, 14 Sep 2017 06:37:21 GMT
ENV NEO4J_SHA256=5cb4c30a257a5391dd055f5bca1df49bd9a96eb3200004550e444f01e8f9414b NEO4J_TARBALL=neo4j-enterprise-3.2.3-unix.tar.gz
# Thu, 14 Sep 2017 06:37:21 GMT
ARG NEO4J_URI=http://dist.neo4j.org/neo4j-enterprise-3.2.3-unix.tar.gz
# Thu, 14 Sep 2017 06:37:21 GMT
COPY file:2e411d607fa15f91ae6f4b515dde6bf3e158d34c0036556e00553ed1c50cd63d in /tmp/ 
# Thu, 14 Sep 2017 06:37:39 GMT
# ARGS: NEO4J_URI=http://dist.neo4j.org/neo4j-enterprise-3.2.3-unix.tar.gz
RUN curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -csw -     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* /var/lib/neo4j     && rm ${NEO4J_TARBALL}     && mv /var/lib/neo4j/data /data     && ln -s /data /var/lib/neo4j/data     && apk del curl
# Thu, 14 Sep 2017 06:37:40 GMT
WORKDIR /var/lib/neo4j
# Thu, 14 Sep 2017 06:37:42 GMT
VOLUME [/data]
# Thu, 14 Sep 2017 06:37:42 GMT
COPY file:4b58674fde5f35ee7b68cae22e9b985fa91c7de85350af95dcdef88ef233c3d6 in /docker-entrypoint.sh 
# Thu, 14 Sep 2017 06:37:42 GMT
EXPOSE 7473/tcp 7474/tcp 7687/tcp
# Thu, 14 Sep 2017 06:37:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Sep 2017 06:37:43 GMT
CMD ["neo4j"]
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
	-	`sha256:1b189c09a59eeeb11786015dce1bcc14e98169832e842939bd02057974ab0a7c`  
		Last Modified: Thu, 14 Sep 2017 07:06:56 GMT  
		Size: 1.5 MB (1502861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd90cc2934615b3ad26b87b52e4b5cda06a23ef694c55efb9ab898726fc49710`  
		Last Modified: Thu, 14 Sep 2017 07:07:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81a227738fe1f308ab809ac29a90b70ab33cd75b64692530d911e9d0c447eefe`  
		Last Modified: Thu, 14 Sep 2017 07:07:31 GMT  
		Size: 89.9 MB (89937366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63ea0324fe1877102f81acaa9d56289e9199aad7a3e659e7611556ce766790e`  
		Last Modified: Thu, 14 Sep 2017 07:07:23 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
