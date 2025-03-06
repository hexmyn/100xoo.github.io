---
layout: single
title: RedHat Container Day Checklist
categories: Linux
tags:
  - Linux
  - RedHat
  - Cloud Native
  - OpenShift
  - Seminar
toc: true
---

주제 : **클라우드 네이티브, 오픈시프트, AI 플랫폼**

## 🔎 사전 공부 키워드 & 가이드

### 1. 클라우드 네이티브 기본 개념

> **핵심 키워드**: 마이크로서비스, 컨테이너, DevOps, CI/CD, Kubernetes

- 클라우드 네이티브 아키텍처란?
- 모놀리식 vs 마이크로서비스
- Kubernetes와 컨테이너 오케스트레이션 기본 개념
- DevOps에서 클라우드 네이티브가 왜 중요한가?
- GitOps 개념도 간단히 알아두면 좋음

📚 참고: CNCF 클라우드 네이티브 정의 → [https://www.cncf.io/about/faq/](https://www.cncf.io/about/faq/)



---

### 2. OpenShift의 특징과 주요 기능

> **핵심 키워드**: 엔터프라이즈 Kubernetes, DevOps 툴체인 내장, 하이브리드 클라우드 대응

- OpenShift가 일반 쿠버네티스와 어떤 차이가 있는지
- OpenShift가 제공하는 **개발자 경험(DevEx)** 강화 기능 (GUI, CLI, 파이프라인 내장 등)
- **OpenShift Virtualization**: VM까지 OpenShift 위에서 관리하는 기능 (이번 행사 주요 포인트)

📚 참고: [https://www.redhat.com/ko/technologies/cloud-computing/openshift](https://www.redhat.com/ko/technologies/cloud-computing/openshift)

---

### 3. 클라우드 네이티브 가상화 (OpenShift Virtualization)

> **핵심 키워드**: VM과 컨테이너 혼합 운영, 기존 시스템 모던화 브릿지

- 기존 VM 환경을 어떻게 컨테이너 환경으로 자연스럽게 옮기는지
- OpenShift Virtualization의 구조 (KubeVirt 기반)
- VM을 컨테이너처럼 관리하는 방식 (CI/CD 적용 가능성 등)

📚 참고: [https://www.redhat.com/ko/technologies/cloud-computing/openshift/virtualization](https://www.redhat.com/ko/technologies/cloud-computing/openshift/virtualization)

---

### 4. 미들웨어의 클라우드 네이티브 전환

> **핵심 키워드**: 서비스 메시, API Gateway, 데이터 스트리밍 (Kafka), 이벤트 기반 아키텍처

- 기존 미들웨어 (WAS, ESB 등) vs 클라우드 네이티브 시대의 미들웨어
- 서비스 메시 (Istio 등)와 미들웨어 역할 변화
- API 관리 (Red Hat 3scale 등)
- 이벤트 기반 아키텍처와 스트리밍 (Kafka)

---

### 5. AI 네이티브 플랫폼 (Red Hat AI)

> **핵심 키워드**: AI/ML 모델 배포 자동화, MLOps, 데이터 플랫폼과의 연계

- AI 플랫폼을 왜 클라우드 네이티브 아키텍처로 구성하는가?
- MLOps에서 OpenShift의 역할 (학습-배포-운영 사이클)
- Red Hat OpenShift AI 개념
- AI 서비스도 쿠버네티스에서 관리하는 흐름 이해

📚 참고: [https://www.redhat.com/ko/technologies/cloud-computing/openshift/ai](https://www.redhat.com/ko/technologies/cloud-computing/openshift/ai)

---

### 6. 레드햇의 전략 키워드

> **핵심 키워드**: 하이브리드 클라우드, 오픈소스 혁신, 엔터프라이즈 지원

- 레드햇이 강조하는 오픈소스 기반 하이브리드 클라우드 전략
- AWS, Azure, GCP 등 퍼블릭 클라우드와의 관계
- Red Hat과 IBM의 협업 포인트 (특히 AI 분야에서)

---

## 📋 요약 추천 흐름

|주제|추천 준비 내용|
|---|---|
|클라우드 네이티브|기본 개념, 아키텍처 구성 요소|
|OpenShift|OpenShift의 특징과 차별점|
|가상화|VM과 컨테이너의 통합 운영 사례|
|미들웨어|서비스 메시, API 관리, 이벤트 처리 흐름|
|AI|MLOps와 클라우드 네이티브 AI 플랫폼|

---

## 💡 질문거리

- 기존 레거시 VM을 OpenShift로 전환할 때 실제 고객들이 가장 어려워하는 포인트는?
- OpenShift Virtualization이 다른 VM 관리 솔루션과 차별화되는 강점은?
- 클라우드 네이티브 환경에서 AI 플랫폼을 구축할 때, 데이터 파이프라인이나 모델 배포 자동화에서 OpenShift가 어떻게 기여하는가?
- 서비스 메시와 미들웨어의 역할 분담은 어떻게 정리하는 게 좋은가?

