# 데메테르 법칙

* [Law of Demeter - Wikipedia](https://en.wikipedia.org/wiki/Law_of_Demeter)
* [Law of Demeter - WikiWikiWeb](https://wiki.c2.com/?LawOfDemeter)
* [Introducing Demeter and its Laws](http://www.bradapp.net/docs/demeter-intro.html)

## 데메테르 법칙에 대한 기억법
[Erik Dietrich](https://github.com/erikdietrich)에 의해 작성된 [Visualization Mnemonics for Software Principles](http://www.daedtech.com/visualization-mnemonics-for-software-principles) 포스트는 데메테르 법칙이 무엇인지 이해하는 (그리고 더 이상 까먹지 않는) 매우 효과적인 트릭을 제공합니다. 이탈리아 번역은 [여기](https://github.com/arialdomartini/mnemonics/blob/law-of-demeter/README-italian.md)있습니다.

## 코드 예제
[Krzysztof Grzybek](https://github.com/krzysztof-grzybek)에 의해 제공된 데메테르 법칙을 위반하는 코드의 예입니다.

```javascript
class Plane {
    constructor(crew) {
        this.crew = crew;
    }
    
    getPilotsName() {
        this.crew.pilot.getName();
    }
}

class Crew {
    constructor(pilot) {
        this.pilot = pilot;
    }
}

class Pilot {
    getName() {
        // ...
    }
}
```

객체 사이의 단단한 결합을 만들기 때문에 이것은 좋지 않습니다. 그들은 다른 객체의 내부 구조에 의존합니다.

Fixed code:
```javascript
class Plane {
    getPilotsName() {
        this.crew.getPilotsName();
    }
}

class Crew {
    constructor(pilot) {
        this.pilot = pilot;
    }

    getPilotsName() {
        return this.pilot.getName();
    }
}
