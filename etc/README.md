# ETC

- 토이 프로젝트를 진행하면서 배우는 지식들 정리

---

# Chatting, 실시간 채팅

## 참고

- https://engineering.linecorp.com/ko/blog/the-architecture-behind-chatting-on-line-live/

## 개념

- Chat Server1에 접속된 Client 1이 코멘트를 보내고 그 코멘트가 Chat Server2에 접속된 Client 2로 전송
- websocket
- **pub/sub 구조**: 메시지를 생성하는 서비스를 해당 메시지를 처리하는 서비스에서 분리하는 확장 가능한 비동기 메시징 서비스
  - publisher가 메시지를 channel에 publish하면, subscriber가 publisher에 관계 없이 channel로 부터 해당 메시지를 받아서 처리(비동기, 많은 메시지 처리 가능)
- message broker
  - redis
  - kafka

## spring boot(java)

## Go(Golang)

# MSA

## 개념

- Micro Service Architecture의 약자로, 하나의 애플리케이션을 여러 개의 작은 서비스로 나누어 개발하는 방법론
- 각각의 서비스는 독립적으로 개발, 배포, 운영이 가능하다.
- 모노리틱 아키텍처가 서비스간의 호출이 하나의 프로세스 내에서 이루어지기 때문에 속도가 빠르지만 MSA의 경우 서비스간 호출을 API통신을 이용하기 때문에 속도가 느리고, 통신에 사용하기 위해 값을 데이터 모델로 변환시켜주는 오버헤드가 발생하기도합니다.
- **데이터 분리**: 데이터 저장 시 하나의 DB에 중앙 집중화를 하지 않고 서비스 별 별도의 데이터 베이스를 사용합니다.
- **API Gateway**: MSA의 문제점 중 하나는 각 서비스가 다른 서버에 분리 배포되어있기 때문에 서버 URL이 각기 다를 수 밖에 없습니다. 이때 API Gateway는 API 서버 앞 단에서 모든 API 서버들의 End-Point를 단일화하여 묶어주는 역할을 합니다.

# Serverless 구조

## 개념

- 서버가 없는 서비스라는 사전적 의미지만 실제로는 서버가 존재하지만 서버를 관리할 필요가 없는 서비스, 즉 개발자는 서버를 신꼉쓰지 말고 비즈니스 로직에 집중하라는 의미

# JPA 설계

## 개념

### 들어가기 앞서

- 프로젝트를 진행했을 때 테이블 설계가 JPA에 어울리지 않아서, JPA를 사용하는데 어려움을 겪었다.
- JPA를 사용하면서 테이블 설계를 어떻게 해야 JPA에 적합한지 알아보고자 한다.

### Entity

- 개념: DB 테이블에 대응하는 하나의 클래스, 테이블 컬럼에 대응하는 필드를 가지고 있다, **_Annotation: @Entity_**
- OnToOne, OneToMany, ManyToOne, ManyToMany
  - OneToOne: 1:1 관계
  - OneToMany: 1:N 관계
  - ManyToOne: N:1 관계
  - ManyToMany: N:M 관계
- 단방향
- 양방향
  - .
