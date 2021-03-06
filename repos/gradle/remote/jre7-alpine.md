## `gradle:jre7-alpine`

```console
$ docker pull gradle@sha256:db85b1ea46cae23723a965a6d7c1017bcf9b596c0b38ef1e1ff4329f5fe8ab27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gradle:jre7-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:12762e7aa0c11fac1a2d88a9cbf91f7ade27ce92a9e5c4359fbd2c142f1f7a93
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134551945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deccfe7a766cd34defc0479fd1919ede70caff05afa082c3fb3ae0e91fbc9918`
-	Default Command: `["gradle"]`

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
# Thu, 14 Sep 2017 06:24:15 GMT
CMD ["gradle"]
# Thu, 14 Sep 2017 06:24:15 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 26 Sep 2017 17:30:26 GMT
ENV GRADLE_VERSION=4.2
# Tue, 26 Sep 2017 17:30:26 GMT
ARG GRADLE_DOWNLOAD_SHA256=515dd63d32e55a9c05667809c5e40a947529de3054444ad274b3b75af5582eae
# Tue, 26 Sep 2017 17:30:34 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=515dd63d32e55a9c05667809c5e40a947529de3054444ad274b3b75af5582eae
RUN set -o errexit -o nounset 	&& echo "Installing build dependencies" 	&& apk add --no-cache --virtual .build-deps 		ca-certificates 		openssl 		unzip 		&& echo "Downloading Gradle" 	&& wget -O gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip" 		&& echo "Checking download hash" 	&& echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c - 		&& echo "Installing Gradle" 	&& unzip gradle.zip 	&& rm gradle.zip 	&& mkdir /opt 	&& mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/" 	&& ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle 		&& apk del .build-deps 		&& echo "Adding gradle user and group" 	&& addgroup -S -g 1000 gradle 	&& adduser -D -S -G gradle -u 1000 -s /bin/ash gradle 	&& mkdir /home/gradle/.gradle 	&& chown -R gradle:gradle /home/gradle 		&& echo "Symlinking root Gradle cache to gradle Gradle cache" 	&& ln -s /home/gradle/.gradle /root/.gradle
# Tue, 26 Sep 2017 17:30:34 GMT
USER [gradle]
# Tue, 26 Sep 2017 17:30:34 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 26 Sep 2017 17:30:35 GMT
WORKDIR /home/gradle
# Tue, 26 Sep 2017 17:30:39 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=515dd63d32e55a9c05667809c5e40a947529de3054444ad274b3b75af5582eae
RUN set -o errexit -o nounset 	&& echo "Testing Gradle installation" 	&& gradle --version
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
	-	`sha256:5707c7cbba33b6c5f7b1244d471655c698bfd762346b0e20ef2632a722210235`  
		Last Modified: Tue, 26 Sep 2017 17:34:52 GMT  
		Size: 71.4 MB (71428902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:343fc2f110f0cb756f853d746a69b69cc8d54d2eb4d6ca67a2c0f9538ec4a3d6`  
		Last Modified: Tue, 26 Sep 2017 17:34:45 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
