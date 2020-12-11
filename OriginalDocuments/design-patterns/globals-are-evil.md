# 전역객체는 나쁘다

[Krzysztof Grzybek](https://github.com/krzysztof-grzybek)에 의한 힌트입니다.

1. 전역 객체나 스태틱 객체는 종속성/결합을 유발합니다. 그러므로 전역 객체나 스태틱 객체는 캡슐화의 개념을 깨뜨립니다.
2. 이에 대해 추론하기 어렵습니다. - 이러한 객체들의 행동을 이해하는 논리적 범위는 전체 프로그램으로 확장됩니다.
3. 이들은 mock/stub하기 어렵습니다.
4. 전역 객체는 메인 범위를 오염시킵니다.

Bad:
```javascript
class Player {
    walk() {
        this.x = nextDestination.x;
        this.y = nextDestination.y;
    }
}
```

Good:
```javascript
class Player {
    walk(destination) {
        this.x = destination.x;
        this.y = destination.y;
    }
}
```
