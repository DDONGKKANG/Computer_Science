# 트랜잭션 스케줄

## 트랜잭션 스케줄
정의 : 트랜잭션들을 구성하는 연산들의 실행 순서를 의미
- 트랜잭션이 갖고 있는 모든 연산들을 포함한다. 
- 즉, 스케줄은 트랜잭션의 집합이다.
- 스케줄안에서 각 트랜잭션의 본래 순서는 보존되어야 한다.

### 직렬 스케줄 (Serial Schedule)
트랜잭션의 연산을 모두 순차적으로 실행하는 스케줄을 의미
- 하나의 트랜잭션이 실행되면 해당 트랜잭션이 완료되어야 다른 트랜잭션이 실행 가능하다.

### 비직렬 스케줄 (Nonserial Schedule)
트랜잭션의 직렬 수행 순서와 상관없이 병행 수행하는 스케줄을 의미
- 한 트랜잭션이 진행중인 상황에서 다른 트랜잭션이 실행 가능하다.

### 직렬 가능 스케줄 (Serializable Schedule)
서로 영향을 주지 않는 직렬 스케줄을 비직렬적으로 수행하는 스케줄을 의미

## Concurrent Execution (동시 다발적 수행)
1. throughput 증가한다. (단위 시간당 몇 개의 트랜잭션 처리)
2. average response time 감소한다.
3. isolation 보장해야 한다.
4. consistency는 보장해야 한다. 

## Serializability (직렬가능성)
정의 : Concurrent 실행으로 트랜잭션을 처리해도 직렬하게 처리했을 때와 결과가 같을 수 있는가?

### serializable하다
serial 스케줄들 중에 하나와 결과가 같으면 serializable하다고 한다.
- 하나하나 비교하기에는 비용이 너무 많이 들어서 두가지 관점으로 이 두가지 조건이 맞으면 serializable하다고 판단한다.
  - Conflict serializability : 위치 바꿔서 Serial Schedule 만들기 가능하면 O
  - View serializability : 조건 3개 만족하면 O

### Non Serializable Execution 의 대표적인 3가지 문제
1. dirty read
2. lost update
3. unrepeatable read

### Conflict Serializable Schedule
- Conflict equivalent <br>
    : 스케줄 S의 비충돌연산들(read, 다른 item에 read,write) 위치를 바꾸어서 만들어 내는 스케줄 S’는 S와 동일한 스케줄이다.  이때 S와 S’은  Conflict equivalent를 만족한다.
- Conflict serializable <br>
    : Conflict equivalent를 이용하여 직렬화 스케줄을 만들수 있으면 Conflict serializable하다고 한다

### How to Test Serializability
Conflict Serializability 검사
- 선형 그래프(precedence graph) 이용
  - 방향이 존재하는 그래프 사용
  - 충돌이 있는 경우(rw, wr, ww)에 선을 그리며 먼저 데이터에 접근한 트랜잭션 방향에서 시작하여 그 후에 접근한 트랜잭션으로 도착하게 그린다.
- 사이클이 존재하면 not conflict serializability하다.
- **사이클이 존재하지 않으면 conflict serializability하다.**