# CCAAK 준비

Confluent Certified Administrator for Apache Kafka. 교재: **카프카 핵심 가이드 (2판)**.

## 시험 개요

90분, 60문항 내외, $150, Pass/Fail(점수 비공개), 객관식·매칭·순서 배열, 유효기간 2년.

| 도메인 | 비중 | 교재 매핑 |
|---|---|---|
| Cluster Configuration | 22% | 2, 6, 7, 12장 |
| Fundamentals | 15% | 1, 3, 4, 6장 |
| Security | 15% | 11장 |
| Troubleshooting | 15% | 7, 12, 13장 |
| Deployment Architecture | 12% | 2, 6, 10장 + KRaft |
| Kafka Connect | 12% | 9장 |
| Observability | 10% | 13장 |

> 시간·형식·유효기간은 Confluent 공식 페이지 기준. 문항 수·가격·비중은 서드파티 출처 여러 곳에서 일치하는 값(합계 101%라 반올림 오차 있음). 공식 시험 가이드(training.confluent.io)는 로그인/JS 페이지라 직접 확인 못 함. (2026-10-11 확인)

## 기록 방식

- 챕터 노트: `docs/ccaak/chNN-<주제>.md` — 개념 정리 + 시험 포인트 + 실습(kiwi-lab 클러스터)
- 일일 로그: `docs/log/YYYYMMDD.md` — 기존 형식 그대로 (복습 / 학습 / 퀴즈)

## 진도

| 장 | 제목 | CCAAK 관련도 | 노트 |
|---|---|---|---|
| 1 | 카프카 시작하기 | ★★ 기본 용어 | [미리보기](https://claude.ai/artifact/Pg6nPwxLVVgSaRd61iN7TH) · [ch01](ch01-getting-started.md) ✅ 21/30 |
| 2 | 카프카 설치하기 | ★★★ 브로커·토픽 설정 | [미리보기](https://claude.ai/artifact/9NdjZbmLhGm5Fuw9bmcMv5) 🔄 |
| 3 | 카프카 프로듀서 | ★★ acks, 배치, 재시도 | |
| 4 | 카프카 컨슈머 | ★★★ 그룹, 리밸런스, 오프셋 | |
| 5 | 코드로 카프카 관리하기 | ★ AdminClient | |
| 6 | 카프카 내부 메커니즘 | ★★★ 컨트롤러, 복제, 세그먼트, 컴팩션 | |
| 7 | 신뢰성 있는 데이터 전달 | ★★★ ISR, min.insync.replicas, unclean election | |
| 8 | 정확히 한 번 의미 구조 | ★★ 멱등성, 트랜잭션 | |
| 9 | 데이터 파이프라인 구축하기 | ★★★ Kafka Connect | |
| 10 | 클러스터 간 미러링 | ★★ MirrorMaker 2 | |
| 11 | 카프카 보안하기 | ★★★ SSL, SASL, ACL | |
| 12 | 카프카 운영하기 | ★★★ CLI 도구, 재할당, 설정 변경 | |
| 13 | 카프카 모니터링하기 | ★★★ 핵심 JMX 지표 | |
| 14 | 스트림 처리 | ★ | |

## 교재 밖에서 보강할 것

책(2판)은 ZooKeeper 기준이라 시험 범위와 차이가 있음.

- KRaft 모드 (컨트롤러 쿼럼, `process.roles`, 메타데이터 로그)
- Confluent 컴포넌트: Schema Registry, Control Center, RBAC
