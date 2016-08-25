---
title: ES6의 7번째 타입 Symbol
date: 2016-08-18 00:05:57
categories:
 - Javascript
tags:
  - ES6
  - Standard

---

참고) http://hacks.mozilla.or.kr/2015/09/es6-in-depth-symbols/

기존 JS는 다음과 같이 6가지 타입을 가지고 있었습니다.

- Undefined
- Null
- Boolean
- Number
- String
- Object

Symbol은 7번째로 추가된 (문자열이나 객채가 아닌) 어떠한 값을 갖는 새로운 타입 입니다.

다음 코드는 Symbol이 활용될 수 있는 경우를 나타내는 예제 입니다.

<iframe height='265' scrolling='no' src='//codepen.io/KunmyonChoi/embed/dXAZqg/?height=265&theme-id=0&default-tab=js,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>See the Pen <a href='http://codepen.io/KunmyonChoi/pen/dXAZqg/'>dXAZqg</a> by Kunmyon Choi (<a href='http://codepen.io/KunmyonChoi'>@KunmyonChoi</a>) on <a href='http://codepen.io'>CodePen</a>.
</iframe>


예제 에서는 object 에 annotation 용도로 flag를 설정하고자 합니다.

isMoving flag는 Symbol을 사용해 지정했고, isHaving flag는 일반적인  boolean property를 사용해 지정 했습니다.

결과를 비교해 보면 Object.keys() 에서 isMoving은 보이지 않지만 isHaving은 key로 나타납니다.

일반적으로 이렇게 property 삽입으로 변형된 array의 경우 Object.keys()나  for-in loop에 의도치 않게 key로 해석되어 나타나기 때문에 권장되는 방법이 아닙니다.

Symbol은 이런 경우  key로 해석되지 않기 때문에 안전하게 사용이 가능합니다.