# 🌍 Layer 1 & Layer 2 블록체인 솔루션

## 🔎 Layer 1과 Layer 2 이해하기
### 🧩 Layer 1 (기본 블록체인 네트워크)
- Layer 1은 블록체인의 기본 레이어로, 비트코인, 이더리움, 솔라나, 폴카닷 등 자체적인 네트워크를 운영하는 독립적인 블록체인 플랫폼이다
- 기능: 트랜잭션 검증, 합의 알고리즘, 스마트 컨트랙트 실행
- 확장성 문제: 네트워크 사용자가 많아지면 속도가 느려지고 가스비용(트랜잭션 비용)이 증가한다
- 예시: 비트코인, 이더리움, 솔라나, 폴카닷, 아발란체 

### 🧩 Layer 2 (확장 솔루션)
- Layer 2는 Layer 1의 부하를 덜어주기 위한 확장 솔루션이다
- Layer 1 위에서 동작하며, 트랜잭션을 Layer 2에서 처리한 후, 최종 결과만 Layer 1에 기록한다
- 속도 향상, 가스비 절감, 확장성 강화가 목표이다
- 예시
  - 비트코인: 라이트닝 네트워크(Lightning Network)
  - 이더리움: Optimistic Rollup, zk-Rollup, Arbitrum, Polygon

## ⚖️ Layer 1과 Layer 2 비교하기
||Layer 1| Layer 2                               |
|--|--|---------------------------------------|
|기본 개념|블록체인의 기본 네트워크| Layer 1위에서 동작하는 확장 네트워크               |
|트랜잭션 처리 방식|직접 블록에 기록| Layer 2에서 처리 후 Layer 1에 기록            |
|속도|상대적 느림| 빠름                                    |
|트랜잭션 비용|높음| 저렴                                    |
|확장성|제한적| 무제한(이론적으로)                            |
|보안성|Layer 1 자체 보안| Layer 1 보안에 의존                        |
|스마트 컨트랙트|직접 실행| Layer 2에서 실행 후 Layer 1에 기록            |
|사용 사례 |비트코인, 이더리움, 솔라나, 폴카닷| 라이트닝 네트워크, Arbitrum, zkSync, Polygon  |

## 📦 Layer 1 주요 플랫폼과 특징
### 1. 비트코인
- 목표: 디지털 금, 가치 저장
- 합의 알고리즘: PoW
- 확장성 문제: 7TPS -> Layer2 (라이트닝 네트워크)로 해결중
- Layer 2 솔루션: Lightning Network

### 2. 이더리움
- 목표: 스마트 컨트랙트 플랫폼, DApp, DeFi
- 합의 알고리즘: PoS
- 확장성 문제: 15~30 TPS -> Layer 2 Rollup으로 해결중
- Layer 2 솔루션
  - Optimistic Rollup (Optimism, Arbitrum)
  - zk-Rollup (zkSync, StarkNet)
  - Polygon (사이드체인 기반 L2)

### 3. 솔라나
- 목표: 초고속 트랜잭션 처리 (65000 TPS)
- 합의 알고리즘: PoS + PoH
- 확장성 문제: Layer 1에서 직접 처리 (Layer 2 필요성 낮음)
- Layer 2 솔루션: 없음 (Layer 1에서 확장성 해결)

### 4. 폴카닷
- 목표: 체인 간 상호운용성
- 합의 알고리즘: NPoS
- 확장성 문제: Parachain을 통해 확장성 확보
- Layer 2 솔루션: Parachain 자체가 Layer 2 역할

## 🚊 Layer 2 주요 솔루션 및 특징
### 1. 라이트닝 네트워크 - 비트코인
- 특징: 비트코인의 확장성을 해결하는 Layer 2 솔루션
- 트랜잭션 방식: 소규모 거래에서는 Layer 2에서 처리, 최종 정산만 Layer 1에 기록
- 장점: 수수료가 거의없고 초당 수천건의 트랜잭션 처리가 가능하다

### 2. Optimistic Rollup - 이더리움
- 특징: 트랜잭션이 정상이라고 가정하고 Layer 2에서 처리, 이의 제기(챌린지) 기간에 검증
- 주요 프로젝트: Optimism, Arbitrum
- 장점: EVM 호환성 높음
- 단점: 트랜잭션 최종 확정까지 1~2주 지연

### 3. zk-Rollup - 이더리움
- 특징: 트랜잭션을 암호학적 증명(SNARK/STARK)으로 검증 후 Layer 1에 기록
- 주요 프로젝트: zkSync, StarkNet, Polygon zkEVM
- 장점: 빠르고 보안성이 높고, 즉시 트랜잭션이 확정된다(챌린지 기간 없음)
- 단점: 개발 복잡성 높음

## 🛠️ Layer 1과 Layer 2의 상호작용
### Layer 1 (이더리움 메인넷)
- NFT 민팅하거나 대규모 거래를 처리할 때 사용
### Layer 2 (Optimism, zkSync)
- NFT 전송, 소규모 결제, DeFi 거래

## 🚀 Layer 1과 Layer 2 선택 기준
### 1. Layer 1 사용 추천 상황
- 대규모 자산 이동
- 보안성이 중요한 상황(NFT 민팅, 스마트 컨트랙트 배포 등)
- 스마트 컨트랙트 초기 개발 단계

### 2. Layer 2 사용 추천 상황
- 소규모 트랜잭션(DeFi, 게임, NFT 전송 등)
- 거래량이 많은 애플리케이션
- 트랜잭션 비용을 절감하고 싶은 경우 

## 결론
> - Layer 1은 보안성과 탈중앙화에 집중
> - Layer 2는 확장성과 트랜잭션 비용 절감에 기여 