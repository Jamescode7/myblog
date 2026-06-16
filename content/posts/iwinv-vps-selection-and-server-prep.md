---
title: "iwinv VPS 선택 과정과 서버 준비 기록"
date: 2026-06-16T00:00:00+09:00
draft: true
description: "iwinv VPS를 선택한 이유와 Ubuntu 서버 초기 준비 과정을 정리합니다."
categories:
  - "DevOps"
tags:
  - "iwinv"
  - "VPS"
  - "Ubuntu"
  - "Server"
slug: "iwinv-vps-selection-server-prep"
---

# 문제

서비스 운영을 위해 어떤 VPS를 선택하고, 서버를 어떤 기준으로 준비할지 결정해야 했다.

# 환경

- OS:
- VPS 사양:
- 운영 예정 서비스:

# 원인 분석

비용, 성능, 국내 접속 속도, 관리 편의성, 확장 가능성을 함께 고려해야 했다.

# 해결 방법

## 비교 기준

- 월 비용
- CPU/RAM/디스크
- 국내 접속 지연 시간
- 서버 관리 콘솔
- 스냅샷 또는 백업
- 커스텀 도메인과 SSL 적용 난이도

## 초기 서버 준비

- SSH 키 기반 접속 설정
- 패키지 업데이트
- 기본 방화벽 설정
- Docker 설치 여부 검토
- Nginx 리버스 프록시 적용 여부 검토

# 결과

선택한 VPS와 초기 설정 결과를 기록한다.

# 배운 점

VPS 선택은 단순 가격 비교가 아니라 운영 방식과 장애 대응까지 포함한 의사결정이다.
