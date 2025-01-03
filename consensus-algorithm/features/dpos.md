# ☄️ Delegated Proof of Stake - 위임 지분 증명

## 1. DPoS란?
> - DPoS는 PoS의 변형 알고리즘으로, 토큰 보유자들이 대표자에게 자신의 스테이킹 권한을 위임하여 블록을 생성하고 네트워크를 운영하는 방식이다.
> - PoS의 확장성과 성능을 개선하기 위해 설계되었다.
> - 투표 기반의 민주적 블록체인 합의 알고리즘으로, 블록 생성자가 소수로 구성된다.
> - 대표자(Block Producer)는 토큰 보유자들의 투표로 선출된다.

## 2. DPoS 작동방식
### 1. 대표자(Delegate) 선출
- 네트워크 참여자는 코인을 스테이킹하고 투표를 통해 블록 생성 및 검증을 수행할 대표자를 선출한다.
- 많은 표를 얻은 상위 21~100명의 검증자가 블록 생성에 참여한다. But, 네트워크에 따라 수는 다르다.
- 대표자는 보상(=블록 생성 수수료)을 받고, 보상 중 일부는 투표자에게 나누어진다.

### 2. 블록 생성 과정
- 대표자가 선출되면, 라운드마다 순서대로 블록을 생성한다.
- 특정 시간 안에 블록을 생성하지 못하면 다음 대표자가 기회를 얻는다.
- 블록 생성 실패 시, 해당 대표자는 패널티를 받고 신뢰를 잃을 수 있다.

### 3. 보상 분배
- 블록을 생성한 대표자는 트랜잭션 수수료와 블록 보상을 받는다.
- 일부는 투표자(위임자)에게 분배된다.
- 이렇게 함으로써 토큰 보유자들은 직접 블록 생성에 참여하지 않고도 보상을 받을 수 있다.

## 3. DPoS의 장단점
### 장점
1. 빠른 블록 생성
   - 대표자 수가 적고, 빠르게 블록을 생성하므로 초당 트랜잭션수(TPS)가 매우 높다
   - 이오스는 초당 3000~4000TPS를 처리할 수 있다
2. 확장성
   - 소수의 검증자만 블록을 생성하기 떄문에 네트워크 확장성이 뛰어나다
   - 트랜잭션 병목 현상이 적다
3. 민주적 구조
   - 토큰 보유자들이 직접 투표하여 대표자를 선출한다
   - 대표자가 부적절한 행동을 하면 투표를 통해 교체 할 수 있다
4. 에너지 효율성
   - PoW와 달리 막대한 연산력과 전력이 필요하지 않다
   - 대표자는 가벼운 컴퓨터로 블록을 생성할 수 있다

### 단점 및 보안문제
1. 중앙화 문제
   - 소수의 대표자가 블록을 생성하기 때문에 중앙화의 위험이 존재한다
   - 21명의 대표자가 전체 네트워크를 운영하는 경우, 소수가 네트워크를 지배할 수 있다
2. 검열 위험
   - 대표자가 네트워크를 검열(트랜잭션 삭제) 할 가능성이 있다
   - 악의적인 대표자가 특정 트랜잭션을 의도적으로 포함하지 않을 수 있다
3. 51% 공격 위험
   - 소수의 대표자만 공격하면 네트워크가 장악될 수 있다
   - PoW에서의 51% 공격보다 훨씬 쉬운 공격이 가능하다 

## 4. DPoS vs Pos / PoW
|            | Proof of Work | Proof of Stake  | Delegated Proof of Stake |
|------------|---------------|-----------------|--------------------------|
| 블록 생성 방식   | 연산 경쟁(해시퍼즐)   | 지분에 비례하여 무작위 선출 | 선출된 대표자가 블록 생성           |
| 참여자        | 누구나 채굴 가능     | 누구나 검증자 가능      | 소수의 대표자(위임자 투표)          |
| 속도 및 확장성   | 느림(TPS 낮음)    | 누구나 검증자 가능      | 소수의 대표자(위임자 투표)          |
| 에너지 효율성    | 에너지 소모 큼      | 에너지 절약          | 에너지 절약                   |
| 탈중앙화 수준    | 높음            | 중간              | 낮음                       |
| 보안성        | 매우 높음         | 중간              | 중간                       |
| 51% 공격 난이도 | 매우 어려움        | 어려움             | 상대적으로 쉬움                 |


## 5. DPoS 적용 사례
### 1. EOS 이오스
- DPoS의 대표적인 사례로, 최대 21명의 대표자가 블록을 생성
- 빠른 트랜잭션 처리와 낮은 수수료가 강점
- 초당 3000~4000 TPS 처리 가능

### 2. TRON 트론
- EOS와 유사하게 DPoS 방식을 사용하며, 최대 27명의 대표자가 트랜잭션을 검증하고 블록을 생성한다
- 빠른 속도와 DApp 플랫폼을 운영하는데 적합하다

### 3. STEEM 스팀
- 블로그 및 SNS 기반 블록체인으로, 사용자가 컨텐츠를 생성하고 보상을 받는 시스템이다
- DPoS를 기반으로 한 빠른 트랜잭션 속도를 자랑한다 

## 6. DPoS의 역할과 미래
- DPoS는 빠른 트랜잭션 처리와 확장성을 제공하는 강력한 합의 알고리즘이다.
- 하지만, 중앙화의 위험이 존재하므로 검증자와 투표 시스템의 공정성이 중요하다.
- EOS, TRON, Steem과 같은 DPoS 기반 프로젝트는 속도와 효율성에서 큰 성과를 보이고 있다. 