### Anti pattern, 안티 패턴

안티패턴이란, 실제 많이 사용되는 패턴이지만 비효율적이거나 비생산적인 패턴을 의미한다.
실제 습관적으로 많이 사용하는 패턴이지만, 성능, 디버깅, 유지보수, 가독성 등의 측면에서 서비스에 부정적인 영향을 줄 수 있어 사용을 지양하는 패턴이다.


안티패턴은 여러가지가 존재한다.

## if/for/where문 한 줄짜리 블록을 생략하는 것은 좋지 않다.

코드 구조를 애매하게 만들어 가독성이 떨어지고, 문법적 오류가 아니기 때문에 디버깅이 어려워 오류 확률이 높은 잠재적 위험 요소가 될 수 있다.


## 배열 순회시 array.length는 캐시하고 사용하는 것이 좋다.

주어진 조건 표현식이 만약 100번 1000번 반복하게 된다면, array.length가 100번 1000번 수행하게된다. 따라 프로그램의 성능을 높이기 위해서는 
불필요한 계산이 반복되지 않도록 배열의 길이를 한 번만 계산한도록 캐싱하는 것이 좋은 방법이다.

