# 특별한 Null

## [Krzysztof Grzybek](https://github.com/krzysztof-grzybek)

"NULL", 흔히 "알 수 없는 누락된 값" 라고 표현합니다. Null은 존재하지 않는 무언가를 표현하기 때문에 특별한 처리를 하기 위해 종종 필요합니다.
NULL과 NULL의 산술 비교 결과가 NULL이기 때문에 하단의 예는 동작하지 않습니다.

```sql
1 = NULL, 1 <> NULL, 1 < NULL, 1 > NULL
```
, 그리고 심지어
```sql
NULL = NULL
```
숫자를 존재하지 않는 것과 어떻게 비교하거나 존재하지 않는 것을 존재하지 않는 것과 어떻게 비교하겠습니까?!
