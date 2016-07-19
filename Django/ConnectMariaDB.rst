Ubuntu 16.04에 Mariadb설치 후 Django에 연결하기
===============================================

.. code-block:: bash

    sudo apt-get install mariadb-server

을 입력하면 Ubuntu에 가장 최신 버전을 설치하게 된다.

Django에서 이용하기 위해서 설치를 하였는데

타블로그에서 mariadb는 libmariadbclient-dev를 설치하라고 적혀있었으

Ubuntu 16.04 LTS에서 아직 libmariadbclient-dev 설치하지 못하여 libmysqllient-dev로 설치하여 mysqlclient를 설치하였다.

.. code-block:: python

    pip install mysqlclient

Django에서 이용하기 위해서

settings.py에 다음과 같이 수정해 준다.

.. code-block:: pythonf

    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'HOST' : 'localhost',
        'USER' : 'USERNAME',
        'NAME' : 'DATABASENAME',
        'PASSWORD' : 'PASSWORD',
        'PORT' : 3306,
    }

이때 `ENGINE` 을 제외한 나머지는 각자 세팅에 맞게 설정해주면 된다.
