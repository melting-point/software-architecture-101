# Chapter 7. 아키텍처 특성 범위

전통적으로 아키텍처 특성의 범위를 시스템 레벨에 두는 것을 당연시 여겼다.
공학 기술의 등장, 마이크로서비스 등의 아키텍처 스타일이 가능해지면서 아키텍처 특성의 범위는 좁아졌다.

어떤 아키텍처 스타일의 구조적인 진화 가능성을 측정할 기술이 필요했다.
기존의 측정 기술로는 상세한 수준까지 정확히 측정할 수 없었다.

앞선 장들에서 소개된 메트릭들은 모두 코드에 관한 저수준의 세부만 밝힐 뿐,
아키텍처 특성에 영향을 미치는 (데이터베이스 같은) *코드베이스 외부의 의존성*을 지닌 컴포넌트는 평가할 수가 없었다.

아무리 노력해도 시스템이 그런 특성에 부합하지 않는 데이터베이스를 사용하면 애플리케이션이 성공할 수 없다.

아키텍트는 운영 아키텍처 특성을 따져보고 아키텍처 특성에 영향을 미치는 *코드베이스 외부의 컴포넌트*를 잘 살펴봐야 한다.

# 커네이선스
두 컴포넌트 중 *한쪽이 변경될 경우 다른 쪽도 변경해야 전체 시스템의 정합성이 맞는다면* 이들은 *커네이선스*를 갖고 있는 것입니다.

> ! 커네이선스 = 연결성을 측정할 수 있는 방법

소프트웨어를 서로 엮는 것은 컴포넌트 레벨의 커플링만이 아니다.
많은 비즈니스의 개념이 의미상 여러 시스템 파트를 한데 엮어 기능적으로 응집되어 있다.

# 아키텍처 퀀텀
퀀텀 = 상호작용을 하는 모든 물리 입자 가운데 가장 작은 양

높은 기능 응집도와 동기적 커네이선스를 가진, 독립적으로 배포 가능한 아티팩트

## 독립적으로 배포 가능
단일 데이터베이스를 사용하는 레거시 시스템은 아키텍처 퀀텀 = 1
서비스 마다 데이터베이스가 따로 존재하는 마이크로서비스 아키텍처는 아키텍처 퀀텀 = N

## 높은 기능 응집도
응집도는 컴포넌트 설계에 따라 구현된 코드가 얼마나 목적에 맞게 통합되어 있는지를 나타낸다.

## 동기적 커네이선스
애플리케이션 콘텍스트 내부 또는 분산 서비스 간의 동기 호출을 의미한다.

동기 호출은 호출의 길이에 대해 동적 커네이선스를 만들어 낸다.
-> 한쪽이 다른쪽을 기다린다면  호출하는 도중에는 양쪽의 운영 아키텍처 특성이 동일해야한다.
-> 메세지 큐가 일시적인 버퍼 역할을 수행하도록 설계하면 비동기적 커네이선스 덕분에 아키텍처가 유연해 질 수 있다.





