Django study
============

Django DB에 json으로 값넣기
--------------------------

::

    python manage.py loaddata 파일명

위와 같이 Django를 이용하여 json 으로된 파일을 DB에 한번에 때려박을수 있는데 이때 json 형식은
::

    [{"model":"모델명","fields":{컬럼명:값}},
     ...
    ]

과 같다.


Django manytomanyField에 들어있는 값 출력하기
--------------------------------------------

Django를 공부할겸 instagram을 카피하는중

User와 Post로 나누고

User에 manytomanyField로 Post를 넣어 놨다.

즉 User 는 id값과 Posts의 pk값들을 갖고 있다.

이때 user를 가져와서 posts를 출력하기위해서는

::

    {% for post in userr.posts.all %}
        {{post.text}}
        {{post.date}}
    {% endfor %}

와같이 posts뒤에 all이라던지 조건을 붙여서 부른뒤 넣어야한다.