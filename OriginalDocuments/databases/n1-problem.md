# N + 1 문제

## [Krzysztof Grzybek](https://github.com/krzysztof-grzybek)

ORM 엔진에 따라 다르지만 일반적으로 `JOIN` 쿼리를 사용하는 것이 수정됩니다. 하이버네이트에서는 `join fetch`로 `INNER JOIN` SQL query의 결과를 냅니다.
