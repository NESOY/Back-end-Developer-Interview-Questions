# Blue-Green Deployment

## [Krzysztof Grzybek](https://github.com/krzysztof-grzybek)

이것은 Blue-Green Deployment에서 가장 까다로운 부분입니다. 이 문제에 대한 일반적인 해결책은 이전 릴리즈와 다음 릴리즈와 지원이 되는 데이터베이스 스키마를 가지는 중간 릴리즈를 가지는 것입니다.
이 접근 방식을 사용하면 quick revert를 포함하여 Blue-Green Deployment의 모든 장점을 계속 이용할 수 있습니다. 비용은 중간 릴리스의 오버헤드입니다.
