# 🙋‍♂️ Introduction

**채지훈** · Jihun Chae

중앙대학교 전자전기공학부 학부생이고 2027년 2월 졸업 예정이다. AI·신호 연산을 위한 디지털
하드웨어를 설계한다. 컨볼루션 연산기, 고정소수점 데이터패스, DDR2 위에서 측정한 LLM 디코딩용
무손실 KV 캐시 엔진, 배치·배선까지 200 MHz로 닫은 이벤트 카메라 가속기, 그리고 그것이
소프트웨어 레퍼런스와 비트 단위로 같다는 것을 증명하는 테스트벤치를 만든다.

주로 다루는 영역은 RTL 자체보다 그 주변까지다. 양자화 상수, 버스 인터페이스, 타이밍 클로저,
골든 모델 검증. Verilog에서 배치·배선을 마친 레이아웃까지(OpenROAD와 Cadence Innovus 양쪽), 비트스트림에서 동작하는 보드
시연까지 완주해 봤다.

[![Email](https://img.shields.io/badge/jinny20020202@gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:jinny20020202@gmail.com)

[English](README.md)

---

## 🎓 Education

| 과정 | 소속 | 기간 |
|---|---|---|
| 전자전기공학부 학사 | 중앙대학교 창의ICT공과대학 | 2021.03 – 2027.02 (졸업예정) |

병역 2023.03 – 2024.09.

## 👩‍🔬 Research Experience

| 역할 | 소속 | 주제 | 기간 |
|---|---|---|---|
| 하계 학부연구 인턴 | 서울대학교 전기·정보공학부 | FPGA 셀프 어텐션 가속기 (정수 연산만으로 QKᵀ·소프트맥스·×V) | 2026.06 – 2026.07 |
| 학부연구생 | 서울대학교 전기·정보공학부 | 지연 시간이 일정한 FPGA 기술지표 가속기 | 2026.03 – 2026.06 |

## 📝 Projects

### FPGA 가속기

| 프로젝트 | 내용 | 기술 |
|---|---|---|
| [무손실 KV 캐시 조기 종단 엔진](https://github.com/chaezhun/KV_CACHE_ET_ENGINE) | 졸업논문, 팀장. GQA LLM 디코딩에서 상위 16개 토큰을 잃지 않고 KV 캐시 DRAM 읽기를 건너뜀. DDR2 보드 실측 | SystemVerilog, Vivado, Xilinx MIG, Python |
| [YOLOv2 FPGA 가속기](https://github.com/chaezhun/YOLO-ACCELERATOR) | 22개 레이어 객체 탐지기를 Artix-7 한 장에. 레이어 단위 전 구간 검증 | Verilog, Vivado, MicroBlaze |
| [HFT 기술지표 가속기](https://github.com/chaezhun/HFT_ACCELERATOR) | 볼린저·MACD·RSI를 하나의 매매 결정으로 융합, 지연 시간 고정 | Verilog, C, Vivado |
| [FPGA 셀프 어텐션 가속기](https://github.com/chaezhun/ATTENTION_ACCELERATOR) | QKᵀ, 소프트맥스, 값 행렬 곱을 Python 골든 모델로 검증 | Verilog, Python |

### ASIC·물리설계

| 프로젝트 | 내용 | 기술 |
|---|---|---|
| [Pixel-to-World 매핑 가속기](https://github.com/chaezhun/PIXEL2WORLD_ACCELERATOR) | 전국 대학생 AI반도체 회로설계 경진대회, 2인 팀. 회전하는 이벤트 카메라의 픽셀 이벤트를 월드 좌표로 매핑해 칩 안의 월드 메모리에 누적. GPDK045 200 MHz 배치·배선 완료 | Verilog, Cadence Genus / Innovus, GPDK045 |
| [16×16 행렬 곱셈 ASIC](https://github.com/chaezhun/MATMUL-ASIC) | SRAM 인터페이스 뒤에 붙는 고정소수점 행렬 곱셈기. 사이클당 2 MAC, 버블 없음 | Verilog, Vivado |
| [CNN 컨볼루션 가속기](https://github.com/chaezhun/CONV_ACCELERATOR) | 3채널 5×5 stride-3 컨볼루션. RTL부터 배치·배선까지 완주 | Verilog, OpenROAD, Nangate45 |

### SoC·버스 IP

| 프로젝트 | 내용 | 기술 |
|---|---|---|
| [K-means FPU 가속기](https://github.com/chaezhun/KMEANS_FPU) | IEEE-754 FPU를 APB로 RISC-V 코어에 붙여 소프트웨어 실수 연산을 대체 | Verilog, C, APB |
| [APB 커스텀 IP](https://github.com/chaezhun/APB_CUSTOM_IP) | 메모리 맵 가속기 두 개 — 바이트 병렬 덧셈, 128비트 SIMD MAC | Verilog, C |

### 임베디드 시스템

| 프로젝트 | 내용 | 기술 |
|---|---|---|
| [딸기 선별 시스템](https://github.com/chaezhun/STRAWBERRY_SORTING) | 이종 보드 3대를 CAN과 IPC로 묶어 숙도별로 선별 | C, Python, CAN, FreeRTOS |
| [스마트 그늘막](https://github.com/chaezhun/SMART_SUNSHADE) | 해를 따라 움직이고 바람이 세지면 스스로 접히는 공공 그늘막 | Arduino, ESP8266 |

### 딥러닝

| 프로젝트 | 내용 | 기술 |
|---|---|---|
| [MNIST / ResNet50 전이학습](https://github.com/chaezhun/MNIST_RESNET50_TXFR) | 하이퍼파라미터 분석과 2,350만 파라미터 백본과의 통제 비교 | PyTorch |

### 핵심 결과

| 프로젝트 | 결과 |
|---|---|
| KV 캐시 엔진 | DDR2 보드에서 K burst **dense 대비 0.581**, **22개 표본 모두 골든모델과 같음**. 문맥 2K 에서 **KV 트래픽 3.0배 감축**, 1,280 스텝 상위 16개 손실 0 (골든모델). **DSP 0**, LUT 48% |
| YOLOv2 | 22개 레이어 전체를 Artix-7 한 장에. C 레퍼런스와 레이어 단위 **0 mismatch**, 81.25 MHz WNS −0.18 ns |
| HFT | 주가 7,700배 차이에도 **지연 890 ns 동일**. 33 → 100 MHz, 타이밍 위반 0건 |
| 어텐션 | 어텐션 헤드 전체를 **118.2 MHz, 칩 자원 약 10%** 로. 출력 1,024개 보드 검증 |
| Pixel-to-World | GPDK045에서 **배치·배선까지 200 MHz 충족**(셋업 +65 ps, hold +31 ps). 같은 조건의 이벤트 단위 기준 설계 대비 로직 면적 **1/1.91**, 이벤트당 로직 에너지 **1/2.43**. 8,800만 이벤트에서 월드 칸 123,904개 **전부 골든모델과 같음** |
| 행렬곱 ASIC | **2,051 사이클 중 2,048 사이클 가동**(99.85%), 정답 256개 전부 일치 |
| 컨볼루션 | 채점 면적 **295,842 → 106,234 µm²** (2.8배), 점수 41.3 → 33.1. 1 GHz에서 **최악 경로 여유 +0.10 ns·DRC 0**으로 물리 구현 사인오프 |
| K-means FPU | 보드 실측 **187.75 ms → 60.02 ms** (3.13배) |
| 딸기 선별 | 보드 3대·프로토콜 3종을 명령 하나로. 초당 2프레임에서 **딸기 1개당 정확히 1회 동작** |
| 전이학습 | **학습 파라미터 4,098개(0.017%)로 100%**, 전체 2,350만 개 학습은 66.67% |

## 🏅 Awards

| 수상 | 대회 | 시점 |
|---|---|---|
| 장려상 (19팀 중) | 2026 Deep Learning Hardware 설계 경진대회 | 2026.06 |

## 📄 Publications

- 「대학생의 AI 활용 정도가 AI 리터러시와 생산성에 미치는 영향」,
  **『인공지능인문학연구』 제21권** (KCI 등재지), 2025.12 — 공동저자.
  서론, 이론적 배경, 인터뷰 문항 설계, 인터뷰 진행을 담당했다.

## ⚒ Tech Skills

![Verilog](https://img.shields.io/badge/Verilog-1A1A1A?style=flat-square&logoColor=white)
![SystemVerilog](https://img.shields.io/badge/SystemVerilog-3F3F3F?style=flat-square&logoColor=white)
![C](https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=c&logoColor=black)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)

| | |
|---|---|
| **언어** | **Verilog**, SystemVerilog · **C**, C++ · **Python** (PyTorch, NumPy) · 셸 스크립트 |
| **환경** | **Linux** (Ubuntu, Yocto, WSL), Git, Makefile |
| **EDA** | Vivado (xsim, MIG, XADC 포함), Cadence Genus / Innovus / Conformal LEC / Xcelium, Questa / ModelSim, NCverilog, Verilator, OpenROAD, Icarus, OpenRAM / CACTI |
| **하드웨어** | AXI4 / AXI4-Lite / APB, DDR2 (Xilinx MIG), CAN, UART, I2C, DMA, FSM 설계, 파이프라이닝, 타이밍 클로저, clock gating, SRAM 뱅킹 |
| **플랫폼** | Artix-7 (Nexys A7), MicroBlaze, RISC-V SoC, FreeRTOS, Arduino / ESP8266 · GPDK045, Nangate45 표준 셀 |

**Top languages** — 위 저장소들의 소스 바이트 기준

```text
Verilog        ███████████░░░░░░░░░░░░░░░░░░░  35%
Python         ██████████░░░░░░░░░░░░░░░░░░░░  34%
C              ████░░░░░░░░░░░░░░░░░░░░░░░░░░  13%
SystemVerilog  ███░░░░░░░░░░░░░░░░░░░░░░░░░░░   9%
Tcl            █░░░░░░░░░░░░░░░░░░░░░░░░░░░░░   4%
```

**Most used topics** — `verilog` · `fpga` · `rtl` · `asic` · `event-camera` · `risc-v` · `fixed-point` · `embedded` · `pytorch`

## 📜 Certificates

| 자격 | 점수·등급 | 취득 |
|---|---|---|
| TOEIC | 910점 (LC 475 / RC 435) | 2024.12 |
| OPIc (영어) | IM2 | 2026.09 |
| 제2종 보통 운전면허 | — | 2021.07 |

---

*모든 저장소에 영문·국문 README를 함께 둔다. 각 저장소에서 배포물로 표시한 파일은 수업이나
대회에서 제공된 것이며 프로젝트가 빌드되도록 하기 위해서만 포함했으니, 재사용 전에 원
라이선스를 확인하기 바란다. 그 외는 모두 직접 작성한 것이고, 팀으로 진행한 프로젝트는 각
README에 담당 범위를 명시했다.*
