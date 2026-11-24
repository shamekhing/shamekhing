<div align="center">

# Shamekh Al-Suwi

**AI & FPGA engineer · MSc Artificial Intelligence @ JKU Linz**

Systems, hardware and machine learning, built close to the metal.

<a href="https://www.linkedin.com/in/shamekhalsuwi/"><img src="https://img.shields.io/badge/LinkedIn-shamekhalsuwi-137dc5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
<a href="mailto:shamekhing@gmail.com"><img src="https://img.shields.io/badge/Email-shamekhing@gmail.com-112d4e?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
<a href="./Europass_CV/"><img src="https://img.shields.io/badge/CV-Europass-b17a50?style=for-the-badge&logo=readme&logoColor=white" alt="CV" /></a>

<img src="./Shamekh.jpg" alt="Shamekh Al-Suwi" width="120" />

</div>

## 👋 About

I'm a multidisciplinary AI and software engineer based in **Linz, Austria**, with a background in mechatronics, control systems, computer vision and applied research. I like building systems close to the metal: FPGA computing, custom CPUs, C++ simulation, and hardware-software co-design.

**Open to:** AI research, FPGA / embedded and software engineering roles in Austria and the EU.

**Interests:** efficient ML accelerators, FPGA-based AI, computer architecture, digital arithmetic, and LLM-assisted RTL design and verification.
## 🧭 Skills

| Area | Tools |
|---|---|
| **Hardware** | SystemVerilog, Gowin FPGAs, custom CPUs, USB CDC, Icarus Verilog, Verilator, GTKWave |
| **AI / ML** | PyTorch, deep learning, reinforcement learning, probabilistic models, computer vision, OpenCV |
| **HPC / scientific** | C++17, CUDA, Eigen, numerical simulation, CFD, parallel computing |
| **Software** | C/C++, Python, MATLAB, Dart/Flutter, CMake, Qt, Raylib, Linux, Bash, Git |
| **Systems & control** | Control theory, Simulink, embedded systems, PLCs, signal processing |

## 💼 Experience

- **Freelance Software Developer** *(March 2026 - present)*: C++ applications, Python tools, computer vision, LLM-assisted workflows, simulation, verification, and FPGA exploration
- **Junior Research Engineer**, [Austrian Institute of Technology (AIT)](https://www.ait.ac.at/en/), Technology Experience Department *(October 2024 - March 2026)*: AI system integration, data-driven monitoring systems, real-time AI interfaces, reliability and evaluation, and research-to-application transfer
- **Teaching Assistant**, [JKU Institute of Computer Graphics](https://www.jku.at/institut-fuer-computergrafik/) *(October 2023 - February 2024)*: practical support in computer vision, machine learning, deep learning, data analysis, and system modelling
- **Software Developer Intern**, [Sequality](https://www.sequality.at/en/your-partner-for-technical-software/) *(October 2023 - November 2023)*: industrial software interfaces with C++ and Qt
- **Research Assistant**, [JKU Institute of Semiconductor and Solid State Physics](https://www.jku.at/en/institute-of-semiconductor-and-solid-state-physics/) *(August 2022 - February 2023)*: scientific software for entangled-photon quantum key distribution and secure distributed systems
- **Software Engineer**, [Simma Software](https://www.simma.io/) *(November 2021 - April 2022)*: Selenium automation, integration workflows, and automated testing tools
- **R&D Software Engineer**, [Mixed Dimensions](https://integralrealitylabs.com/) *(February 2020 - November 2021)*: geometry-processing algorithms, computational models, performance optimisation, and repair of damaged 3D models for commercial printing
- **Mechatronics Intern**, Bahbish *(January 2019 - April 2019)*: microscope automation and computer-aided design

## 🎓 Education

- **MSc Artificial Intelligence**, [Johannes Kepler University Linz](https://www.jku.at/en/), Austria *(March 2024 - present)*
  - Machine learning, deep learning, recurrent networks, reinforcement learning, computer vision, probabilistic models, parallel computing, signal processing, adaptive systems, and quantum information
- **BSc Mechatronics Engineering**, [University of Jordan](https://www.ju.edu.jo/), Jordan *(July 2014 - June 2019)*
  - Control theory, robotics, automation, embedded systems, digital logic, electronics, PLCs, sensors, actuators, industrial process control, and CAD
  - **Bachelor's thesis:** Intelligent transportation using vehicle-to-vehicle communication for cooperative vehicle tracking and collision warnings

📄 Full details in my [Europass CV](./Europass_CV/).

## 🏆 Competitive Programming

I competed in national, regional, and international programming contests using **C++**, with a focus on algorithms, data structures, and problem solving.

| Competition | Result |
|---|---:|
| IEEEXtreme 2019 | 93rd of ~9,400 participants |
| Africa & Arab Collegiate Programming Contest 2019 | 28th place |
| Jordan Collegiate Programming Contest 2019 | 5th place |
| Jordan Collegiate Programming Contest 2018 | 13th place |
| Arab Collegiate Programming Contest 2017 | 92nd place |

[Certificates](./Certificates/)


## 🚀 Projects

**Index:** [cfd-sim](#cfd-sim) · [cv_deepSort](#cv_deepsort) · [OpenJoey2](#openjoey2) · [doomai](#doomai) · [fpga-snn](#fpga-snn) · [Ahoy](#ahoy) · [Kalman GPS Tracking](#kalman-gps-tracking) · [Mean-Shift Clustering](#mean-shift-clustering) · [cooda](#cooda) · [fpga-usb](#fpga-usb) · [fpga-skill](#fpga-skill) · [pysuwi](#pysuwi)

### [cfd-sim](https://github.com/shamekhing/cfd-sim)

A computational fluid dynamics engine written from scratch. It simulates air flowing around a cylinder by solving the incompressible Navier-Stokes equations on a staggered grid with the SIMPLE algorithm, and it reproduces the Kármán vortex street shown in the capture. Optional CUDA acceleration.

`C++17` `CUDA` `Numerical Methods`

<div align="center"><img src="./portfolio/cfd-sim/field.gif" alt="Velocity field showing vortex shedding behind a cylinder" width="640" /></div>

```mermaid
graph LR
  MESH["Mesh the domain around the cylinder"] --> PRED["Predict velocity for one time step"]
  PRED --> CORR["Project pressure to satisfy continuity"]
  CORR --> FORCE["Integrate surface forces (Cd, Cl)"]
  FORCE -->|next step| PRED
  FORCE --> OUT["Write field snapshots and force traces"]
```

### [cv_deepSort](https://github.com/shamekhing/cv_deepSort)

A multi-object tracking pipeline for video. YOLOv5 detects objects in each frame and Deep SORT keeps a stable identity on each one by combining motion prediction with appearance embeddings. Built for drone footage, with recorded result clips.

`Python` `PyTorch` `OpenCV`

<div align="center"><img src="./portfolio/cv_deepSort/tracking.gif" alt="YOLOv5 and Deep SORT tracking output on drone footage" width="480" /></div>

```mermaid
graph LR
  VID["Video frames"] --> DET["Detect objects per frame (YOLOv5)"]
  DET --> ASSOC["Associate detections across frames<br/>(motion + appearance)"]
  ASSOC --> TRACKS["Maintain track IDs (Deep SORT)"]
  TRACKS --> OUT["Rendered tracks with boxes and IDs"]
```

### [OpenJoey2](https://github.com/shamekhing/OpenJoey2)

A Yu-Gi-Oh! engine that implements the classic ruleset from scratch in C++17: summon types, attack and defense math, chains with Spell Speeds, and bounded undo snapshots. A raylib interface drives the game, and the same code builds for the browser.

`C++17` `Raylib` `Game Engine`

<div align="center"><img src="./portfolio/OpenJoey2/walkthrough.gif" alt="OpenJoey2 walkthrough of the duel interface" width="640" /></div>

<table align="center">
  <tr>
    <td><img src="./portfolio/OpenJoey2/duel.png" alt="Duel board with opening hands and phase bar" width="280" /></td>
    <td><img src="./portfolio/OpenJoey2/preview.png" alt="Card preview with rules text" width="280" /></td>
    <td><img src="./portfolio/OpenJoey2/summon.png" alt="Monster summoned to the field" width="280" /></td>
  </tr>
  <tr>
    <td><img src="./portfolio/OpenJoey2/menu.png" alt="Main menu" width="280" /></td>
    <td><img src="./portfolio/OpenJoey2/action.png" alt="Available-actions menu" width="280" /></td>
    <td><img src="./portfolio/OpenJoey2/log.png" alt="Duel log" width="280" /></td>
  </tr>
</table>

```mermaid
graph LR
  ENTRY["main.cpp<br/>entry point"] --> APP["App shell<br/>window · input · screens"]
  APP --> DB["Card database<br/>cards.json, runtime fetch"]
  DB --> EDITOR["Deck editor<br/>search · preview · 40-card deck"]
  APP --> DUEL["Duel screen<br/>hotseat"]
  subgraph RULES["Rules engine: classic ruleset"]
    ACT["Action vocabulary<br/>213 actions"] --> GATE["Legal-action gates<br/>engine predicates"]
    GATE --> CAT["Classic effect catalog<br/>name-keyed resolution"]
    CAT --> CHAIN["Chains · Spell Speeds<br/>battle replays"]
    CHAIN --> SNAP["Undo snapshots<br/>bounded stack"]
  end
  DUEL --> ACT
  ACT --> FIELD["Field · zones · positions"]
  APP --> WEB["Web build<br/>Emscripten"]
```
### [doomai](https://github.com/shamekhing/doomai)

Reinforcement learning agents for the JKU ViZDoom deathmatch challenge. Each agent first learns by imitating recorded human play, then improves with PPO and DQN training rewarded for frags, and exports to ONNX.

`Python` `PyTorch` `RL`

<div align="center"><img src="./portfolio/doomai/gameplay.gif" alt="BC-initialized DQN agent in a ViZDoom deathmatch" width="320" /></div>

```mermaid
graph LR
  ENV["ViZDoom deathmatch"] --> BC["Behaviour cloning from recorded human play"]
  BC --> RL["PPO / DQN training from reward"]
  RL --> EVAL["Evaluation matches"]
  EVAL --> EXP["Export the trained agent (ONNX)"]
  EVAL --> GIF["Recorded gameplay video"]
```

### [fpga-snn](https://github.com/shamekhing/fpga-snn)

An experimental spiking neural network accelerator for MNIST, where neurons carry information as spike timing instead of numbers. A Python trainer learns the weights and a SystemVerilog datapath replays them on a Gowin FPGA.

`SystemVerilog` `Python` `SNN`

<div align="center"><img src="./portfolio/fpga-snn/waveform.gif" alt="Waveform from the fpga-snn RTL simulation" width="640" /></div>

```mermaid
graph LR
  IMG["MNIST digit"] --> ENC["Encoder: pixels to differential-time events"]
  ENC --> SCHED["Scheduler: order events by time"]
  SCHED --> NEU["128 LIF neurons: integrate and fire"]
  NEU --> OUT["Spike counts: predicted class"]
  TRAIN["Python training app"] -.->|learned weights| NEU
```

### [Ahoy](https://github.com/shamekhing/Ahoy)

A privacy-first messaging app in Flutter for phones that are near each other. It picks the best direct link (Wi-Fi Direct, LAN or Bluetooth), encrypts messages end to end so keys never leave the phone, and needs no server or account.

`Dart` `Flutter` `Privacy`

<div align="center"><img src="./portfolio/ahoy/screens.gif" alt="Ahoy chat app running on a phone" width="320" /></div>

```mermaid
flowchart LR
  P1["Phone A"] --> APP["Chat app: discover · chat · profile"]
  APP --> SEC["End-to-end encryption, keys never leave the phone"]
  SEC --> STO["Encrypted message store"]
  STO --> T["Direct links: Wi-Fi Direct · LAN · Bluetooth, strongest wins"]
  T --> P2["Phone B"]
```

### [Kalman GPS Tracking](https://github.com/shamekhing/Kalman-Filter-for-GPS-Tracking)

A header-only C++ Kalman filter that turns jumpy GPS fixes into a smooth route. It predicts where the vehicle should be, blends that with each GPS measurement, and outputs a cleaned position and velocity track.

`C++` `Eigen` `State estimation`

<div align="center"><img src="./portfolio/Kalman-Filter-for-GPS-Tracking/track.gif" alt="Kalman-filtered track against raw GPS samples" width="560" /></div>

```mermaid
graph LR
  RAW["Noisy GPS points"] --> PRED["Predict next state"]
  PRED --> MIX["Correct with the GPS measurement<br/>(Kalman gain)"]
  MIX --> OUT["Smoothed position and velocity"]
  OUT -->|next fix| PRED
```

### [Mean-Shift Clustering](https://github.com/shamekhing/Mean-Shift-Clustering)

A mean-shift clustering implementation in C++ and Eigen. It groups 2-D points without being told how many clusters exist, shifting each point toward its neighborhood mean until they settle together.

`C++` `Eigen` `Clustering`

<div align="center"><img src="./portfolio/Mean-Shift-Clustering/clusters.gif" alt="Mean-shift clusters over 600 points" width="560" /></div>

```mermaid
graph LR
  IN["600-point dataset"] --> STEP["Shift each point to its neighbourhood mean"]
  STEP --> CONV{"Converged?"}
  CONV -->|no| STEP
  CONV -->|yes| CLUS["Points that converge together form a cluster"]
```

### [cooda](https://github.com/shamekhing/cooda)

A complete 32-bit computer built from scratch in SystemVerilog: a 26-bit instruction set, a 64 × 32-bit register file, a bit-serial ALU, and a bus connecting BSRAM, DDR3 and an HDMI display. There is no vendor CPU core, and it boots a handwritten-digit demo over HDMI.

`SystemVerilog` `Computer Architecture` `FPGA`

_Specification from the RTL: 32-bit word, 26-bit instruction set, 64 × 32-bit register file, multi-cycle bit-serial ALU, 32 KiB BSRAM, 128 MiB DDR3, 27 MHz core clock, HDMI 720p60 output._

Datapath:

```mermaid
flowchart LR
  PC["Program counter<br/>cpu_pc"] --> FETCH["Instruction fetch<br/>read-only bus master"]
  FETCH --> IBUF["Instruction buffer<br/>32-bit word"]
  IBUF --> DEC["Decoder<br/>cpu_decoder"]
  DEC -->|"register enables<br/>ALU op · flags · memory control"| CTRL["Control"]
  DEC --> RF["Register file<br/>64 × 32-bit · 2 read · 1 write<br/>r0 hardwired to zero"]
  RF --> OPA["Operand A<br/>rs1 value"]
  RF --> OPB["Operand B mux<br/>rs2 value / immediate"]
  IBUF --> IMM["Immediate word<br/>next instruction word"]
  IMM --> OPB
  OPA --> ALU["ALU<br/>multi-cycle, bit-serial"]
  OPB --> ALU
  subgraph ALUSUB["ALU sub-units, one selected per opcode"]
    ARITH["Arithmetic<br/>add · sub · mul · div"]
    LOGIC["Logic<br/>not · and · or · xor"]
    SHIFT["Shift / rotate<br/>shl · shr · sar · rol · ror"]
    CMP["Comparator<br/>eq · ne · signed / unsigned order"]
  end
  ALU --- ALUSUB
  ALU --> WB["Writeback mux<br/>ALU result / load data"]
  WB --> RF
  ALU --> FLAGS["STATUS flags<br/>Z · N · C · V · DZ"]
  FLAGS --> DEC
  OPA --> BR["Branch unit<br/>cpu_branch"]
  OPB --> BR
  DEC -->|branch condition| BR
  BR -->|"redirect + target"| PC
  CTRL --> ALU
  CTRL --> WB
  CTRL --> FLAGS
```

Control sequence:

```mermaid
stateDiagram-v2
  [*] --> Fetch
  Fetch --> Decode: instruction word in buffer
  Fetch --> Fault: instruction-bus error
  Decode --> Fault: reserved bits set
  Decode --> Capture: decoded control
  Capture --> Run: latch rs1 / rs2 / immediate
  Run --> Memory: load or store
  Run --> Retire: ALU done
  Memory --> Retire: data-bus handshake
  Memory --> Fault: bus error
  Retire --> Fetch: PC += 4 (or += 8 with immediate)
  Retire --> Fetch: branch redirect
  Fault --> [*]: sticky until reset
  note right of Capture
    Core FSM: Idle → Capture → Run →
    Wait (memory) → Retire.
    An immediate is a second 32-bit word.
  end note
```
System bus and memory:

```mermaid
flowchart LR
  subgraph MASTERS["Bus masters"]
    IF["CPU instruction fetch<br/>slot 0"]
    DM["CPU data<br/>slot 1"]
    LD["Dataset loader<br/>UART / microSD · slot 2"]
    DISP["Display fetcher<br/>slot 3"]
  end
  IF --> ARB["4-client round-robin arbiter<br/>32-bit · byte-addressed<br/>grant held through stalls"]
  DM --> ARB
  LD --> ARB
  DISP --> ARB
  ARB --> DECODE["Address decode + alignment checks"]
  DECODE --> BSRAM["32 KiB BSRAM<br/>0x0000_0000-0x0000_7FFF<br/>boot from hex"]
  DECODE --> DDR3["128 MiB DDR3<br/>0x0800_0000-0x0FFF_FFFF<br/>800 MT/s"]
  BSRAM --> CPU["CPU"]
  DDR3 --> CPU
  DDR3 --> VIEW["HDMI 720p60<br/>448 × 448 digit"]
  LD --> DDR3
  DISP --> VIEW
  CLK["clk27: CPU · bus · BSRAM<br/>pclk: DDR3 controller<br/>pix_clk: HDMI raster"] -.-> ARB
```

Chip overview:

```mermaid
graph LR
  DS["Digit dataset<br/>(from a PC or a microSD card)"] --> LOAD["Dataset loader"]
  subgraph CHIP["One FPGA chip: a complete computer built from scratch"]
    LOAD --- BUS["System bus: instruction and data traffic"]
    BOOT["Boot memory: 32 KiB BSRAM"] --- BUS
    CPU["CPU core: fetch, decode, execute"] --- BUS
    RAM["Working memory: 128 MiB DDR3"] --- BUS
    BUS --> DISP["Display engine"]
  end
  DISP --> HDMI["HDMI screen: one digit at a time"]
```

### [fpga-usb](https://github.com/shamekhing/fpga-usb)

A USB CDC serial device implemented on a Gowin FPGA through an external ULPI PHY. It turns the FPGA into a USB device a computer can talk to, with SystemVerilog testbenches and host-side tools.

`SystemVerilog` `USB` `FPGA`
### [fpga-skill](https://github.com/shamekhing/fpga-skill)

A reusable engineering workflow for Gowin FPGA projects, distilled from many working sessions: one guide per task (RTL, simulation, synthesis, timing, programming, debugging) plus tested scripts and checklists that stop steps being skipped.

`SystemVerilog` `Gowin` `Tooling`

```mermaid
graph LR
  TASK["Identify the task"] --> ENV["Probe installed tools"]
  ENV --> REF["Read the task guide"]
  REF --> DO["Run the checked scripts and recipes"]
  DO --> CHECK{"Tests pass?"}
  CHECK -->|no| FIX["Fix using recorded pitfalls"] --> DO
  CHECK -->|yes| BOARD["Build and test on the real board"]
  BOARD --> LESSON["Feed lessons back into the guides"]
```

### [pysuwi](https://github.com/shamekhing/pysuwi)

A command-line toolbox with one rule: drop a Python file in the plugins folder and it becomes a subcommand, with no registration needed. It ships with a pinned installer and a doctor command that reports installation health.

`Python` `CLI` `Tooling`

```mermaid
graph LR
  CMD["You type a subcommand"] --> SCAN["Scan the plugins folder"]
  SCAN --> RUN["Every file there is a command: run it"]
  RUN --> RES["Result in the terminal"]
  INST["Installer: pinned, checked versions"] -.-> SCAN
```

<div align="center">
  <br />
  <em>Building at the intersection of code, hardware and intelligent systems.</em>
</div>