# 6장 아키텍처 특성의 측정 및 거버넌스

## 아키텍처 특성 측정

- 물리학이 아니다
- 정의가 너무 다양하다
- 너무 복합적이다

### 운영적 측정

- 달성하기 어려운 성능 수치를 정하는 대신, 통계 분석 결과로 얻은 나름대로의 정의에 기반

### 구조적 측정

- 순환 복잡도 측정

### 프로세스 측정

- 시험성, 배포성 등을 측정

## 거버넌스와 피트니스 함수

### 아키텍처 특성 관리

- 아키텍처 거버넌스는 아키텍트가 영향력을 행사하려는 모든 소프트웨어 개발 프로세스를 포괄

### 피트니스 함수

- 결과가 목표에 얼마나 근접했는지를 나타내는 목표 함수
- 아키텍처 피트니스 함수: 어떤 아키텍처 특성의 객관적인 무결성을 평가하는 모든 메커니즘
- 순환 의존성: 순환 참조가 발생하는지 테스트하는 피트니스 함수가 필요
- ‘메인 시퀀스로부터의 거리’ 피트니스 함수: 임계치를 설정하고 클래스가 이 범위를 벗어나는지 테스트하는 피트니스 함수가 필요

## 부가 내용

- [oreil.ly/usx7p와](http://oreil.ly/usx7p와) 같은 주소로 접근 시 위키피디아로 이동되는데 301 redirect를 시켜준다.

## 논의하면 좋을 것

- [https://kurly0521.atlassian.net/wiki/spaces/DO/pages/3496936175/SonarCloud+Project+Metric](https://kurly0521.atlassian.net/wiki/spaces/DO/pages/3496936175/SonarCloud+Project+Metric)
- [https://github.com/kisstkondoros/codemetrics](https://github.com/kisstkondoros/codemetrics)
- [https://github.com/kisstkondoros/tsmetrics-core](https://github.com/kisstkondoros/tsmetrics-core)