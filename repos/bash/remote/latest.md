## `bash:latest`

```console
$ docker pull bash@sha256:5d02be0d31c2d59f51c250a4cc2c0ade30eb8b8c16c7eb19505135fc38f5bb32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `bash:latest` - linux; amd64

```console
$ docker pull bash@sha256:37ac215e20983bacdb6a93228212004f6936347372d02708d20377190f943fc3
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5069176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f75fd0e533046a637f34138d6f76bc1cb32df47472751e327fa80b07dd73d51`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 Sep 2017 14:32:25 GMT
ADD file:4583e12bf5caec40b861a3409f2a1624c3f3556cc457edb99c9707f00e779e45 in / 
# Wed, 13 Sep 2017 14:32:26 GMT
CMD ["/bin/sh"]
# Thu, 14 Sep 2017 23:09:57 GMT
ENV _BASH_GPG_KEY=7C0135FB088AAF6C66C650B9BB5869F064EA74AB
# Thu, 14 Sep 2017 23:09:57 GMT
ENV _BASH_VERSION=4.4
# Thu, 14 Sep 2017 23:09:57 GMT
ENV _BASH_PATCH_LEVEL=0
# Thu, 14 Sep 2017 23:09:57 GMT
ENV _BASH_LATEST_PATCH=12
# Tue, 26 Sep 2017 00:30:53 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		bison 		ca-certificates 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		make 		ncurses-dev 		openssl 		patch 		tar 	; 		version="$_BASH_VERSION"; 	if [ "$_BASH_PATCH_LEVEL" -gt 0 ]; then 		version="$version.$_BASH_PATCH_LEVEL"; 	fi; 	wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$version.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$version.tar.gz.sig"; 		if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_PATCH_LEVEL" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_PATCH_LEVEL + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$_BASH_VERSION-patches/bash${_BASH_VERSION//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$_BASH_GPG_KEY"; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	rm -rf "$GNUPGHOME"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	for f in config.guess config.sub; do 		wget -O "support/$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 	done; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -r 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .bash-rundeps $runDeps; 	apk del .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION.$_BASH_LATEST_PATCH" ];
# Tue, 26 Sep 2017 00:30:53 GMT
COPY file:fdf06dbdd83ac10faaf143ecd72819fb62707a3e7d98847f450da20c672c1bf5 in /usr/local/bin/ 
# Tue, 26 Sep 2017 00:30:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Sep 2017 00:30:53 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:88286f41530e93dffd4b964e1db22ce4939fffa4a4c665dab8591fbab03d4926`  
		Last Modified: Tue, 27 Jun 2017 18:49:37 GMT  
		Size: 2.0 MB (1990402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e648449132e173c8be646241e85235ccb6211eba9b964170f5d7d72d3821ade0`  
		Last Modified: Tue, 26 Sep 2017 00:45:39 GMT  
		Size: 3.1 MB (3078433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4d2e5ab66c8d3b948d4b673b433fedf0e29e540ac34ed4bcb148e171ed25b9`  
		Last Modified: Tue, 26 Sep 2017 00:45:38 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
