# ☄️ Proof of Stake - 지분 증명 

## 1. Proof of Stake란?
> - 블록체인에서 블록 생성 및 검증 권한을 코인의 보유량(지분)에 따라 부여하는 합의알고리즘
> - PoS는 PoW의 대안으로, 연산 자원이 아닌 코인 보유량에 따라 블록 생성 권한을 얻음
> - 블록 생성자는 채굴자(=Miner) 대신 검증자(=Validator)라고 부름
> - 많이 스테이킹(Staking) 할수록 블록 생성 가능성이 높아짐

## 2. PoS 작동 방식
### 1. 스테이킹(Staking) 과정
- 네트워크 참여자가 보유중인 암호화폐를 스테이킹한다
- 스테이킹된 코인은 일종의 담보 역할을 하며, 블록 검증 과정에 참여할 수 있는 자격을 부여한다

### 2. 블록 검증 및 생성
- PoW에서는 수학문제(해시 퍼즐)를 푸는 채굴 경쟁이 필요하지만, PoS에서는 많은 코인을 스테이킹한 검증자가 확률적으로 블록을 생성한다
- 운과 지분 크기에 따라 검증자가 선출된다. 즉, 많이 스테이킹 할수록 블록 생성 기회가 커진다

## 3. PoS 주요 개념
### 1. Validator - 검증자
- Validator(검증자)는 네트워크에 스테이킹하여, 트랜잭션 검증 및 블록 생성을 수행하는 역할을 한다
- 검증자는 정직하게 행동할 의무가 있으며, 악의적인 행동 시 스테이킹한 코인 일부를 잃을 수 있다

### 2. Slashing - 슬래싱
- 검증자가 악의적인 행동(이중 서명, 블록 조작 등)을 할 경우, 스테이킹 한 지분의 일부를 벌금(=소각)으로 잃는 방식이다
- 슬래싱은 네트워크 보안 및 검증자의 정직성을 보장하는 메커니즘이다

### 3. Random Selection - 랜덤 선택
- 블록 생성자는 무작위로 선택되지만, 스테이킹한 코인의 양이 많을수록 선택될 확률이 높아진다
- 공평성과 보안성을 확보하기 위한 방식이다

## 4. PoS의 장단점
### 장점
1. 에너지 효율성
   - PoS는 PoW보다 훨씬 적은 전력으로 네트워크를 유지할 수 있다
   - PoW의 환경문제(비트코인 전력 소모)를 해결한다 
2. 확장성
   - PoS는 PoW보다 더 빠른 트랜잭션 처리가 가능하다
   - 트랜잭션 속도가 빨라지고, 수수료도 낮아진다
3. 탈중앙화 유지
   - 누구나 코인을 보유하고 스테이킹하면 검증자가 될 수 있다
   - 하드웨어 성능에 의존하지 않기 떄문에 진입 장벽이 낮다

### 단점 및 보안문제
1. Nothing as Stake - 무위험 문제
   - 검증자가 여러 체인에서 동시에 블록을 생성하는 이중 서명 문제가 발생할 수 있다
   - PoW에서는 한 번에 하나의 체인만 작업할 수 있지만, PoS에서는 여러 체인을 검증해도 비용이 들지 않음
   - 해결책 : Slashing을 통해 이중 서명 시 검증자의 지분을 강제로 소각하다
2. 초기 부자 집중 문제
   - 많은 코인을 보유한 초기 검증자가 네트워크 권력을 독점할 가능성이 있다
   - 돈이 돈을 버는 구조로 이어질 수 있따
   - 해결책 : 랜덤 선택 및 검증자 순환을 통해 공정성을 확보한다 


## 5. PoW vs PoS
|            | Proof of Work          | Proof of Stake       |
|------------|------------------------|----------------------|
| 작동 방식      | 해시 퍼즐을 풀어 블록 생성        | 코인 보유량(지분)에 따라 블록 생성 |
| 자원 소모      | 높은 전력 소비(GPU, ASIC 필요) | 낮은 전력 소비(연산 자원 불필요)  |
| 보상 방식      | 채굴자(연산력 제공자)가 보상 획득    | 검증자(스테이킹한 자)에게 보상 제공 |
| 탈중앙화       | 채굴풀 집중 가능성(중앙화 위험)     | 지분 보유자 집중 가능성        |
| 환경 친화성     | 에너지 낭비 문제              | 친환경적(전력 소모 최소화)      |
| 확장성        | 낮음(TPS 제한)             | 높음(빠른 블록 생성 가능)      |
| 51% 공격 가능성 | 네트워크의 51% 해시 파워 필요     | 전체 코인의 51% 스테이킹 필요   |
| 보안성        | 높은 연산력 필요              | Slashing으로 보안성 확보    |


## 6. PoS의 실제 사례
### 1. 이더리움 2.0
- 이더리움은 2022년 PoW에서 PoW로 전환
- 이로인해 에너지 사용량이 99% 이상 감소
- 최소 32ETH를 스테이킹하면 검증자로 참여 가능

### 2. 솔라나
- 솔라나는 PoS + PoH(Proof of History) 방식
- 블록체인 내에서 시간을 기록하는 PoH와 PoS를 결합
- 트랜잭션 순서와 시간을 사전에 기록해 속도와 확장성을 극대화
- 초당 최대 5만 트랜잭션(TPS) 처리 가능

### 3. 폴카닷
- Nominated Proof of Stake
- 검증자와 추천자(Nominator)로 구성
- 추천자가 검증자에게 코인을 스테이킹 하여 신뢰할 수 있는 검증자 선출
- 하나의 검증자가 부적절한 행동을 하면 추천자도 함께 지분을 잃는 구조
- 검증자와 추천자 모두 네트워크 안정성에 기여
- 네트워크 보안 강화 및 스테이킹 보상 분배

### 4. 아발란체
- Snowman Consensus (눈사람 합의 알고리즘)
- PoS 기반이지만, 트랜잭션 검증 과정에서 병렬 처리를 통해 빠른 합의를 도출
- 하나의 체인에서 다양한 서브체인을 생성 가능
- 트랜잭션 처리가 즉각적으로 이루어지며, 거래 확정 속도는 1~2초 소요

### 5. 알고랜드
- Pure PoS 방식
- 네트워크에 참여하는 모든 사람이 검증자로 활동할 수 있음
- 순수 PoS 방식으로 누구나 동등하게 블록 생성 기회를 얻음
- 트랜잭션 확정 속도는 약 5초내외
- 고속 결제 시스템에 적합해 탈중앙화 및 보안성 강화에 탁월 

## 7. 결론
> - PoS는 블록체인의 지속 가능성을 높이고, 대규모 확장성 문제를 해결하는 핵심 기술로 주목받고 있다.
> - 환경 친화성 덕분에 다양한 신규 블록체인 프로젝트에서 PoS를 채택하고 있다.
> - PoS는 다양한 방식으로 발전해 왔으며, 속도, 확장성, 보안성을 향상시키기 위한 변형 알고리즘들이 등장하고 있다.
> - 프로젝트마다 검증자 선출 방식, 보상 시스템, 확장성 구조가 다르므로, 각 프로젝트의 PoS 방식은 네트워크 설계 철학에 따라 결졍된다.