# 🎇 Unreal Niagara VFX Study Project

<img src="Udemy_Niagara.jpg" width="450" height="800" style="aspect-ratio: 9/16; object-fit: cover;" alt="Verification">

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

> *아래 링크를 클릭하면 유튜브에서 고화질로 시청할 수 있습니다. (YouTube)*

### Udemy 실습 영상

[YouTube : Udemy 실습 영상](https://youtu.be/xsyFOx90I90?si=NQGeRHLeelcNYJ8m)


https://github.com/user-attachments/assets/94a4fe2e-a478-4fb3-8f68-187adfe2173b



### 복습 Nier 영상
*   Udemy에서 배운 내용을 통해 자체적으로 제작한 영상입니다. Level 내 Mesh 들은 Blender를 통해 자체 제작했습니다.
  
[YouTube : Nier](https://youtu.be/FxfLJo7ZLfc?si=RFETOVWBMa0q3dNW)


https://github.com/user-attachments/assets/3899c8ec-9880-4aea-a706-4369c895f197


---

## 🛠️ 3. 사용 기술 (Tech Stack)

### Engine & Language
*   **Unreal Engine 5.6**: Core Engine (최신 기능 활용)
*   **Blueprints**: 파티클 전용 머티리얼 제작 / Niagara Spawn 설정
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

- [나이아가라 학습 노트 보기](https://github.com/KINGWONWOO/obsidian/blob/c01251f59885cd1a43de5cb84ea0f8255d3bb616/%EC%96%B8%EB%A6%AC%EC%96%BC%20%EA%B3%B5%EB%B6%80/Unreal/%EC%9D%BC%EC%9D%BC%20%EA%B3%B5%EB%B6%80/1-UE5%20C%20%20(24.06.25.~24.08.03.)/merged%20copy.md)

---


## 🚀 5. 트러블 슈팅 (Troubleshooting)

### 이슈 1: 메시 단면 렌더링 문제 (Two Side Error) (2024.06.28)
* 문제: 액터의 한쪽 면만 보이고 반대편은 투명하게 렌더링되는 현상.
* 해결: 해당 Mesh에 사용된 Material 설정에서 Two Sided 옵션을 활성화하여 양면 렌더링 적용.

### 이슈 2: 루멘(Lumen) 환경 내 머터리얼 일렁임 현상 (2024.11.04)
* 문제: 구식 머터리얼 사용 시 루멘의 빛 처리와 충돌하여 화면이 일렁이거나 깨지는 현상.
* 해결: 머터리얼 노드에서 Pixel Depth Offset 연결을 해제하여 루멘과의 연산 간섭 제거.

### 이슈 3: 나이아가라(Niagara) 미리보기와 레벨 내 출력 차이 (2024.11.25)
* 문제: 프레임 환경 차이로 인해 이펙트의 속도나 모양이 다르게 보이는 문제.
* 해결: Niagara System의 파란색 노드 설정에서 **고정된 틱 델타 시간(Fixed Tick Delta Time)**을 활성화하여 프레임 독립적인 시뮬레이션 환경 구축.

### 이슈 4: 파티클이 화면에 보이지 않는 문제
* 문제: 시스템 구성 후에도 뷰포트나 게임 내에서 파티클이 시각적으로 보이지 않는 현상.
* 해결: Spawn Rate가 0으로 설정되어 있는지 확인하고, 시스템 내 Sprite Renderer 모듈 존재 여부 및 Material의 정상 연결 상태를 점검하여 해결.

### 이슈 5: 파티클이 즉시 사라지는 현상
* 문제: 파티클이 생성되자마자 화면에서 바로 사라져 효과가 나타나지 않음.
* 해결: Lifetime 값이 0 또는 극소값으로 설정되었는지 확인 후, Random Range 설정을 적용하여 자연스러운 지속 시간(Duration) 부여.

### 이슈 6: 성능 저하 문제
* 문제: 다량의 파티클 스폰 시 FPS 드랍 및 렌더링 부하 발생.
* 해결: Spawn Rate 최적화 및 거리별 LOD(Level of Detail) 설정을 적용하고, 계산 집약적인 연산의 경우 GPU Simulation으로 전환하여 CPU 부하 분산.

---

## 📚 6. 공부 확장 방향(Future Study Plan)
* GPU Particle Simulation 심화 학습  
* 이벤트(Event Handler) 기반 파티클 시스템 구조 이해  
* Collision 및 Physics 연동 심화 학습  
* Blueprint 및 C++과 Niagara 간 데이터 바인딩 구조 학습  
* 실제 게임 이펙트(폭발, 스킬 이펙트, 환경 효과) 분석 및 재구현  
* 최적화 전략 및 퍼포먼스 프로파일링 학습  

---

**Contact:** (강원우 / king_wonwoo@naver.com)  
