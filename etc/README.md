# Chatting, 실시간 채팅

## 공통

### 참고

- https://engineering.linecorp.com/ko/blog/the-architecture-behind-chatting-on-line-live/

### 개념

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
