# 손상 방지 레이어 (Anti-corruption Layer)란?
  
## [Krzysztof Grzybek](https://github.com/krzysztof-grzybek)

동일한 모델에서 작동하지 않는 하위 시스템 (대부분 외부 또는 레거시 시스템과 함께) 간의 통신을 담당하는 시스템의 계층입니다.
손상 방지 레이어의 목적은 클라이언트에게 고유한 도메인 모델의 기능을 제공하는 고립된 계층을 생성하기 위함입니다.
