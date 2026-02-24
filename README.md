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

<details>
<summary>💻 옵시디언 공부 정리 - 접기/펼치기</summary>
<details>
<summary> 모듈 종류 정리 - 접기/펼치기</summary>
## Emitter Spawn
## Properties
- GPU Sprite 변경법 : Sim Target을 CPUCompute로 변경 후, Calculate Bound Volume을 Fixed로 변경
## Emitter Update
- Emitter State : Emitter의 수명을 결정(System/Self)
- Beam Emitter Setup : Beam의 시작과 끝/ Tangent 설정
- Spawn Burst Instantaneous : 한 번에 모든 Particle을 생성
- Spawn Rate : Rate를 통해 Particle의 생성 속도를 설정
- Spawn Particles in Grid : 육면체 안에 Particle을 Spawn
## Particle Spawn
- Initialize Particle : Paricle의 수명, 색깔, 크기 등의 다양한 속성을 설정
- Add Velocity : Particle에 속도를 부여해 이동시킴
- Shape Location : Particle을 Spawn하는 모양을 설정. Particle은 해당 모양 내에서 랜덤하게 생성
- Spawn Beam : Spline을 따라 빔 형태의 이펙트를 만드는 역할. 정확도를 설정
- Beam Width : Curve로 빔의 모양을 설정
- Sprite Facing and Velocity : 스프라이트의 Facing과 Alignment를 설정. 이를 적용 시키기 위해선. Sprite Renderer에서 Custom으로 바꿔야함.
- Grid Location : Spawn Particles in Grid에 사용되는 Grid 관련 설정
- Sample Texture : Texture 가져오기
- Static Mesh Location : Static Mesh의 형상으로 Particles 생성
- Initialize Mesh Reproduction Sprite : 움직이는 Mesh의 Particle 추적
- Set parameter : parameter를 직접 설정
## Particle Update
- Particle State : Particle의 재생이 끝날 시 삭제 설정
- Sprite Rotation Rate : 스프라이트가 시간에 따라 회전하며 각도를 입력 받음
- Scale Sprite Size : Particle의 크기를 설정. Curve를 통해 다양한 크기 변화 가능
- Scale Color : Particle의 RGBA값을 설정. A값에 변화를 줘 Fade 효과 적용 가능
- Forces : Particle에 힘을 가함
	- Curl Noise Force : 무작위 성의 힘을 부여
	- Point Attraction Force : 한 쪽 점으로 끌어당김. 블랙홀
	- Drag : 이동 방향 반대로 끌어당기는 힘. 이동을 줄여줌
	- Aerodynamic Drag : Drag의 업그레이드 버전으로 더욱 상세한 조정이 가능
	- Vortex Force : 특정한 축을 기준으로 회전
	- Wind Force : 바람의 힘을 적용 가능
	- Update Mesh Orientation(Rotation Rate) : 랜덤한 회전을 부여
	- Gravity Force : 중력 효과를 적용
	- Acceleration Force : 가속도 효과를 적용
- Scale Velocity : 입자의 속도를 증가 또는 감소 시켜줌.
- Scale Mesh Size : Mesh용으로 Mesh의 크기를 조정
- Solve Forces and Velocity : 힘이나 속도 관련 모듈 추가 시 필요한 종속 모듈
- Dynamic Material Parameters : 다이나믹 파라미터 설정
- Color : Scale Color와 같이 색깔을 조정하는 모듈. 단, Scale Color와 Color중 하나만 적용됨.
- Collison : Niagara에 충격 효과를 생성
- Sub UV Animation : FlipBook Texture를 통한 UV Animation 적용 시 필요한 모듈
- Kill Particles in Volume : Particle이 사용자 정의 Volume안에 들어오면 삭제
- Update Mesh Reproduction Sprite : 움직이는 Mesh의 Particle 업데이트트
- Lerp Particle Attributes : Module간에 Lerp 동작을 가능하게 해줌. 작동하지 않을 시 모듈 간 순서 변경해보기(강의에서는 Update Mesh Reproduction과 Solve Forces and Velocity간의 Position, Velocity 보간)

## Event Handler(Stage에서 Handler 추가 시 생성)
- Event Handler Properties : 이벤트를 받는 속성을 설정
- Receive {} Event : 이벤트를 받음
## Render
- Sprite Renderer : 카메라를 향하는 Renderer
- Mesh Renderer : Mesh처럼 작동하는 Renderer
- Ribbon Renderer : 이동 발생 시 페이드되는 잔상을 남기는 효과(캐릭터 돌진, 총탄 궤적 등)
</details>
</details>

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
