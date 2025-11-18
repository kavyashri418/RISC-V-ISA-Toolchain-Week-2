# System on Chip (SoC)

System-on-Chip (SoC) technology has become the foundational element of modern electronic products, enabling high performance, miniaturization, and enhanced reliability. Whether in large-scale systems such as data centers and servers or compact devices like smartphones, wearables, and sensor nodes, SoCs provide the essential computational and control capabilities required for efficient operation. They process both analog and digital signals, perform complex computations, store the processed data, and generate meaningful outputs to control external hardware or deliver information to users. A typical SoC integrates numerous logic blocks and functional units—CPU cores, memory blocks, communication interfaces, DSP engines, and power management units—onto a single silicon die. However, certain system-level components such as large display modules, mechanical keypads, antennas, and battery units generally remain external because they cannot be economically or physically implemented using CMOS or CMOS-compatible technologies such as Bi-CMOS, MEMS, or discrete memory technologies. Modern SoCs are far more advanced than the early generations, often containing hundreds of IP cores, on-chip interconnect networks, embedded memories, and expansion interfaces while operating at extremely low power. Their development demands a blend of digital VLSI design, mixed-signal custom design, and FPGA-based prototyping methodologies, making SoC design a multidisciplinary and technologically intensive process.

<img width="410" height="236" alt="Screenshot 2025-11-19 005414" src="https://github.com/user-attachments/assets/3e443638-79be-48f3-951d-1ab10b18fd04" />
<img width="389" height="244" alt="Screenshot 2025-11-19 005422" src="https://github.com/user-attachments/assets/501e6ea2-123f-46d5-9d52-a13c59afae9e" />
 
## SoC Trends

- Modern lithography methods such as EUV and double patterning, along with advanced FEOL architectures, continue to scale device dimensions beyond the 3 nm node.
- This scaling increases transistor packing density, requiring sophisticated EDA tools and complex design flows to meet performance, safety, security, and reliability demands.
- Dennard scaling predicts that shrinking devices no longer provide proportional performance improvements, especially below 5 nm, which has led to slower performance gains.
- This slowdown has encouraged innovations in device architectures, new process technologies, advanced integration techniques, and improved design methodologies.
- A major trend is the heterogeneous integration of digital cores, embedded memories, analog and RF blocks, sensors, and on-chip antennas within a single SoC.
- CMOS and CMOS-compatible processes enable the integration of diverse functional blocks on the same die.
- Traditional NAND/NOR flash technologies are reaching their limits, driving adoption of MRAM technologies such as STT-MRAM and SOT-MRAM to replace portions of cache memory.
- The rapid need for real-time AI inference in IoT, automotive, and 5G applications is increasing demand for powerful edge-AI SoCs, including analog compute-in-memory architectures.
- AI/ML workloads in data centers require massive compute and memory, motivating innovations like wafer-scale SoCs and scalable compute architectures.
- 3D-IC technology enables stacking chiplets vertically using silicon interposers and RDL, offering higher integration levels and greater design flexibility.

<img width="466" height="461" alt="Screenshot 2025-11-19 005434" src="https://github.com/user-attachments/assets/817563eb-6855-434d-b2ad-c2888f602c07" />

## Components of SoC

A typical SoC integrates several key components, including one or more general-purpose RISC processors, DSP cores, dense on-chip memory, protocol engines, and interfaces for external memory expansion and off-chip connectivity. It also includes essential housekeeping blocks such as clock generation and stabilization circuits, power management units, analog interfaces, user-interface modules, and sensor or radio interfaces depending on application needs. Additionally, every SoC incorporates software elements like bootloaders, embedded firmware, and application programs. Each block is developed using suitable design methodologies—full-custom for analog and mixed-signal circuits, automated cell-based flow for digital logic, and structured memory compilers for embedded memories—before being integrated into a single chip or multi-die package.

##  Design Abstractions of SoC Design

 Different design abstraction levels of SoC design in consideration are the following:
 • Design Model as system C or system Verilog.
 • RTL level Top hierarchy.
 • RTL level block level which could be analog or digital or cell or transistor level.
 • Structural level as design Netlist which is HDL file with standard cells/Macrocells and Memory cells and their interconnections.
 • Design layout level in GDS format cell dimensions.

## Integration of SoC Design Components

SoC design is traditionally realized by integrating analog, digital, memory macros, and standard cells using automated cell based design technique. According to the sub block design type, the cores are designed using different design flows such as custom layout, mixed system or standard cell based design flow.

##  Trends in SoC Design Methodology

<img width="317" height="615" alt="Screenshot 2025-11-19 005230" src="https://github.com/user-attachments/assets/25503fa3-7306-4e10-b777-c7e182b6a863" />

The demands of future day SoC designs are substantial. The convergence of multiple heterogeneous SoC technologies in sophisticated package requires holistic analysis of the entire solution. The current SoC design methods will not work for these requirements. Future SoC designs require hyper convergent design flow to address the complexities of systems and technologies

##  Future Trends of Systems

- Feature size reduction is expected to approach fundamental limits around 7–8 nm by the end of this decade.
- With the integration of AI, system capabilities can surpass human performance, particularly in vision and perception systems.
- Innovations continue with the development of new devices beyond CMOS, enabling enhanced functionality.
- Hundreds of NAND layers are now stacked vertically to create extremely dense memory structures.
- Quantum computing and quantum communication offer the potential for massive leaps in functionality and computational capability.
- Multiple emerging technologies are making low-cost, high-density storage more practical.
- Stacked transistors are becoming feasible, supporting higher performance and improved area efficiency.
- Future SoCs will increasingly integrate CMOS and non-CMOS devices into a single platform.
- Such heterogeneous integration is already being realized through SiP (Silicon-in-Package) technologies.
- Complex SoCs containing many cores running at different clock frequencies are simplified by assigning each IP core an independent timing domain.
- This approach makes the on-chip interconnect behave like a separate IP core, improving design modularity and timing closure.

<img width="335" height="212" alt="Screenshot 2025-11-19 005210" src="https://github.com/user-attachments/assets/83cb5eae-8060-4655-9b61-a6a94cae3069" />

System-on-Chip (SoC) technology has become the backbone of modern electronic systems, enabling high performance, compact size, and efficient power consumption within a single integrated platform. With continued scaling, heterogeneous integration, emerging memory technologies, and AI-driven architectures, SoCs are evolving to meet the growing demands of computing, communication, and intelligent automation. Future trends such as 3D-IC stacking, chiplet-based design, and integration of CMOS with non-CMOS devices will further enhance capability and flexibility. Overall, SoCs will continue to drive innovation across consumer electronics, IoT, automotive, data centers, and edge AI applications.


# Introduction to VSDBabySoC

VSDBabySoC is a compact yet powerful RISC-V-based System-on-Chip (SoC) designed primarily to integrate and test three fully open-source IP cores together for the first time. It serves as an educational, experimental, and proof-of-concept platform for open-source silicon development.
The SoC consists of three key components:
- RVMYTH microprocessor – A simple RISC-V CPU.
- 8× PLL (Phase-Locked Loop) – Generates a stable and higher-frequency clock.
- 10-bit DAC (Digital-to-Analog Converter) – Interfaces with analog devices.
This combination makes VSDBabySoC an ideal minimal SoC for learning, modeling, simulation, and physical design using open-source tools on the Sky130 process.

<img width="2270" height="1260" alt="image" src="https://github.com/user-attachments/assets/42272eb9-657e-42ab-907b-d850aeeeb087" />

### Problem Statement
The VSDBabySoC project focuses on designing and integrating a compact SoC around the RVMYTH RISC-V processor core. The SoC relies on an on-chip PLL for clock generation and a 10-bit DAC to communicate with external analog hardware.
Devices such as televisions, mobile phones, speakers, and other systems that accept analog input can interpret the DAC output and convert it into audio or visual signals.
The SoC is fabricated using the Sky130 open-source PDK, making it fully accessible for academic, learning, and hobbyist use.

### What is an SoC?
A System-on-Chip is a complete electronic system integrated on a single silicon die.
It contains various IP cores such as:
- Microprocessors / CPUs (digital)
- Memories (SRAM, ROM)
- Analog and RF blocks
- Communication units (USB, SPI, I2C, modems)
- Peripheral interfaces
- SoCs combine digital, analog, and mixed-signal components to form a full standalone solution.

### RVMYTH
RVMYTH is a simple RISC-V-based CPU core developed during a VSD–RedwoodEDA workshop.
Key points:
- Designed using TL-Verilog, a modern timing-abstract design language.
- Created in only 5 days by students, including beginners.
- Fully open-source with continuous student contributions.
- Converted to Verilog using SandPiper-SaaS for integration into SoC design flows.
- RVMYTH demonstrates how accessible open-source CPU design can be, even for new learners.

<img width="959" height="655" alt="image" src="https://github.com/user-attachments/assets/892f08e4-b021-4171-bf4f-d57a715d48dd" />

### PLL
A Phase-Locked Loop (PLL) is a control system that generates a stable, high-frequency clock signal synchronized to a reference input.
In VSDBabySoC, the 8× PLL multiplies the input clock, ensuring:
- Stable system timing
- Reliable processor operation
- Proper synchronization across the SoC
- PLLs are essential in modern SoCs for clocking, synchronization, and frequency scaling.

<img width="1027" height="331" alt="image" src="https://github.com/user-attachments/assets/0a0d929f-ca77-4e8c-af98-ee0b10ff0cb6" />

### DAC
A Digital-to-Analog Converter (DAC) converts digital values into continuous analog signals.
Applications include:
- Audio generation
- Video signal processing
- Communication systems
- Sensor interfacing
The 10-bit DAC in VSDBabySoC provides analog output values based on RVMYTH’s computation results.

<img width="740" height="446" alt="image" src="https://github.com/user-attachments/assets/45269f60-1b33-4140-9f9c-8a0c4aa9cf8d" />

### VSDBabySoC Modeling and Simulation
The SoC is modeled and simulated using the following workflow:
- Icarus Verilog (iverilog) is used to compile and simulate the Verilog modules.
- GTKWave visualizes the waveforms.
- Initial input signals activate the PLL.
- The PLL generates a stable system clock.
- The RVMYTH processor executes instructions stored in its instruction memory (imem).
- During execution, register r17 is sequentially updated with new values.
- These values feed into the DAC.
- The DAC outputs an analog-equivalent signal named OUT.

Thus, the SoC integrates:
- 3 IP cores (RVMYTH, PLL, DAC)
- 1 wrapper module
- 1 testbench for simulation
All together, these demonstrate a complete mini-SoC.

### RVMYTH Modeling
Since RVMYTH is written in TL-Verilog, it must be converted to Verilog before integration.
- SandPiper-SaaS performs this TL-Verilog → Verilog transformation.
- The referenced repository provides guidance for modeling and testing the CPU.
This allows the CPU to be synthesized, simulated, and included in the SoC.

### PLL and DAC Modeling
Analog circuits cannot be synthesized using Verilog, but they can be modeled behaviorally using real-number modeling.
- Behavioral models of PLL and DAC are taken from open-source reference repositories.
- These models mimic analog behavior sufficiently for digital-level SoC simulation.
During physical design, the PLL model was improved and adapted into a new version named AVSDPLL to meet real IP requirements.
