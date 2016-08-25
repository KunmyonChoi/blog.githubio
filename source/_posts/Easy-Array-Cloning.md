---
title: Easy Array Cloning
date: 2016-08-18 00:25:05
categories:
 - Javascript
tags:
 - Tip

---

React를 사용하다 보면 immutable 이라는 단어를 많이 보게 됩니다.

pure function으로 previous state와 action으로 next state를 생성하는 과정에서 이전 상태의 일부 값을 변경하는 것이 아니라 완전히 새로운 객체를 생성해 내게 됩니다.

ReactElement 코드를 보면 다음과 같은 구문을 볼 수 있는데, 이는 Array를 복사한 새로운 Clone array를 만들어 내는 역할을 합니다.

``` var shadowChildren = props.children.slice(0); ```

이렇게 복사된 객체가 이전과 동일한지 아래와 같이 확인해 볼 수 있다.

<iframe height='265' scrolling='no' src='//codepen.io/KunmyonChoi/embed/zBbajy/?height=265&theme-id=0&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>See the Pen <a href='http://codepen.io/KunmyonChoi/pen/zBbajy/'>Array clone</a> by Kunmyon Choi (<a href='http://codepen.io/KunmyonChoi'>@KunmyonChoi</a>) on <a href='http://codepen.io'>CodePen</a>.
</iframe>