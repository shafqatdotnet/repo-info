## `groovy:jre7-alpine`

```console
$ docker pull groovy@sha256:b52b7f87cc010e1b6cecf747d7b64c5c725231d366766a1984d64f9af018171b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `groovy:jre7-alpine` - linux; amd64

```console
$ docker pull groovy@sha256:ac0fe72ccfc3ed9f1aa7a847d93aba0b136ce189a4346a7077155f2b4b37c6ec
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.0 MB (101027440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b7dbfb01155e40f8f337d6e76de0ca35ef2a517557fb2a4ab470610acbc888f`
-	Default Command: `["groovysh"]`

```dockerfile
# Wed, 13 Sep 2017 14:32:25 GMT
ADD file:4583e12bf5caec40b861a3409f2a1624c3f3556cc457edb99c9707f00e779e45 in / 
# Wed, 13 Sep 2017 14:32:26 GMT
CMD ["/bin/sh"]
# Thu, 14 Sep 2017 04:13:40 GMT
ENV LANG=C.UTF-8
# Thu, 14 Sep 2017 04:13:41 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 14 Sep 2017 04:17:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.7-openjdk/jre
# Thu, 14 Sep 2017 04:17:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.7-openjdk/jre/bin:/usr/lib/jvm/java-1.7-openjdk/bin
# Thu, 14 Sep 2017 04:17:46 GMT
ENV JAVA_VERSION=7u131
# Thu, 14 Sep 2017 04:17:47 GMT
ENV JAVA_ALPINE_VERSION=7.131.2.6.9-r1
# Thu, 14 Sep 2017 04:18:00 GMT
RUN set -x 	&& apk add --no-cache 		openjdk7-jre="$JAVA_ALPINE_VERSION" 	&& [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 14 Sep 2017 06:22:18 GMT
CMD ["groovysh"]
# Thu, 14 Sep 2017 06:22:18 GMT
ENV GROOVY_HOME=/opt/groovy
# Thu, 14 Sep 2017 06:22:18 GMT
ENV GROOVY_VERSION=2.4.12
# Thu, 14 Sep 2017 06:22:32 GMT
RUN set -o errexit -o nounset 	&& echo "Installing dependencies" 	&& apk add --no-cache 		bash 		&& echo "Installing build dependencies" 	&& apk add --no-cache --virtual .build-deps 		ca-certificates 		gnupg 		openssl 		unzip 		&& echo "Downloading Groovy" 	&& wget -O groovy.zip "https://dist.apache.org/repos/dist/release/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip" 		&& echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server" 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in 		"7FAA0F2206DE228F0DB01AD741321490758AAD6F" 		"331224E1D7BE883D16E8A685825C06C827AF6B66" 		"34441E504A937F43EB0DAEF96A65176A0FB1CD0B" 		"9A810E3B766E089FFB27C70F11B595CEDC4AEBB5" 	; do 		for server in 			ha.pool.sks-keyservers.net 			hkp://p80.pool.sks-keyservers.net:80 			pgp.mit.edu 		; do 			echo "  Trying ${server}"; 			if gpg --keyserver "${server}" --recv-keys "${key}"; then 				break; 			fi; 		done; 	done; 	if [ $(gpg --list-keys | grep -c "pub ") -ne 4 ]; then 		echo "ERROR: Failed to fetch GPG keys" >&2; 		exit 1; 	fi 		&& echo "Checking download signature" 	&& wget -O groovy.zip.asc "https://dist.apache.org/repos/dist/release/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc" 	&& gpg --batch --verify groovy.zip.asc groovy.zip 	&& rm -rf "${GNUPGHOME}" 	&& rm groovy.zip.asc 		&& echo "Installing Groovy" 	&& unzip groovy.zip 	&& rm groovy.zip 	&& mkdir /opt 	&& mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/" 	&& ln -s "${GROOVY_HOME}/bin/grape" /usr/bin/grape 	&& ln -s "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy 	&& ln -s "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc 	&& ln -s "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole 	&& ln -s "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc 	&& ln -s "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh 	&& ln -s "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy 		&& echo "Applying workaround for https://issues.apache.org/jira/browse/GROOVY-7906" 	&& sed -i "s|#!/bin/sh|#!/bin/bash|" "${GROOVY_HOME}/bin/grape" 	&& sed -i "s|#!/bin/sh|#!/bin/bash|" "${GROOVY_HOME}/bin/groovy" 	&& sed -i "s|#!/bin/sh|#!/bin/bash|" "${GROOVY_HOME}/bin/groovyc" 	&& sed -i "s|#!/bin/sh|#!/bin/bash|" "${GROOVY_HOME}/bin/groovyConsole" 	&& sed -i "s|#!/bin/sh|#!/bin/bash|" "${GROOVY_HOME}/bin/groovydoc" 	&& sed -i "s|#!/bin/sh|#!/bin/bash|" "${GROOVY_HOME}/bin/groovysh" 	&& sed -i "s|#!/bin/sh|#!/bin/bash|" "${GROOVY_HOME}/bin/java2groovy" 		&& echo "Cleaning up build dependencies" 	&& apk del .build-deps 		&& echo "Adding groovy user and group" 	&& addgroup -S -g 1000 groovy 	&& adduser -D -S -G groovy -u 1000 -s /bin/ash groovy 	&& mkdir -p /home/groovy/.groovy/grapes 	&& chown -R groovy:groovy /home/groovy
# Thu, 14 Sep 2017 06:22:32 GMT
USER [groovy]
# Thu, 14 Sep 2017 06:22:32 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Thu, 14 Sep 2017 06:22:32 GMT
WORKDIR /home/groovy
# Thu, 14 Sep 2017 06:22:35 GMT
RUN set -o errexit -o nounset 	&& echo "Testing Groovy installation" 	&& groovy --version
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
	-	`sha256:fd43573df90c82d7e60c22718682d64c6c6b89fc2c409dd3c426090b41f0b573`  
		Last Modified: Thu, 14 Sep 2017 04:53:05 GMT  
		Size: 61.1 MB (61132262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5a2431f76c28849ae18cdc04157dfc019caa1faec0ef3558dbc9a9e411d7497`  
		Last Modified: Fri, 15 Sep 2017 00:29:58 GMT  
		Size: 37.9 MB (37904398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82465923243d30ca7967ca809eced85d6a44aa7160c0125cc52b7c0be4b24979`  
		Last Modified: Fri, 15 Sep 2017 00:29:54 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
