# 🎇 Unreal Niagara VFX Study Project

> **"실시간 이펙트의 원리를 이해하고 직접 구현하다."**  
>
> *Udemy 강의를 기반으로 Unreal Engine Niagara VFX 시스템을 학습하며 제작한 실습 프로젝트입니다.*

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

---

## 🎮 2. 개발 환경 (Environment)

* **Engine:** Unreal Engine 5 (Niagara VFX System)  
* **IDE:** Unreal Editor  
* **Language:** Blueprint 기반 설정 및 일부 C++ 구조 이해  
* **Platform:** Windows

---

## 🛠️ 3. 기술 스택 (Tech Stack)

### Engine & VFX
* **Niagara System**: 파티클 생성 및 제어
* **Niagara Emitter**: 개별 파티클 동작 정의
* **Material Editor**: 파티클 전용 머티리얼 제작
* **Curve / Parameter 제어**: 시간 기반 값 변화 제어

### Core Concepts
* Spawn Rate & Burst 제어
* Particle Lifetime 설정
* Color / Size / Velocity 모듈 커스터마이징
* Local / World Space 전환
* Dynamic Parameter 활용

---

## 💡 4. 주요 학습 내용 및 구조 (Features & Implementation)

### 4.1 Niagara System 구조 이해


Niagara System
└── Niagara Emitter
├── Spawn
├── Initialize Particle
├── Update
└── Render


* **System**: 여러 Emitter를 포함하는 상위 개념
* **Emitter**: 개별 파티클 로직 단위
* **Module Stack**: 각 단계별 동작 정의

---

### 4.2 Spawn & Lifetime 제어

* `Spawn Rate`를 통해 초당 생성 파티클 수 설정
* `Burst`를 통해 특정 순간 대량 생성
* `Lifetime` 설정으로 자연스러운 소멸 구현


---

### 4.3 Color & Size Over Life

* `Color Over Life` 모듈을 활용해 시간에 따른 색상 변화 구현
* `Scale Sprite Size`를 통해 점점 커지거나 줄어드는 효과 연출
* Curve Editor를 통해 자연스러운 페이드 아웃 구현

---

### 4.4 Velocity & Force 적용

* Initial Velocity로 방향성 부여
* Gravity Force로 자연스러운 낙하 효과 구현
* Drag 설정을 통해 공기 저항 표현

---

### 4.5 Material 연동

* Additive / Translucent 블렌딩 모드 활용
* Emissive Color를 통한 발광 효과 구현
* Dynamic Parameter를 통해 Niagara 값과 머티리얼 연결

---

## 📂 5. 프로젝트 구조 (Directory Structure)


Udemy_Unreal_NiagaraVFX/
├── Content/
│ ├── Niagara/
│ │ ├── Systems/
│ │ ├── Emitters/
│ │ └── Materials/
│ ├── Maps/
│ └── Blueprints/
├── Config/
├── Source/ (Optional)
└── Udemy_Unreal_NiagaraVFX.uproject


---

## 🚀 6. 트러블 슈팅 (Troubleshooting)

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

## 📚 7. 향후 공부 방향 (Future Study Plan)

* GPU Particle Simulation 심화 학습  
* 이벤트(Event Handler) 기반 파티클 시스템 구조 이해  
* Collision 및 Physics 연동 심화 학습  
* Blueprint 및 C++과 Niagara 간 데이터 바인딩 구조 학습  
* 실제 게임 이펙트(폭발, 스킬 이펙트, 환경 효과) 분석 및 재구현  
* 최적화 전략 및 퍼포먼스 프로파일링 학습  

---

**Contact:** (Your Name / Email)  
**GitHub:** https://github.com/KINGWONWOO/Udemy_Unreal_NiagaraVFX  
