# Chatting, 실시간 채팅

## 참고

- https://engineering.linecorp.com/ko/blog/the-architecture-behind-chatting-on-line-live/

## 개념

- Chat Server1에 접속된 Client 1이 코멘트를 보내고 그 코멘트가 Chat Server2에 접속된 Client 2로 전송
- websocket
- **pub/sub 구조**: 메시지를 생성하는 서비스를 해당 메시지를 처리하는 서비스에서 분리하는 확장 가능한 비동기 메시징 서비스
  - publisher가 메시지를 channel에 publish하면, subscriber가 publisher에 관계 없이 channel로 부터 해당 메시지를 받아서 처리(비동기, 많은 메시지 처리 가능)
- redis
- kafka
- message broker

## spring boot(java)

## Go(Golang)

# MSA

# Serverless 구조

## 개념
- 서버가 없는 서비스라는 사전적 의미지만 실제로는 서버가 존재하지만 서버를 관리할 필요가 없는 서비스, 즉 개발자는 서버를 신꼉쓰지 말고 비즈니스 로직에 집중하라는 의미
# JPA 설계
## 개념
### 들어가기 앞서
- 프로젝트를 진행했을 때 테이블 설계가 JPA에 어울리지 않아서, JPA를 사용하는데 어려움을 겪었다.
- JPA를 사용하면서 테이블 설계를 어떻게 해야 JPA에 적합한지 알아보고자 한다.

### Entity
- 개념: DB 테이블에 대응하는 하나의 클래스, 테이블 컬럼에 대응하는 필드를 가지고 있다, ***Annotation: @Entity***
- 단방향
- 양방향
    - 
