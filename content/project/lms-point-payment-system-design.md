---
title: "LMS 포인트 결제 시스템 설계 기록"
date: 2026-06-16T00:00:00+09:00
draft: true
description: "LMS에서 포인트 결제 시스템을 설계할 때 고려한 데이터 모델과 예외 상황을 정리합니다."
categories:
  - "Project Log"
  - "Django"
tags:
  - "LMS"
  - "Django"
  - "Payment"
  - "Point"
slug: "lms-point-payment-system-design"
---

# 문제

LMS에서 포인트 충전, 사용, 취소, 환불 흐름을 안정적으로 설계해야 했다.

# 환경

- Backend:
- Database:
- Payment Provider:

# 원인 분석

포인트는 단순 숫자가 아니라 거래 이력, 정합성, 중복 요청 방지, 관리자 조정 내역을 함께 관리해야 한다.

# 해결 방법

## 핵심 모델

- 사용자 포인트 잔액
- 포인트 거래 이력
- 결제 요청
- 결제 승인 결과
- 환불 또는 취소 이력

## 예외 상황

- 중복 결제 콜백
- 결제 성공 후 서버 저장 실패
- 포인트 사용 후 주문 취소
- 관리자 수동 조정

# 결과

최종 데이터 모델과 API 흐름을 기록한다.

# 배운 점

결제 도메인은 성공 흐름보다 실패와 보정 흐름을 먼저 설계해야 한다.
