# ☄️ Practical Byzantine Fault Tolerance - 실용 비잔틴 장애 허용

## 1. PBFT란?
> - PBFT(Practical Byzantine Fault Tolerance)는 분산 시스템에서 비잔틴 장애를 견딜 수 있도록 설게된 합의 알고리즘이다
> - 1999년 MIT의 미구엘 카스트로와 바바라 리스코프가 제안했다
> - 비잔틴 장군 문제를 해결하며, 네트워크 내 일부 노드가 악의적으로 동작하거나 오류를 일으켜도 전체 시스템이 안정적으로 운영될 수 있다
> - PBFT는 블록체인, 금융 시스템, 분산 데이터베이스 등 다양한 분야에서 사용된다

## 2. 비잔틴 장군 문제란?
비잔틴 장군문제 : `분산 시스템에서 일부 구성원이 악의적이거나 오류를 일으켜도, 나머지 구성원들이 합의에 도달할 수 있는가?`
- 장군들이 각각 다른 위치에서 적을 공격하거나 후퇴해야하는데, 일부 장군(=노드)이 배신하거나, 잘못된 정보를 전달할 경우 전체 작전이 실패할 수 있다.
- 해결책: PBFT는 네트워크에서 최대 1/3까지 비정상(악의적) 노드가 존재하더라도 정상적인 합의를 도출한다.

## 3. PBFT의 작동방식
### 1. 노드 구성
- Primary 노드 (리더) : 합의를 주도하는 노드
- Replica 노드 (팔로워) : 트랜잭션을 검증하고 Primary 노드가 제안한 블록에 동의

### 2. 기본 개념
- 3f + 1개의 노드가 필요로 한다
  - 여기서 f는 악의적인 노드 수이다
  - 예를 들어, f=1인 경우, 총 4개의 노드가 필요하다
- 최대 1/3의 비잔틴 노드가 존재해도 시스템은 정상적으로 동작한다

### 3. PFBT 합의 단계 (3단계 프로토콜)
1. Pre-Prepare 단계
   - Primary 노드가 클라이언트 요청을 받아 새로운 블록 생성을 제안한다
   - 제안된 블록은 모든 Replica 노드에게 전파된다
2. Prepare 단계
   - 각 Replica 노드는 Primary 노드가 보낸 블록을 검증한다
   - 블록에 문제가 없다면 OK 메세지를 다른 노드에게 전송한다
   - 2f + 1개의 OK 메세지를 받은 경우, 트랜잭션이 유효하다고 판단한다
3. Commit 단계
   - 모든 Replica 노드는 Commit 메세지를 서로 교환하여 최종 합의를 진행한다
   - 모든 노드가 Commit을 확인하면 블록이 블록체인에 추가된다

## 4. PBFT의 장단점
### 장점
1. 높은 보안성
   - 1/3 이하의 비잔틴 노드가 있어도 합의가 가능하다
   - 악의적인 노드가 있어도 전체 시스템이 마비되지 않는다
2. 빠른 트랜잭션 관리
   - PoW과 달리 연산 자원이 거의 필요하지 않다
   - 트랜잭션 속도가 빠르고, 에너지 효율적이다
3. 즉각적 확정성
   - 트랜잭션이 합의되면 즉시 확정되어 롤백이 불가능하다
   - 비트코인의 PoW와 달리 Fork가 발생하지 않는다

### 단점 및 한계
1. 노드 수가 많을수록 느려진다
   - PBFT는 노드 수가 많을수록 합의 과정이 느려진다
   - 네트워크 부하가 커지면 확장성 문제가 발생한다
2. Partial Synchrony가 필요하다
   - PBFT는 노드 간 부분 동기화를 전제로 한다
   - 노드간 통신이 지연되면 합의 실패가 발생할 수 있다
3. 과반수 공격 가능성
   - 전체 네트워크의 1/3 이상이 악의적이면 합의에 실패한다

