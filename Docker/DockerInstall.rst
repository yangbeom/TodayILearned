Docker 설치하기
===============

.. note:
	Ubuntu 16.04 LTS를 설치후 진행하였습니다.

`Docker Install Ubuntu <https://docs.docker.com/engine/installation/linux/ubuntulinux/>`_ 를 보고 설치하였습니다.

Update apt sources
--------------------

::

	sudo apt-get update
	sudo apt-get install apt-transport-https ca-certificates

를 이용하여 업데이트를 합니다.

`etc/apt/sources.list.d/docker.list` 에 `deb https://apt.dockerproject.org/repo ubuntu-xenial main` 을 적고 저장합니다.

::

	sudo apt-get update
	sudo apt-get purge lxc-docker
	apt-cache policy docker-engine

을 이용하여 업데이트를 해줍니다.

Prerequisites by Ubuntu Version
-----------------------------------

::

	sudo apt-get update
	sudo apt-get install linux-image-extra-$(uname -r)

을 이용하여 `linux-image-extra` packge를 커널버전에 맞춰 설치합니다.

Install
--------

::

	sudo apt-get install docker-engine

을 입력하여 Docker를 설치합니다.

::

	sudo docker run hello-world

설치가 완료된후 hello-world를 실행시키면 다음과 같은 글을 확인 할 수 있습니다.

::

	Hello from Docker!
This message shows that your installation appears to be working correctly.

To generate this message, Docker took the following steps:
 1. The Docker client contacted the Docker daemon.
 2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
 3. The Docker daemon created a new container from that image which runs the
    executable that produces the output you are currently reading.
 4. The Docker daemon streamed that output to the Docker client, which sent it
    to your terminal.

To try something more ambitious, you can run an Ubuntu container with:
 $ docker run -it ubuntu bash

Share images, automate workflows, and more with a free Docker Hub account:
 https://hub.docker.com

For more examples and ideas, visit:
 https://docs.docker.com/engine/userguide/
