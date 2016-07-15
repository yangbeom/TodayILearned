VirtualEnv
===========

Virtualenv는 시스템에 영향을 주지않는 환경을 만들어주는 프로젝트이다.
여러 프로젝트를 진행할시 필요없는 패키지나 의존성등을 설치하지 않고
사용 할 수 있게 각각의 독립적인 환경을 만들어주는 환경이다.

Ubuntu를 기준으로 설명 하려 한다.

설치
----

설치는 간단하게 pip을 이용하여 설치 하면 된다.

.. code-block: bash

    sudo pip3 install Virtualenv

Virtualenv 환경 만들기
----------------------

.. code-block: bash

    virtualenv {env name}

을 적는다면 env name 폴더가 생성되며 env name이라는 환경이 생성되게 된다.

이때 Python 버전이 여러개라면 -p 옵션을 통하여 원하는 버전을 이용하여 생성이 가능하다.

.. code-block: bash

    virtualenv -p /usr/bin/python2.7 venv //2.7버전을 이용하여 virtualenv생성
    virtualenv -p /usr/bin/python3.5 venv //3.5버전을 이용하여 virtualenv생성

나는 ``` virtualenv -p /usr/bin/python3.5 ~/.venv/flask ``` 라고 만들었다.

Virtualenv 이용하기
-------------------

.. code-block: bash

    source ~/.venv/flask/bin/activate

를 적어주면 Virtualenv환경이 실행된다.

이때 실행이 잘되었다면 (env name)이 나타나게 될 것이다.

잘 설치가 되었다면 pip을 이용하여 원하는 패키지를 설치해 보자.

그후 Virtualenv를 이용하고 있는 상태에서 pip list와 사용하고 있지 않은
상태에서의 pip list를 사용했을때 출력되는 list가 다른것을 확인 할 수 있다.

마지막으로 Virtualenv를 종료하기 위해서는

.. code-block: bash

    deactivate

를 적어주면 Virtualenv에서 나올 수 있다.