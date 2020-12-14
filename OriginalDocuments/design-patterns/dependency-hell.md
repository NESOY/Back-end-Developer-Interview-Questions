# 의존성 지옥 (Dependency Hell)

## [Krzysztof Grzybek](https://github.com/krzysztof-grzybek)

1. 가장 기본적인 접근 방식은 수동으로 종속성을 업데이트하여 다른 패키지 버전 관리를 만족하거나 유지 관리자에게 이를 수행하도록 요청하는 것입니다.
2. 내가 사용하는 시맨틱 버전 관리 라이브러리를 신뢰한다면보다 편안한 버전 관리를 시도합니다.
3. 이 문제에 대한 더 나은 해결책은 프로젝트를 monorepo로 유지하는 것입니다. 이 접근 방식은 다른 문제를 의미합니다.
3. 또 다른 흥미로운 솔루션은 넷플릭스 엔지니어링 팀에서 발표한 [system for easier dependencies management](https://www.youtube.com/watch?v=VNqmHJtItCs)입니다.
