## 챕터3 모듈성

### 모듈

- 복잡한 구조를 만드는데 쓰이는 각각의 표준화한 부품이나 독립적 단위
    - 개발자 기준 보통 연관된 코드를 함께 묶는 수단으로 모듈을 사용

### 모듈성 측정

- 응집
- 커플링
- 커네이선스

### 응집

- 모듈의 구성요소가 동일 모듈에 얼마나 포함되어있는지
    - 모듈 구성 파트가 각각 얼마나 연관되어 있는지
- 이상적이라면 모든 파트가 함께 패키징
- 응집도의 측정범위
    - 기능적응집
    - 순차적응집
    - 소통적응집
    - 절차적응집
    - 일시적응집
    - 논리적응집
    - 동시적응집

### 커네이선스

- 구심/원심 커플링 메트릭을 더욱 발전시긴 개념
    - 한쪽이 변경될때 다른쪽도 변경되어야 한다면 커네이선스를 갖고 있는것
- 정적 커네이선스
    - 소스레벨의 커플링
        - 명칭 커네이선스
        - 타입 커네이선스
        - 의미 커네이선스(관례)
        - 위치 커네이선스
        - 알고리즘 커네이선스
- 동적 커네이선스
    - 실행커네이선스
        - 실행순서 의존
    - 시점 커네이선스
        - 컴포넌트의 실행 순서 의존
    - 값 커네이선스
    - 식별 커네이선스

### 커네이선스의 속성

- 강도
    - 커네이선스를 얼마나 쉽게 리펙터링 할수 있는지에 따라 강도가 결정됨
    - 보통 아키텍트는 동적 커네이선스 보다 정적을 선호함
    - 동적 커네이선스를 정적으로 리팩터링 하면 커네이선스를 개선한것
- 지역성
    - 모듈들의 근접도
    - 모듈을 서로 떨어뜨렸을때 커플링이 형편없다면 이걸 붙임으로서 개선해나가는것
- 정도
    - 커네이선스가 미치는 영향의 규모