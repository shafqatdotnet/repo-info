## `openjdk:7-jre`

```console
$ docker pull openjdk@sha256:8181dd77e50da3267d2ede6e55d3c03144310308bf59a008ba5d8ca0212f71e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `openjdk:7-jre` - linux; amd64

```console
$ docker pull openjdk@sha256:3e8eb36aa6a2ff0032163f49231293cdcc70adc86b665be2752ff14149458fd6
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.5 MB (189538328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:936ff883245f3167d884c6c68359c415dfbccfaaacfce6477556cf0a386192db`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 Sep 2017 08:40:43 GMT
ADD file:d7333b3e0bc6479d2faed32e06d85f1975e5b23e13e75555aeed0f639770413b in / 
# Wed, 13 Sep 2017 08:40:43 GMT
CMD ["bash"]
# Wed, 13 Sep 2017 12:32:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Sep 2017 12:32:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 Sep 2017 04:14:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 14 Sep 2017 04:14:25 GMT
ENV LANG=C.UTF-8
# Thu, 14 Sep 2017 04:14:26 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 14 Sep 2017 04:14:28 GMT
RUN ln -svT "/usr/lib/jvm/java-7-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Thu, 14 Sep 2017 04:14:28 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Thu, 14 Sep 2017 04:14:28 GMT
ENV JAVA_VERSION=7u151
# Thu, 14 Sep 2017 04:14:28 GMT
ENV JAVA_DEBIAN_VERSION=7u151-2.6.11-1~deb8u1
# Thu, 14 Sep 2017 04:15:48 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-7-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
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
	-	`sha256:606c0b57feb051ea7df9ecb5091d7c5275047f4baa9b54700350c3f35e4a4f26`  
		Last Modified: Thu, 14 Sep 2017 04:51:25 GMT  
		Size: 795.6 KB (795601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584c35e01c21b7270342137194d0860c0a7a90f65441c6e8a1e0f7571bc84a30`  
		Last Modified: Thu, 14 Sep 2017 04:51:27 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b2c1657fd0e01b54bc8a64a8e8c5470058e23a343328e8ac2379e3d043e6ce`  
		Last Modified: Thu, 14 Sep 2017 04:51:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b4dd65ad29cb149c9ecfc67a1032e7737acfd4c5f696afda2a27483ad9152ae`  
		Last Modified: Thu, 14 Sep 2017 04:51:54 GMT  
		Size: 116.9 MB (116883085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:7-jre` - linux; arm variant v5

```console
$ docker pull openjdk@sha256:829cf6b028d6012005886243c6bf365ab7ae65a0dd5b4099f7d506e9bdc47184
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.2 MB (166177534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f776fffddad023f5aedf44e3bba705c43dd6863d9f83188d45775157a66f462`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 27 Sep 2017 14:24:27 GMT
ADD file:195667b0ccd6dad7d7793044adefb6ab0b4934a95d6383e0e1b09275397bc1e7 in / 
# Wed, 27 Sep 2017 14:24:27 GMT
CMD ["bash"]
# Wed, 27 Sep 2017 14:47:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 27 Sep 2017 14:47:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 27 Sep 2017 15:15:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 27 Sep 2017 15:15:41 GMT
ENV LANG=C.UTF-8
# Wed, 27 Sep 2017 15:15:42 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 27 Sep 2017 15:15:43 GMT
RUN ln -svT "/usr/lib/jvm/java-7-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 27 Sep 2017 15:15:43 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 27 Sep 2017 15:15:43 GMT
ENV JAVA_VERSION=7u151
# Wed, 27 Sep 2017 15:15:43 GMT
ENV JAVA_DEBIAN_VERSION=7u151-2.6.11-1~deb8u1
# Wed, 27 Sep 2017 15:16:52 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-7-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
```

-	Layers:
	-	`sha256:0000473879860f50b5d7e33d60cdb2bd20eccd2563da6dfab9023b079c54f91b`  
		Last Modified: Wed, 27 Sep 2017 14:28:25 GMT  
		Size: 50.9 MB (50879797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:383dc0c402c2a94402ca03cfa2ec05c87d8e91d968961c72d52a7f47b0823a7f`  
		Last Modified: Wed, 27 Sep 2017 15:01:39 GMT  
		Size: 18.7 MB (18653386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636c71cf23a0e02422b029c67bb652759226bc08a46050db8ca3e34118d2c9d4`  
		Last Modified: Wed, 27 Sep 2017 15:31:09 GMT  
		Size: 788.3 KB (788348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a7695c88a60e744b02ca7c8c5386680ad543bdaeffd652becc698d607be0c72`  
		Last Modified: Wed, 27 Sep 2017 15:31:09 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30af743ef3c6d30e8cdb5029e4001c3752dffeed996d894f384e2e6be1451f90`  
		Last Modified: Wed, 27 Sep 2017 15:31:08 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0db5d90ba6727880a1d5d0c51323714da87bf74259cc79069a08866c0b3c6c34`  
		Last Modified: Wed, 27 Sep 2017 15:31:31 GMT  
		Size: 95.9 MB (95855625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:7-jre` - linux; arm variant v7

```console
$ docker pull openjdk@sha256:592d5ae10f8bd3ccdd0a5feaf46b3f7da01c8d52eeeb9e2039e25a6172da66e3
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.0 MB (171967524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bda94bd12531f6ce1f52245158e5782a6030b3dbe490693d1ef6b902e4e3cbd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 27 Sep 2017 04:12:21 GMT
ADD file:ef59ce7fe68882b1b44bc3c4a5e9e465561cb257fb63f8c2b3c247abb012486b in / 
# Wed, 27 Sep 2017 04:12:22 GMT
CMD ["bash"]
# Wed, 27 Sep 2017 04:39:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 27 Sep 2017 04:39:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 27 Sep 2017 05:19:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 27 Sep 2017 05:19:21 GMT
ENV LANG=C.UTF-8
# Wed, 27 Sep 2017 05:19:22 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 27 Sep 2017 05:19:24 GMT
RUN ln -svT "/usr/lib/jvm/java-7-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 27 Sep 2017 05:19:24 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 27 Sep 2017 05:19:24 GMT
ENV JAVA_VERSION=7u151
# Wed, 27 Sep 2017 05:19:25 GMT
ENV JAVA_DEBIAN_VERSION=7u151-2.6.11-1~deb8u1
# Wed, 27 Sep 2017 05:20:47 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-7-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
```

-	Layers:
	-	`sha256:8c7b63aa62f92f5be1e93e5129c5c99dac397c6d3b5f6c6452bfd0905f6f20be`  
		Last Modified: Wed, 27 Sep 2017 04:17:18 GMT  
		Size: 48.7 MB (48686544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a607bd01ffd678134d1281825ba8fafc069965446932fb3da991e8e6c2d3065d`  
		Last Modified: Wed, 27 Sep 2017 04:58:12 GMT  
		Size: 18.3 MB (18262468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:471f4416b78b04ea9f2c696c8cf2b185f8e140c19484b26d6ba923f8e4f8d39a`  
		Last Modified: Wed, 27 Sep 2017 05:35:15 GMT  
		Size: 763.0 KB (762959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd30762fc0081bbe65b4a1fc76f2eece0404254a02dce19d6d780b1bfd5c042`  
		Last Modified: Wed, 27 Sep 2017 05:35:16 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ffd873da19f0a4486e03412365b191771991f3f1a9ae9c41c8b56e713be1a1`  
		Last Modified: Wed, 27 Sep 2017 05:35:14 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a072022d9431474505ba7eecbd13ba82e7c87a115c846504607840ea5faec61`  
		Last Modified: Wed, 27 Sep 2017 05:36:06 GMT  
		Size: 104.3 MB (104255174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:7-jre` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:8e7ed5f088b0cfbd7bdf12152a4c8dbd653eaa7066c4b25c9fafa7eecf6c9cbc
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.5 MB (163457484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b094b4182666440564925d42a0acb286d51c1428a2d3ee22b8fdeb540d1bc4e5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Sep 2017 17:23:41 GMT
ADD file:9f576a63a5e03994904e585c35fbeef6a2c96c41d8f696705c033f3ca69b6a2b in / 
# Fri, 08 Sep 2017 17:23:42 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 18:32:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 08 Sep 2017 18:32:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 Sep 2017 22:31:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 14 Sep 2017 22:31:37 GMT
ENV LANG=C.UTF-8
# Thu, 14 Sep 2017 22:31:39 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 14 Sep 2017 22:31:41 GMT
RUN ln -svT "/usr/lib/jvm/java-7-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Thu, 14 Sep 2017 22:31:42 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Thu, 14 Sep 2017 22:31:43 GMT
ENV JAVA_VERSION=7u151
# Thu, 14 Sep 2017 22:31:43 GMT
ENV JAVA_DEBIAN_VERSION=7u151-2.6.11-1~deb8u1
# Thu, 14 Sep 2017 22:38:01 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-7-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
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
	-	`sha256:faca5cf969f88a9b02da68ef94499b29d5bf74180ee76a7ad22a7debc7eb1b9c`  
		Last Modified: Thu, 14 Sep 2017 23:07:16 GMT  
		Size: 789.4 KB (789391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f043a5e1e1c7b9c6f765a3e8aaccfdee8ade3ae34a8459190d507e28033a025a`  
		Last Modified: Thu, 14 Sep 2017 23:07:16 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf53c8c46125cb533bbecd8a785d72381c2bc14f12fa007dc8c45d50a5cbe36`  
		Last Modified: Thu, 14 Sep 2017 23:07:16 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de485a156ff7b019f79b449c70a43c051d331598da6d8acd77fb2d57557d9467`  
		Last Modified: Thu, 14 Sep 2017 23:07:41 GMT  
		Size: 94.0 MB (94000654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:7-jre` - linux; 386

```console
$ docker pull openjdk@sha256:edaba1a32861951775a204b83240f7b49332ede26ceada6479417882ece92080
```

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.8 MB (202753679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a836c96ea780a4dcd62e196d413fe8c7b02d4f8f205ba8b94c923421ed2864e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Sep 2017 13:17:52 GMT
ADD file:e02edf114d3ee3a58b6c6729d41261abc361f69333d3b08c7c730572fd6c1874 in / 
# Fri, 08 Sep 2017 13:17:52 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 13:54:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 08 Sep 2017 13:54:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 09 Sep 2017 14:58:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Sat, 09 Sep 2017 14:58:22 GMT
ENV LANG=C.UTF-8
# Sat, 09 Sep 2017 14:58:23 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Sat, 09 Sep 2017 14:58:24 GMT
RUN ln -svT "/usr/lib/jvm/java-7-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Sat, 09 Sep 2017 14:58:24 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Sat, 09 Sep 2017 14:58:25 GMT
ENV JAVA_VERSION=7u151
# Sat, 09 Sep 2017 14:58:25 GMT
ENV JAVA_DEBIAN_VERSION=7u151-2.6.11-1~deb8u1
# Sat, 09 Sep 2017 15:00:16 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-7-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
```

-	Layers:
	-	`sha256:f611f84acffe6a66fad3356eb9101ed9fff54e980701079bbce3ee4826ccd3ae`  
		Last Modified: Fri, 08 Sep 2017 13:22:33 GMT  
		Size: 52.8 MB (52773126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ed51718fa88831e0e4e7d7e02a316d71bc90cca2fb9a38748ac4aebeb93cb6`  
		Last Modified: Sat, 09 Sep 2017 13:59:44 GMT  
		Size: 21.6 MB (21594447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eb4420296f36e7bf08987e529a0d76b095bfc22a558c10611469cccc903eed8`  
		Last Modified: Sat, 09 Sep 2017 15:25:03 GMT  
		Size: 798.6 KB (798611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94034f638cfae0977b58d6b46ba77e90f33369e37dddc08e4b0a4596e8afec2d`  
		Last Modified: Sat, 09 Sep 2017 15:25:03 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76eb68242e2cfa4128fa94189970405dda28003194a04fa5c0df1611085cfda6`  
		Last Modified: Sat, 09 Sep 2017 15:25:03 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484d72516bc1be66f7947a6f0442e56be79bc5751aaf05c7ed1afe24413a2a46`  
		Last Modified: Sat, 09 Sep 2017 15:25:27 GMT  
		Size: 127.6 MB (127587119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:7-jre` - linux; ppc64le

```console
$ docker pull openjdk@sha256:469df5390da9da1388ff94f4cd46c1f6ede99996f27d6aea8b1c12ec6031a866
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.0 MB (167956494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b61dff27bdfc3837dec3cdeb2c4b8cbc36e2e787e5ac2265dd3f5f4e33f64aef`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Sep 2017 00:32:21 GMT
ADD file:483b3245941140ac32394a804364a1a9bd5dfdf1b4475238b61068cc7252ac08 in / 
# Fri, 08 Sep 2017 00:32:21 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 01:03:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 08 Sep 2017 01:03:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 15 Sep 2017 00:36:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Sep 2017 00:36:25 GMT
ENV LANG=C.UTF-8
# Fri, 15 Sep 2017 00:36:34 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 15 Sep 2017 00:36:41 GMT
RUN ln -svT "/usr/lib/jvm/java-7-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 15 Sep 2017 00:36:43 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Fri, 15 Sep 2017 00:36:45 GMT
ENV JAVA_VERSION=7u151
# Fri, 15 Sep 2017 00:36:47 GMT
ENV JAVA_DEBIAN_VERSION=7u151-2.6.11-1~deb8u1
# Fri, 15 Sep 2017 00:50:36 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-7-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
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
	-	`sha256:93aff8e404272e9833703642ba3aa88fed68af07050f24c7709f569d0ac750dc`  
		Last Modified: Fri, 15 Sep 2017 01:44:08 GMT  
		Size: 791.2 KB (791186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47834a4accdc027a0c9c901088dc1f86871788bde1184be049ad9bd7c3e73851`  
		Last Modified: Fri, 15 Sep 2017 01:44:07 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9aee3929de836275f650ebba768390489923f17a18f3a704c24aa5b63b17d7d`  
		Last Modified: Fri, 15 Sep 2017 01:44:07 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d933a6047136f6e6fffa90ce2f3fbe1e16d0a5411b123e2c8b18e5fafa87b823`  
		Last Modified: Fri, 15 Sep 2017 01:44:37 GMT  
		Size: 96.2 MB (96155763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:7-jre` - linux; s390x

```console
$ docker pull openjdk@sha256:d94ebc0f6144bd53f2e54dd8f53d33669186b9c4dfc77873c30e4b960869bd50
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168743844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d8bb066ac9f66e2184067562f28d537aee2b1b2dc2c3125ad6a4154888514f1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Sep 2017 05:21:42 GMT
ADD file:996e52a941b7162fafcf761c415142a34a2fc703e21d2f264b824373e9fa4b1e in / 
# Fri, 08 Sep 2017 05:21:43 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 05:48:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 08 Sep 2017 05:48:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 08 Sep 2017 17:29:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 08 Sep 2017 17:29:02 GMT
ENV LANG=C.UTF-8
# Fri, 08 Sep 2017 17:29:03 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 08 Sep 2017 17:29:03 GMT
RUN ln -svT "/usr/lib/jvm/java-7-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 08 Sep 2017 17:29:03 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Fri, 08 Sep 2017 17:29:04 GMT
ENV JAVA_VERSION=7u151
# Fri, 08 Sep 2017 17:29:04 GMT
ENV JAVA_DEBIAN_VERSION=7u151-2.6.11-1~deb8u1
# Sat, 09 Sep 2017 05:39:03 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-7-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
```

-	Layers:
	-	`sha256:5f39dbffcd07e3254246d3c2e4b3532c3697ed04f83eadf5433da820098787df`  
		Last Modified: Fri, 08 Sep 2017 05:24:42 GMT  
		Size: 52.8 MB (52788802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5a344275c5d5a12a16990e9ddb7cfb9bc9b793cc51fbf8bf8993426e287c27`  
		Last Modified: Fri, 08 Sep 2017 16:41:52 GMT  
		Size: 19.5 MB (19470373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4c084b3ab1af5428f9981ab28f3dd2a8f154f246fb9d9ce2e9e3782792ea6e7`  
		Last Modified: Fri, 08 Sep 2017 17:34:17 GMT  
		Size: 804.2 KB (804244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6057421880039b10c9b7e533d65d4d7e17bf4a8ce08d971a425491d4efb98f39`  
		Last Modified: Fri, 08 Sep 2017 17:34:17 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7677a9187fddb4ecce26b38d362093884ab54cbd74d93eb2fe859fd6db870285`  
		Last Modified: Fri, 08 Sep 2017 17:34:17 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e221891b78d1067cea90f003fa97c1e3c96c3f47ed7510c321eb3130857ae1f`  
		Last Modified: Sat, 09 Sep 2017 05:42:14 GMT  
		Size: 95.7 MB (95680047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
