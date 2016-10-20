Telegram Bot을 만들며 알게 된것들
=================================
Telegram Bot SetWebhook
------------------------
`https://api.telegram.org/bot<token>/setWebhook?url=주소` 와 같은 형식으로 셋팅을 하게되는데

주소는 https:// 이후의 주소를 적어 주어야 적용이 된다.

Telegram Bot message
--------------------

.. code-block:: json

    {'message': {'message_id': 140,
             'chat': {'id': 148xxxxxx,
                      'username': 'username',
                      'first_name': 'first_name',
                      'type': 'private'},
             'date': 1453006866,
             'from': {'id': 148xxxxxx,
                      'username': 'username',
                      'first_name': 'first_name'},
             'text': 'text'},
    'update_id': 893xxxxxx}

형식으로 message가 전송된다.

Telegram Bot Inline Message
---------------------------

.. code-block:: json

    {'update_id': 677165716, 'inline_query': {'offset': '',
                                              'from': {'first_name': 'xx',
                                                       'username': 'xx',
                                                       'id': 12345678},
                                              'query': 'message', 
                                              'id': '123413241234'}}


위와 같은 형식의 메세지가 도착하지만 message가 아닌 inline_query로 도착하게 된다.
