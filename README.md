# 🎇 Unreal Niagara VFX Study Project

![Verification](Doc/Images/Udemy_Niagara.png)

> **"실시간 이펙트의 원리를 이해하고 직접 구현하다."**  
>
> Udemy 강의 **'Unreal Engine 5 : 강의 하나로 Niagara VFX 완벽 마스터하기!'**를 기반으로 Unreal Engine Niagara VFX 시스템을 학습하며 제작한 실습 프로젝트입니다.

---

## 📋 1. 프로젝트 개요 (Overview)

* **프로젝트명:** Udemy Unreal Niagara VFX Study  
* **유형:** Unreal Engine 기반 실시간 VFX 학습 프로젝트  
* **개발 인원:** 1인 개발  
* **개발 목적:** Niagara 시스템의 구조 및 모듈 동작 원리 학습  
* **주요 특징:**  
    * Unreal Engine의 **Niagara System**을 활용한 파티클 이펙트 제작  
    * Emitter / System 구조 이해 및 커스터마이징  
    * Material과 연계한 실시간 시각 효과 구현  
    * 실습 중심의 단계별 VFX 제작
    * 강의 복습을 위한 개인 작품 제작

---
## 🎥 2. 실습 영상 (Practice Video)

> *아래 이미지를 클릭하면 영상을 시청할 수 있습니다. (YouTube)*

### Udemy 실습 영상

[![Gameplay Video](https://img.youtube.com/vi/YOUR_VIDEO_ID/0.jpg)](https://www.youtube.com/watch?v=YOUR_VIDEO_ID)

### 복습 Nier 영상
*   Udemy에서 배운 내용을 통해 자체적으로 제작한 영상입니다. Level 내 Mesh 들은 Blender를 통해 자체 제작했습니다.
  
[![Gameplay Video](https://img.youtube.com/vi/YOUR_VIDEO_ID/0.jpg)](https://www.youtube.com/watch?v=YOUR_VIDEO_ID)

---

## 🛠️ 3. 사용 기술 (Tech Stack)

### Engine & Language
*   **Unreal Engine 5.6**: Core Engine (최신 기능 활용)
*   **C++ & Blueprints**: 파티클 전용 머티리얼 제작 / Niagara Spawn 설정
*   **Camera Sequencer**: 몰입감 있는 시네마틱 카메라 연출

### Modeling
*   **Blender**: Mesh 생성

### Core Concepts
* Spawn Rate & Burst 제어
* Particle Lifetime 설정
* Color / Size / Velocity 모듈 커스터마이징
* Local / World Space 전환
* Dynamic Parameter 활용

---

## 💡 4. 주요 학습 내용 (Features)

- [나이아가라 학습 노트 보기]([언리얼 공부/Unreal/일일 공부/1-UE5 C  (24.06.25.~24.08.03.)/merged copy.md])

---


## 🚀 5. 트러블 슈팅 (Troubleshooting)

### 이슈 1: 파티클이 화면에 보이지 않는 문제
* Spawn Rate가 0으로 설정되었는지 확인
* Sprite Renderer가 추가되어 있는지 확인
* Material이 정상적으로 연결되었는지 확인

### 이슈 2: 파티클이 즉시 사라지는 현상
* Lifetime 값이 0 또는 너무 작게 설정되었는지 확인
* Random Range 설정으로 자연스러운 지속 시간 부여

### 이슈 3: 성능 저하 문제
* Spawn Rate 최적화
* LOD 설정 적용
* GPU Simulation과 CPU Simulation 구분 사용

---

## 📚 6. 향후 공부 방향 (Future Study Plan)

* GPU Particle Simulation 심화 학습  
* 이벤트(Event Handler) 기반 파티클 시스템 구조 이해  
* Collision 및 Physics 연동 심화 학습  
* Blueprint 및 C++과 Niagara 간 데이터 바인딩 구조 학습  
* 실제 게임 이펙트(폭발, 스킬 이펙트, 환경 효과) 분석 및 재구현  
* 최적화 전략 및 퍼포먼스 프로파일링 학습  

---

**Contact:** (Your Name / Email)  
**GitHub:** https://github.com/KINGWONWOO/Udemy_Unreal_NiagaraVFX  
