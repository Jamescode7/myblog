---
title: "Flutter 키보드가 자동으로 닫히지 않는 문제 해결"
date: 2026-06-16T00:00:00+09:00
draft: true
description: "Flutter 입력 화면에서 키보드 종료가 어색하게 동작한 문제와 해결 과정을 정리합니다."
categories:
  - "Troubleshooting"
  - "Flutter"
tags:
  - "Flutter"
  - "Keyboard"
  - "FocusNode"
slug: "flutter-keyboard-dismiss-issue"
---

# 문제

입력 화면에서 외부 영역을 터치해도 키보드가 기대한 방식으로 닫히지 않았다.

# 환경

- OS:
- Flutter:
- Dart:
- 대상 플랫폼:

# 원인 분석

포커스 해제 처리, 스크롤 뷰 구조, GestureDetector 적용 범위를 확인한다.

# 해결 방법

- 현재 포커스 상태 확인
- 외부 터치 시 `FocusScope.of(context).unfocus()` 적용
- 스크롤 영역과 입력 필드의 제스처 충돌 확인

# 결과

수정 후 입력 화면에서 키보드 종료 동작이 자연스럽게 개선되었다.

# 배운 점

모바일 입력 UX는 작은 포커스 처리 차이로 사용성이 크게 달라진다.
