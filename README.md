# 🙋‍♂️ Introduction

**Jihun Chae** · 채지훈

Undergraduate in Electrical and Electronics Engineering at Chung-Ang University, graduating
February 2027. I design digital hardware for AI and signal workloads — convolution engines,
fixed-point datapaths, a lossless KV-cache engine for LLM decoding measured on DDR2, and the
testbenches that prove they match a software reference bit for bit.

Most of my work sits between the RTL and the system around it: quantisation constants, bus
interfaces, timing closure, golden-model verification. I have taken a design from Verilog to a
placed-and-routed layout, and from a bitstream to a working board demonstration.

[![Email](https://img.shields.io/badge/jinny20020202@gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:jinny20020202@gmail.com)

[한국어](README.ko.md)

---

## 🎓 Education

| Degree | Institution | Period |
|---|---|---|
| B.S. in Electrical and Electronics Engineering | Chung-Ang University, College of ICT Engineering | 2021.03 – 2027.02 (expected) |

Military service 2023.03 – 2024.09.

## 👩‍🔬 Research Experience

| Role | Institution | Topic | Period |
|---|---|---|---|
| Summer Research Intern | Seoul National University, Dept. of Electrical and Computer Engineering | FPGA self-attention accelerator (integer-only QKᵀ, softmax, ×V) | 2026.06 – 2026.07 |
| Undergraduate Researcher | Seoul National University, Dept. of Electrical and Computer Engineering | FPGA technical-indicator accelerator with deterministic latency | 2026.03 – 2026.06 |

## 📝 Projects

### FPGA Accelerators

| Project | What it is | Stack |
|---|---|---|
| [Lossless KV-Cache Early-Termination Engine](https://github.com/chaezhun/KV_CACHE_ET_ENGINE) | Graduation thesis, team lead. Skips KV-cache DRAM reads in GQA LLM decoding without losing a top-16 token; measured on a board with DDR2 | SystemVerilog, Vivado, Xilinx MIG, Python |
| [YOLOv2 FPGA Accelerator](https://github.com/chaezhun/YOLO-ACCELERATOR) | A 22-layer object detector fitted onto a single Artix-7, verified layer by layer | Verilog, Vivado, MicroBlaze |
| [HFT Indicator Accelerator](https://github.com/chaezhun/HFT_ACCELERATOR) | Bollinger, MACD and RSI fused into one trading decision at fixed latency | Verilog, C, Vivado |
| [FPGA Self-Attention Accelerator](https://github.com/chaezhun/ATTENTION_ACCELERATOR) | QKᵀ, softmax and the value multiply verified against a Python golden model | Verilog, Python |

### ASIC & Physical Design

| Project | What it is | Stack |
|---|---|---|
| [16×16 Matrix Multiply ASIC](https://github.com/chaezhun/MATMUL-ASIC) | Fixed-point matrix multiplier behind an SRAM interface, two MACs per cycle, no bubbles | Verilog, Vivado |
| [CNN Convolution Accelerator](https://github.com/chaezhun/CONV_ACCELERATOR) | Three-channel 5×5 stride-3 convolution taken from RTL to place-and-route | Verilog, OpenROAD, Nangate45 |

### SoC & Bus IP

| Project | What it is | Stack |
|---|---|---|
| [K-means FPU Accelerator](https://github.com/chaezhun/KMEANS_FPU) | IEEE-754 FPU on APB replacing the software float path of a RISC-V core | Verilog, C, APB |
| [APB Custom IP](https://github.com/chaezhun/APB_CUSTOM_IP) | Two memory-mapped accelerators — byte-parallel addition and a 128-bit SIMD MAC | Verilog, C |

### Embedded Systems

| Project | What it is | Stack |
|---|---|---|
| [Strawberry Sorting System](https://github.com/chaezhun/STRAWBERRY_SORTING) | Three heterogeneous boards tied into one line over CAN and IPC | C, Python, CAN, FreeRTOS |
| [Smart Sunshade](https://github.com/chaezhun/SMART_SUNSHADE) | A public sunshade that tracks the sun and folds itself in wind | Arduino, ESP8266 |

### Deep Learning

| Project | What it is | Stack |
|---|---|---|
| [MNIST / ResNet50 Transfer](https://github.com/chaezhun/MNIST_RESNET50_TXFR) | Hyperparameter analysis and a controlled comparison against a 23.5M-parameter backbone | PyTorch |

### Results at a glance

| Project | Result |
|---|---|
| KV-cache engine | on the board with DDR2, K bursts **0.581 of dense** and **identical to the golden model in 22/22 samples**; **3.0× less KV traffic** at a 2K context with zero top-16 loss over 1,280 steps (golden model); **0 DSP**, 48% LUT |
| YOLOv2 | all 22 layers on one Artix-7, **0 mismatch** against the C reference layer by layer; WNS −0.18 ns at 81.25 MHz |
| HFT | **890 ns latency regardless of a 7,700× price range**; 33 → 100 MHz, zero timing violations |
| Attention | a full attention head at **118.2 MHz using ~10% of the device**, 1,024 outputs verified on board |
| Matmul ASIC | **2,048 of 2,051 cycles active** (99.85%), all 256 golden values matched |
| Convolution | scored area **295,842 → 106,234 µm²** (2.8×), score 41.3 → 33.1; physical implementation signed off with **+0.10 ns worst-path slack and zero DRC** at 1 GHz |
| K-means FPU | **187.75 ms → 60.02 ms** (3.13×) measured on the board |
| Strawberry sorting | three boards and three protocols behind one command; **exactly one actuation per strawberry** at 2 fps |
| Transfer learning | **100% from 4,098 trained parameters (0.017%)**; training all 23.5M gave 66.67% |

## 🏅 Awards

| Award | Competition | Date |
|---|---|---|
| Encouragement Award (of 19 teams) | 2026 Deep Learning Hardware Design Competition | 2026.06 |

## 📄 Publications

- *The effect of university students' degree of AI use on AI literacy and productivity*,
  **Journal of Artificial Intelligence Humanities**, Vol. 21 (KCI-listed), 2025.12 — co-author.
  Responsible for the introduction, theoretical background, interview instrument design and
  the interviews themselves.

## ⚒ Tech Skills

![Verilog](https://img.shields.io/badge/Verilog-1A1A1A?style=flat-square&logoColor=white)
![SystemVerilog](https://img.shields.io/badge/SystemVerilog-3F3F3F?style=flat-square&logoColor=white)
![C](https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=c&logoColor=black)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)

| | |
|---|---|
| **Languages** | **Verilog**, SystemVerilog · **C**, C++ · **Python** (PyTorch, NumPy) · shell |
| **Environment** | **Linux** (Ubuntu, Yocto, WSL), Git, Makefile |
| **EDA** | Vivado (incl. xsim, MIG, XADC), Questa / ModelSim, NCverilog, OpenROAD, Icarus |
| **Hardware** | AXI4 / AXI4-Lite / APB, DDR2 (Xilinx MIG), CAN, UART, I2C, DMA, FSM design, pipelining, timing closure |
| **Platforms** | Artix-7 (Nexys A7), MicroBlaze, RISC-V SoC, FreeRTOS, Arduino / ESP8266 |

**Top languages** — by source bytes across the repositories above

```text
Verilog        █████████████████░░░░░░░░░░░░░  57%
C              ████████░░░░░░░░░░░░░░░░░░░░░░  26%
Python         ██░░░░░░░░░░░░░░░░░░░░░░░░░░░░   7%
Tcl            ██░░░░░░░░░░░░░░░░░░░░░░░░░░░░   5%
C++            █░░░░░░░░░░░░░░░░░░░░░░░░░░░░░   2%
```

**Most used topics** — `verilog` · `fpga` · `rtl` · `asic` · `risc-v` · `fixed-point` · `embedded` · `pytorch`

## 📜 Certificates

| Certificate | Score / Grade | Date |
|---|---|---|
| TOEIC | 910 (LC 475 / RC 435) | 2024.12 |
| Driver's licence, Class 2 Regular | — | 2021.07 |

---

*Each repository ships English and Korean READMEs. Files marked as distributed material in a
repository were provided by a course or competition and are included only so the project builds;
check their original licence before reuse. Everything else is my own work, and team projects
state my scope in their README.*
