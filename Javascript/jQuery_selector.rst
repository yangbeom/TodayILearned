jQuery
======

selector

$('div') -> div 태그를 셀렉트한다
$('div','span') -> div와 span태그를 셀렉트한다. 이와같이 여러가지를 동시에 셀렉트 할수 있다.

$('.title') -> . 은 class 명을 의미 즉 class = "title"로 되어있는것들을 셀렉트한다

$('#title') -> #은 id 값을 의미 즉 id = "title"로 되어있는것을 셀렉트한다

$('[속성명="값"]') -> 속성이름과 값이 일치하는것을 셀렉트한다. =대신 != *= $= ^=를 사용 할수 있는데 순서대로 값이 아닌것,
값을 포함하는것, 값으로 끝나는것, 값으로 시작하는것을 셀렉트한다.
$('속성명="값"] TAG:옵션) 은 속성이름과 값이 일치하는것 안에 태그를 찾는것이다. 이때도 다음과 같은 옵션들을 사용할 수 있다.
`first-child` 첫번째 자식태그를 셀렉트한다.
`last-child` 마지막 자식태그를 셀렉트한다
`nth-child(n)` n번째 를 찾아라 (단 `nth-child(n)의 n은 1부터 시작한다.
`only-child` 태그가 하나인 값을 찾아라

$('TAG':옵션) 옵션을 통하여 여러가지를 선택할수 있는데
`first` 옵션은 TAG중 가장 첫번째를
`last` 는 TAG중 가장 마지막을
`even` 옵션은 짝수번째의 것들을
`odd` 옵션은 홀수번째의 것들을
`not('anothertag')` 를 이용하면 TAG이면서 anothertag가 아닌것을 가져온다 물론 not이후에도 :옵션을 사용가능하다.

`eq(n)`는 n번째것을 선택한다.
`gt(n)`는 n번째 이후의 것들을 선택
`lt(n)`는 n번째 이전의 것들을 선택

`has(anothertag)` 는 TAG중 anothertag가 포함되어있는것
`empty` 비어있는 태그 <div></div> 와같은것
`contains(string)` 문자열을 포함하는것을 셀렉트한다
`parent` 부모를 셀렉트한다

$(TAG > anothertag) 는 TAG안의 첫번째자식을 셀렉트한다
$(TAG + anothertag) 는 TAG뒤에 붙어있는 anothertag를 셀렉트한다
$(TAG ~ anothertag) 는 TAG 뒤에 모든 anothertag를 셀렉트한다