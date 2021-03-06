# 02_운영체제의 역사

## 일괄 작업 시스템(batch processing system)
- 작업에 필요한 프로그램과 데이터를 동시에 입력
- 모든 작업을 한꺼번에 처리
- 프로그램 실행 중간에 사용자가 데이터를 입력, 수정이 불가
## 대화형 시스템(interactive system)
- 작업 중간에 사용자가 입력 가능
- 사용자에게 중간 결과값 보여줄 수 있음
- 단점: 작업시간을 예측하기 힘들다
## 시분할 시스템
- 다중 프로그래밍(multiprogramming)
- time sharing system = multitasking system
    - CPU 사용 시간을 잘게 쪼개어 작업들에게 나누어줌 그럼 영화필름 돌아가는거 마냥 동시에 실행되는 것 처럼 보임
- 단점: 일정 시간 안에 끝나는 것을 보장하지 못함
    - 이에 real time system 사용: 특정 시스템에서 일정 시간 안에 작업이 처리되도록 보장
- 여러 작업을 동시에 실행할수 있다: 한 사람이 여러 프로그램을 동시에 실행 가능, 여러 사람이 동시에 작업 가능
## 분산 시스템
- 네트워크상에 분산되어 있는 여러 컴퓨터로 작업을 처리하고 그 결과를 상호 교환하도록 구성한 시스템, TCP/IP 개념 나옴
## 클라이언트/서버 시스템
- 작업을 요청하는 클라이언트와 거기에 응답하여 요청받은 작업을 처리하는 서버의 이중 구조
- 단점: 서버 과부화
- 데몬: 서버가 멈추지 않고 동작해서 클라이언트 요청을 처리하기 위한 프로그램
    - 데몬을 가진 컴퓨터가 서버가 되는 것
    - 아파치 톰캣이 웹 데몬의 역할을 한다.
## P2P 시스템
- peer-to-peer system
- 사용자의 컴퓨터가 peer(말단 노드) 역할을 하며 서버를 거치지 않고 사용자와 사용자를 직접 연결하는 것
- 서버가 없는, 서버가 있는 P2P로 나뉜다.
- 서버가 없는게 블록체인이라 생각하면 된다.

## 기타 컴퓨팅 환경
- 그리드 컴퓨팅
- 클라우드 컴퓨팅: 그리드 + SaaS