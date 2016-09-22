fork 해둔 레포지토리 최신버전으로 올리기
========================================

fork할 당시 remote를 등록하지 않았다면

.. code-block:: bash

    $ git remote -v

를 했을때 origin 하나만 보일 것이다.

.. code-block:: bash

    $ git remote add <이름> <원본 소스 주소>

를 이용하여 remote 를 등록한다.

.. code-block:: bash

    $ git fetch upstream
    $ git checkout master
    $ git merge <이름>/master


