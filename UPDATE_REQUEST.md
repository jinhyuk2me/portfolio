# 포트폴리오 내용 업데이트 요청 양식

원하시는 변경 사항을 **한글로만** 작성해 주세요. 
작성 후 저에게 "반영해줘"라고 말씀하시면, 제가 영어로 번역하여 `hugo.yaml` 설정에 일괄 적용해 드립니다.

---

## 🎯 메인 화면 (Hero Section)

### 한글 버전
- **Intro**: Control with Perception
- **Title**: 로보틱스 AI 엔지니어
- **Subtitle**: 장진혁
- **Content**: Combining robot control and AI perception to build autonomous systems that work in the real world.

### 영문 버전
- **Intro**: Hello, I am
- **Title**: Jinhyuk Jang.
- **Subtitle**: Full-Stack Robotics & AI System Architect
- **Content**: I design and build complete autonomous systems—from low-level robot control to AI perception and central management servers.

---

## 🚀 프로젝트 (Projects)

### Shopee: 로봇 쇼핑 시스템
- **제목**: Shopee: 로봇 쇼핑 시스템
- **설명**: 
  - 다중 자율주행 로봇 쇼핑 시스템입니다. 
  - 로봇들이 직접 진열대로 이동해 물건을 픽업하고 배달합니다. 
  - ROS2 아키텍처와 FSM 기반 관제, 중앙 서버 제어가 포함되어 있습니다.
- **이미지 경로**: /images/projects/shopee_banner.jpg
- **사용 기술**: [ROS 2, Nav2, Multi-Robot]
- **GitHub 링크**: https://github.com/jinhyuk2me/Shopee

### Roomie: 호텔 배송 로봇
- **제목**: Roomie: 호텔 배송 로봇
- **설명**: 
  - **[개요]** 층간 이동과 정밀 배송이 가능한 자율주행 룸서비스 로봇입니다. 단순 주행을 넘어, 로봇팔을 이용한 엘리베이터 버튼 조작 및 IoT 서랍 제어 시스템을 구현하여 실질적인 서비스 시나리오를 완성했습니다.
  - **[담당 역할]** PM(팀장), 시스템 아키텍처 설계, 비전 AI 구현, 로봇 GUI 개발
  - **[핵심 기능]**
    - **층간 이동**: 로봇팔 제어를 통해 엘리베이터 버튼을 직접 조작하여 자유로운 층간 이동 구현.
    - **비전 인식**: YOLOv8n 기반으로 정적/동적 장애물뿐만 아니라, 투명한 유리문까지 학습시켜 충돌 방지.
    - **통합 관제**: 관리자용 모니터링 시스템 및 고객 상호작용을 위한 로봇 GUI 제공.
  - **[기술적 도전 및 해결]**
    - **투명 유리문 미인식 문제**: LiDAR가 유리를 투과하는 한계를 극복하기 위해, YOLO 모델에 '유리문' 클래스를 추가 학습시켜 비전 기반으로 개폐 여부를 탐지, 충돌 문제를 원천 차단했습니다.
    - **엘리베이터 버튼 오인식**: YOLO 단독 사용 시 다량의 버튼 클래스로 인해 정확도가 5%에 불과했으나, **YOLO(탐지) + CNN(분류)** 2단계 파이프라인으로 구조를 변경하여 정확도를 **95%**까지 향상시켰습니다.
- **이미지 경로**: /images/projects/roomie_banner.png
- **사용 기술**: [ROS 2, IoT (ESP32), PyQt, YOLOv8, Robot Arm]
- **GitHub 링크**: https://github.com/jinhyuk2me/Roomie

### FALCON: 공항 안전 AI
- **제목**: FALCON: 공항 안전 AI
- **설명**: 
  - **[개요]** 실시간 조류 충돌(Bird Strike) 및 FOD 탐지 시스템입니다. 실제 데이터를 구하기 힘든 공항 환경의 한계를 극복하기 위해 합성 데이터를 적극 활용했습니다.
  - **[담당 역할]** 프로젝트 기획, 딥러닝 모델 개발, Unity/Blender 시뮬레이터 제작
  - **[핵심 기능]**
    - **합성 데이터 파이프라인**: Blender/Unity로 공항 환경을 정밀 모사하여 학습용 데이터를 자체 생성.
    - **위험도 산출**: 조류 군집과 항공기의 위치/속도를 삼각측량하여 실시간 충돌 위험도 계산.
    - **지능형 관제**: LLM/STT/TTS 기반 조종사 음성 질의응답 및 TCN 기반 지상 유도사 수신호 인식.
  - **[기술적 도전 및 해결]**
    - **Sim2Real 도메인 갭**: 실제 공항 사진으로 학습한 모델이 축소 모형 환경에서 인식률이 저조했습니다. 이를 해결하기 위해 축소 모형을 3D 스캔(Polycam)하여 가상 환경에 구현하고, 조명/텍스처 랜덤화를 적용한 합성 데이터로 학습시켜 **mAP 0.930**의 높은 성능을 달성했습니다.
- **이미지 경로**: /images/projects/falcon_banner.png
- **사용 기술**: [AI/CV, Unity/Blender, YOLOv8, LLM, Synthetic Data]
- **GitHub 링크**: https://github.com/jinhyuk2me/FALCON

### Bikecast: 자전거 수요 예측
- **제목**: Bikecast: 자전거 수요 예측
- **설명**: 
  - **[개요]** 4,400만 건의 따릉이 주행 데이터를 분석하여 실시간 수요를 예측하고 최적의 대여소 설치 위치를 추천하는 시스템입니다.
  - **[담당 역할]** PM, DB 설계/구축(MySQL), 수요 예측 모델 개발
  - **[핵심 기능]**
    - **실시간 예측**: 기상청 API(기온/강수량)와 과거 이력을 결합한 XGBoost 기반 단기 수요 예측.
    - **입지 분석**: 고도, 경사, 환승 거점, 상권 분석 등 지리적 요인을 반영한 장기적 설치 위치 제안.
  - **[기술적 도전 및 해결]**
    - **대용량 데이터 처리 지연**: 4,400만 건 데이터 조회 시 수 시간이 소요되었으나, 쿼리 패턴을 분석하여 적절한 **인덱싱(Indexing)** 전략을 적용한 결과 조회 시간을 수 분~수십 초 단위로 단축했습니다.
    - **고수요 구간 예측 실패**: 데이터 분포 불균형으로 인한 성능 저하를 해결하기 위해, 수요 구간을 나누어 **3-Stage 분리 학습**을 적용하여 **R²=0.761**의 준수한 예측 성능을 확보했습니다.
- **이미지 경로**: /images/projects/bikecast_banner.png
- **사용 기술**: [Data Analysis, XGBoost, Pandas, MySQL, AWS]
- **GitHub 링크**: https://github.com/jinhyuk2me/Bikecast

### DUST: 스마트 물류 관제
- **제목**: DUST: 스마트 물류 관제
- **설명**: 
  - **[개요]** 다수의 AGV(무인운반차)와 컨베이어 벨트, 게이트를 통합 제어하는 IoT 물류 관제 플랫폼입니다.
  - **[담당 역할]** 중앙 관제 서버 개발, 통신 프로토콜 설계, 실시간 모니터링 GUI 구현
  - **[핵심 기능]**
    - **통합 제어**: FSM(유한상태기계) 기반으로 AGV와 설비 간의 유기적인 협업 시나리오 제어.
    - **커스텀 통신**: TCP/IP, Serial, REST API 등 다양한 통신 방식을 디바이스 특성에 맞게 최적화.
  - **[기술적 도전 및 해결]**
    - **제어 지연(Latency)**: 초기 JSON 통신 방식의 파싱 부하로 AGV 주행이 불안정했으나, **바이너리 기반 커스텀 프로토콜**로 변경하여 메시지 크기를 최소화하고 응답 속도를 **3배 이상** 향상시켰습니다.
    - **주행 불안정**: RFID 태그 인식 시점의 연산 부하로 PWM 출력이 튀는 현상을 발견하고, 인식 직전 PID 제어를 일시 홀딩하는 타이밍 제어 기법을 도입하여 주행 안정성을 확보했습니다.
- **이미지 경로**: /images/projects/dust_banner.png
- **사용 기술**: [IoT, FSM, TCP/IP, PyQt6, MySQL]
- **GitHub 링크**: https://github.com/jinhyuk2me/DUST

---

## 💼 경력 (Experience)

### LK ROBOTICS
- **회사명**: LK ROBOTICS
- **직함**: 임베디드 AI 엔지니어
- **기간**: 2025.10 - 
- **주요 업무**:
  - **NXP i.MX8M Plus** NPU 기반 초기 화재 감지 시스템 **PyroVision** 개발.
  - 오탐지 최소화를 위한 **RGB-IR 센서 퓨전** 알고리즘 구현.
  - 엣지 디바이스 추론을 위한 **YOLOv8** 및 **TensorFlow Lite** 모델 최적화.
  - **YOLOv11**과 **Transformer(TransReID)**를 활용한 **고성능 다중 객체 추적(MOT) 및 재식별(Re-ID)** 시스템 선행 연구 수행.
  - **TCP/IP**, **GStreamer**, **PyQt6**를 활용한 실시간 모니터링 인프라 구축.

---

## 🎓 학력 (Education)

### Addinedu IT Academy
- **학교명**: 애드인에듀 IT 아카데미
- **전공/과정**: ROS2 & AI 자율주행 로봇 부트캠프
- **기간**: 2025.02 - 2025.08
- **설명**: ROS2, 자율주행, 딥러닝, 임베디드 시스템 집중 교육 과정. 팀 리더로서 5개의 주요 프로젝트 성공적 완수.

### KAIST
- **학교명**: KAIST
- **전공/과정**: 전기및전자공학부
- **기간**: 2018.03 - 2025.02 (휴학)
- **설명**: 전기및전자공학부 학부 과정.

---

## 🙋‍♂️ 자기소개 (About Me)

- **소개글**:
  저는 시스템 설계부터 AI까지 전체 시스템을 쌓아올릴 수 있는 **풀스택 로보틱스 엔지니어**입니다.
  하드웨어 제어와 AI 인지, 그리고 소프트웨어 서비스를 연결하여, 실험실이 아닌 현실에서 작동하는 로봇을 만듭니다.

- **핵심 기술**: [ROS 2 (Humble/Jazzy), Python & C++, Nav2 & Manipulation, Computer Vision (YOLO/OpenCV), Deep Learning (PyTorch), IoT & Embedded (ESP32), Linux & Docker, AWS & MySQL, Communication (TCP/REST/Serial)]
