# 🙋‍♂️ Introduction

**Jihun Chae** · 채지훈

Undergraduate in Electrical and Electronics Engineering at Chung-Ang University, graduating
February 2027. I design digital hardware for AI and signal workloads — convolution engines,
fixed-point datapaths, and the testbenches that prove they match a software reference bit for
bit.

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

| Role | Institution | Period |
|---|---|---|
| Undergraduate Research Intern | Seoul National University, Dept. of Electrical and Computer Engineering | 2026.07 – present |
| Undergraduate Research Intern | Chung-Ang University, School of Electrical and Electronics Engineering | 2026.03 – present |

## 📝 Projects

| | Project | What it is | Stack |
|---|---|---|---|
| 01 | [YOLOv2 FPGA Accelerator](https://github.com/chaezhun/yolo-fpga-accelerator) | A 22-layer object detector inferring end to end on a single Artix-7 | Verilog, Vivado, MicroBlaze |
| 02 | [16×16 Matrix Multiply ASIC](https://github.com/chaezhun/matmul16x16-asic) | Fixed-point matrix multiplier behind an SRAM interface, two MACs per cycle, no bubbles | SystemVerilog, Vivado |
| 03 | [CNN Convolution Accelerator](https://github.com/chaezhun/conv-accelerator-rtl) | Three-channel 5×5 stride-3 convolution taken from RTL to place-and-route | Verilog, OpenROAD, Nangate45 |
| 04 | [Smart Sunshade](https://github.com/chaezhun/smart-sunshade) | A public sunshade that tracks the sun and folds itself in wind | Arduino, ESP8266 |
| 05 | [K-means FPU Accelerator](https://github.com/chaezhun/kmeans-fpu-accelerator) | IEEE-754 FPU on APB replacing the software float path of a RISC-V core | Verilog, C, APB |
| 06 | [APB Custom IP](https://github.com/chaezhun/apb-custom-ip) | Two memory-mapped accelerators — byte-parallel addition and a 128-bit SIMD MAC | Verilog, C |
| 07 | [Strawberry Sorting System](https://github.com/chaezhun/strawberry-sorting) | Three heterogeneous boards tied into one line over CAN and IPC | C, Python, CAN, FreeRTOS |
| 08 | [MNIST / ResNet50 Transfer](https://github.com/chaezhun/mnist-resnet50-transfer) | Hyperparameter analysis and a controlled comparison against a 23.5M-parameter backbone | PyTorch |
| 09 | [HFT Indicator Accelerator](https://github.com/chaezhun/hft-fpga-accelerator) | Fixed-point SMA/EMA/RSI/MACD/Bollinger pipeline with deterministic latency | Verilog, C, Vivado |
| 10 | [FPGA Self-Attention Accelerator](https://github.com/chaezhun/fpga-attention-accelerator) | QKᵀ, softmax and the value multiply verified against a Python golden model | Verilog, Python |

### Results at a glance

| Project | Result |
|---|---|
| 01 YOLOv2 | all 22 layers inferring on one Artix-7, **0 mismatch** against the C reference layer by layer |
| 02 Matmul ASIC | **2,048 of 2,051 cycles active** (99.85%), all 256 golden values matched |
| 03 Convolution | scored area **295,842 → 106,234 µm²** (2.8×), total score 41.3 → 33.1 |
| 05 K-means FPU | **187.75 ms → 60.02 ms** (3.13×) measured on the board |
| 07 Strawberry sorting | three boards and three protocols behind one command; **exactly one actuation per strawberry** at 2 fps |
| 08 Transfer learning | **100% from 4,098 trained parameters (0.017%)**; training all 23.5M gave 66.67% |
| 09 HFT | **890 ns latency regardless of a 7,700× price range**; 33 → 100 MHz, zero timing violations |
| 10 Attention | a full attention head at **118.2 MHz using ~10% of the device**, 1,024 outputs verified on board |

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
![SystemVerilog](https://img.shields.io/badge/SystemVerilog-1A1A1A?style=flat-square&logoColor=white)
![C](https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=c&logoColor=black)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)

| | |
|---|---|
| **Languages** | **Verilog**, SystemVerilog · **C**, C++ · **Python** (PyTorch, NumPy) · shell |
| **Environment** | **Linux** (Ubuntu, Yocto, WSL), Git, Makefile |
| **EDA** | Vivado, Questa / ModelSim, NCverilog, OpenROAD, Icarus |
| **Hardware** | AXI4 / AXI4-Lite / APB, CAN, UART, I2C, DMA, FSM design, pipelining, timing closure |
| **Platforms** | Artix-7 (Nexys A7), MicroBlaze, RISC-V SoC, FreeRTOS, Arduino / ESP8266 |

## 📜 Certificates

| Certificate | Score / Grade | Date |
|---|---|---|
| TOEIC | 910 (LC 475 / RC 435) | 2024.12 |
| Driver's licence, Class 2 Regular | — | 2021.07 |

---

## What I focus on

**Bit-exact verification.** The accelerators here were not checked by eye — they were compared
against a software reference. The YOLO engine matches layer by layer from L0 to L20 with zero
mismatches, the matrix multiply ASIC matches all 256 golden values, and the convolution
accelerator matches 1024/1024 on each of three filters. **The real bugs surface on the way to
zero** — sign handling, packing order, rounding direction.

**Rounding and sign, again and again.** Verilog `>>>` rounds toward −∞ while C division rounds
toward zero. On layers where negative values survive, that is a one-LSB error on every negative
pixel, and much of the debugging in `01` and `09` came from exactly this. Reading signed values
as unsigned was the same kind of problem: the results looked plausible, so nothing but a
reference would have caught it.

**Designing for the scoring formula, not for intuition.** Two of these projects are graded by a
formula. In `01` energy sits in the denominator, so buying frames per second with more
multipliers loses points — hence a fixed 144-MAC budget with 1×1 convolution reusing the 3×3
kernel. In `03` the reference power was so small that the power term amplified the total by
143×, and that was only visible by **measuring the reference design**, not by reading the
weights in the formula.

---

*Each repository ships English and Korean READMEs. Files marked as distributed material in a
repository were provided by a course or competition and are included only so the project builds;
check their original licence before reuse. Everything else is my own work, and team projects
state my scope in their README.*
