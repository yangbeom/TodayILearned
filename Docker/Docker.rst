Docker Tutorial
===============

Image 와 Containers
-------------------

``Docker run hello-world`` 의 의미

- docker = Tell your operating system you are using the docker program
         OS에 docker프로그램을 사용한다는 의미.
- run = A subcommand that creates & runs a Docker container
        부가 명령어로 Docker Container를 만들고 실행한다는 의미.
- hello-world = Tells Docker which image to load iinto the container
                Docker에게 Container에 로드할 Image

즉 Image는 filesystem과 parameters이고 실행을 위한것, 상태는 없고 변화 하지도 않는다.

Container는 실행되는 Image를 말한다.

다음 명령어를 입력하면 docker는 hello-world이미지가 있느지 체크하고
없다면 Docker Hub에서 다운로드한다.
다운로드가완료되면 Container에 Image를 로드하고 작동시킨다.

Build your own image
--------------------
1. 폴더를 만들고 폴더안에 Dockerfil을 생성한다.
