C# 기초문법 메모
===============

C# 문자열
---------

C#의 키워드 string은 .NET의 System.String 클래스와 동일하다.
즉 Substring() Length 속성등을 사용할 수 있다.

C#의 string은 Immutable로 설정되면 다시 변경할 수 없다.
같은 변수에 넣으면 새로운 객체를 생성하여 변수에 할당하기때문에 다른 메모리를 갖는 객체를 가리키게 되는것.
즉 string을 계속 변경하면 메모리 낭비가 될 수 있음.

때문에 문자열 갱신이 많은곳에서는 System.Text의 StringBuilder를 사용하는것이 좋다.
StringBuilder는 Mutable 타입이며 별도의 메모리를 생성, 소멸하지 않고 일정한 버퍼를 갖고 문자열 갱신을 효율적으로 처리한다.

?? 연산자
---------

::

    int? x = x ?? 0

a가 Null 이면 0을 리턴 아니면 a를 리턴해준다.

즉 a값이 Null인지 아닌지에 따라 다른 값을 넣어주어야할때 사용.

for vs foreach
--------------

foreach가 다른 루프보다 최적화 되어있다.
다차원 배열의 경우 for문을 여러번 사용해야하는데
foreach를 이용하면 한번에 사용가능하다.

foreach (변수 in literal 변수)

Value Type vs Reference Type
----------------------------

struct를 사용하면 Value Type, class를 사용하면 Reference Type이 생성된다.

Value Type은 상속될 수 없음, 상대적으로 간략한 데이터 값을 저장

Reference Type은 상속이 가능하고 좀 더 복잡한 데이터와 행위들을 정의 하는 곳에 많이 사용됨

Value Type의 전달은 데이터를 copy하여 전달하지만 Reference Type은 Heap에 있는 객체에 대한 reference를 전달

pass by Reference
-----------------

즉 함수 안에서 값이 연산후 끝이아닌 값이 변경되어야하는 인자라면 ref를 사용한다
비슷한 키워드로는 out이 있다. out키워드는 말그대로 out 시킬곳에 값을 넘겨준다.

C# params
---------

파라메터의 갯수를 미리 알수 없는경우 params 키워드를 사용한다.

Event
-----

C#의 Class에는 event라는 키워드가 있어 subscriber들에게 event가 발생했음을 알려준다.
