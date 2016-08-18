Django postgresql 연결하기
==========================

psycopg2 설치
-------------

.. code-block:: python

    pip install psycopg2

이때 설치가 되지 않고 에러가 난다면

.. code-block:: python

    sudo apt-get install python3-dev libpq-dev

을 설치하면 된다.

이후 `settings.py` 에 DATABASES를 수정해주면 된다.

.. code-block:: python

    DATABASES = {
        'default': {
            'ENGINE': 'django.db.backends.postgresql',
            ...
        }
    }

다른 블로그에 보면 ``django.db.backends.postgresql_psycopg2`` 로 적혀 있는 곳이 많이 보인다.

`Django Doc 1.10 <https://docs.djangoproject.com/en/1.10/ref/settings/#std:setting-ENGINE>`_
에 보면 Django 1.9 이전의 ``django.db.backends.postgresql_psycopg2`` 가
``django.db.backends.postgresql``로 바뀌었다고 한다.

그러나 ``django.db.backends.postgresql_psycopg2``는 여전히 작동한다고 적혀있다.
