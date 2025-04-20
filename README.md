# semiconductor-packaging

This repository offers a comprehensive overview of **semiconductor packaging**, encompassing foundational principles through to advanced 3D integration and design modeling. It integrates theoretical frameworks, practical applications, and simulation-based analyses to illustrate the complete packaging lifecycle in contemporary chip design.

Key topics include various packaging technologies—such as DIP, QFN, BGA, and 2.5D/3D ICs—alongside interposer and substrate solutions. Supplemented with diagrams, comparative tables, and ANSYS-based thermal simulations, the content also addresses reliability considerations and critical manufacturing processes.


<summary><h2>Module 1: Packaging Evolution: From Fundamentals to 3D Integration </h2></summary>

<details>
<summary>Introduction to Semiconductor Packaging and Industry Landscape</summary>

### Importance of Semiconductor Packaging

Semiconductor packaging is essential for transitioning a fragile silicon die from a cleanroom environment into real-world electronic systems. Dies produced by foundries like **TSMC, Intel, Samsung**, or **SK Hynix** require protection from corrosion, moisture, and mechanical stress.

#### 🛡️ Core Functions:
1. **Protection** of the die and its circuitry  
2. **Electrical connectivity** to logic boards and system components

A widely used format, such as the **Ball Grid Array (BGA)**, encloses the die in a protective mold and connects it to a substrate via wire bonds, enabling PCB integration.

![image](/images/Screenshot%20(22).png)

#### 🧠 Real-World Example:
In devices like the **iPhone 15**, packaged chips from companies like **Broadcom**, **STMicroelectronics**, **TI**, and **SK Hynix** are integrated on a compact logic board—underscoring the critical role of packaging in system integration.

---

### 🏭 The Semiconductor Value Chain

The industry comprises multiple players with specialized roles:

- **Fabless Companies**: Focus on IC design (e.g., Apple, AMD, Qualcomm)  
- **Foundries**: Fabricate silicon wafers (e.g., TSMC, GlobalFoundries)  
- **OSATs**: Handle packaging and testing (e.g., ASE, Amkor, JCET)  
- **IDMs**: Integrated firms managing design through manufacturing (e.g., Intel, Samsung)

#### 🔁 Workflow:
**Design → Wafer Fabrication → Package & Test → System Assembly**


![image](/images/Screenshot%20(23).png)

</details>

<details>
<summary>Understanding Package Requirements and Key Types</summary>

### 📌 Product Design Considerations

In SoC and board design, selecting an optimal package ensures performance, reliability, and integration. Packaging serves as a structural and functional bridge between the die and the board.

![image](/images/Screenshot%20(25).png)

#### 🔍 Key Selection Criteria:
- **Application-specific** needs (logic, memory, power)  
- **I/O Pin Count**  
- **Thermal Dissipation**  
- **Cost constraints**  
- **Reliability** under stress  
- **Form Factor** and size limits

---

### 🧱 Package Structure Overview

A standard IC package consists of:

- **Die**: The semiconductor core  
- **Carrier**: Routes signals between die and board  
- **PCB**: Final mounting platform  
- **Mold Compound**: Environmental protection

Mounting Types:
- **Through-hole**: e.g., DIP, PGA  
- **Surface-mount (SMT)**: e.g., QFP, QFN, CSP

![image](/images/Screenshot%20(27).png)

---

### 📦 Common Package Categories

- **Through-hole**: DIP, TO, PGA  
- **SMT**: QFN, PBGA, LGA, CSP  
- **Advanced**: MCM (Intel Broadwell), CoWoS (Nvidia H100)

</details>

<details>
<summary>Evolving Architectures: From Single-Chip to Multi-Chip Modules</summary>

### 📦 SoC Packaging Anatomy

Packaging not only safeguards the die but ensures electrical, thermal, and mechanical functionality in SoC systems.

#### 🔹 Leadframe-Based Packages
- **DIP**: Traditional, with wirebonds and external leads  
- **QFN**: Compact with exposed thermal pads  
- **Leadframe CSP & QFP**: Scaled for density and SMT

#### 🔹 Laminate-Based Packages
- **PBGA**: Wirebonded to laminated substrates  
- **Flip Chip PBGA**: Superior signal and thermal performance  
- **LGA, FC-CSP**: Common in modern devices

#### 🔹 Advanced Substrates
- **2D**: Dies placed side-by-side  
- **2.1D**: Adds RDL for better routing  
- **2.3D**: Uses organic interposers  
- **2.5D**: Silicon interposer for high-speed interconnects (e.g., CoWoS)

##### 📌 CoWoS in Practice
Combines HBM and logic SoC on a silicon interposer, used in AI and HPC platforms.

![image](/images/Screenshot%20(28).png)

</details>

<details>
<summary>Interposers, RDLs, and Advanced 2.5D/3D Packaging</summary>

### 📘 Package Architecture & Classification

Modern packages serve single-chip and multi-die systems using complex substrates and interposers.

#### 🏗️ Stack Overview
1. **Semiconductors**: SoCs or chiplets  
2. **Carrier Substrate**: Interface using interposers or thin-film  
3. **PCB**: Final system-level integration

#### 🔀 Multichip Approaches
- **Thin-Film** for compact integration  
- **TSV-less Interposers** for moderate complexity  
- **Passive/Active TSV Interposers** for vertical, high-density interconnects

#### 📦 Integration Levels
- **PBGA**: Single-die  
- **fcCSP**: Flip-chip variant  
- **2D/2.1D**: RDL-enhanced multichip  
- **2.3D–2.5D**: Interposer-enabled  
- **3D**: Full stacking with TSVs

#### 🔧 Example Applications
- **2.5D AI accelerators** with HBM  
- **fcCSP for mobile/IoT**  
- **3D packaging for datacenters and HPC**

![image](/images/Screenshot%20(29).png)

_Source: [Semiconductor Advanced Packaging by John H. Lau](https://www.amazon.com/Semiconductor-Advanced-Packaging-John-Lau/dp/1119869919)_

</details>

<details>
<summary>Comparison of Packaging Technologies</summary>

### 📦 IC Package Comparison

| **Type** | **Advantages** | **Limitations** | **Applications** |
|----------|----------------|------------------|------------------|
| **DIP** | Inexpensive, robust | Bulky, low pin count | Legacy systems |
| **QFN** | Compact, thermally efficient | Limited I/O | Mobile, telecom |
| **LGA** | High density | Fragile, tough to repair | ASICs, controllers |
| **BGA** | Excellent performance | Complex rework | High-end ICs |
| **fcCSP** | Small, cost-effective | Solder challenges | Wearables, smartphones |
| **2.1D** | Efficient integration | Longer routing | RF, datacenters |
| **2.3D** | High I/O, low cost | RDL durability | AI, HPC |
| **2.5D/3D** | High bandwidth, low latency | Expensive | Advanced compute, AI |

</details>


<summary><h2> Module 2: From Wafer to Package: Assembly and Manufacturing Essentials</h2></summary>

<details>
<summary>Supply Chain Overview and Manufacturing Facilities  </summary>

## Semiconductor Packaging – Theoretical Overview

This section presents a structured view of the **semiconductor supply chain** and the inner workings of a **package manufacturing facility**, commonly referred to as ATMP (Assembly, Testing, Marking, and Packaging).

## 🔄 Semiconductor Supply Chain

The semiconductor supply chain is a multi-step process that transforms raw silicon into fully functional electronic products. Key stages include:

### 1. 🎨 **Design House**
- **Inputs**: EDA tools, Foundry PDKs  
- **Outputs**: IC design files (e.g., GDSII), test programs  
- **Task**: Digital chip design using industry-standard software

### 2. 🧪 **Wafer Fabrication**
- **Inputs**: Silicon wafers, equipment, gases, chemicals  
- **Output**: IC-fabricated wafers  
- **Task**: Fabrication of circuits using photolithography and related techniques

### 3. 📦 **Package Assembly & Test (ATMP)**
- **Inputs**: Substrates, materials, tools  
- **Output**: Packaged ICs (e.g., Apple A15)  
- **Task**: Dicing, die attach, wire/flip-chip bonding, encapsulation, and testing

### 4. 🔧 **Board Assembly & Test**
- **Inputs**: PCBs and packaging components  
- **Output**: Assembled boards with ICs  
- **Task**: Surface-mount integration and board-level validation

### 5. 📱 **System Assembly**
- **Inputs**: Electronic components  
- **Output**: Final end-product (e.g., iPhone)  
- **Task**: Product-level integration and verification

![image](/images/Screenshot%20(33).png)


---
## 🏭 Inside a Package Manufacturing Facility (ATMP)

ATMP encompasses four core operations: **Assembly**, **Testing**, **Marking**, and **Packaging**.

### 🏢 Facility Types
- **OSAT Providers**: ASE, Amkor, TATA  
- **In-House Facilities**: Intel, TSMC, Micron, Samsung

### 🧱 Facility Layout

#### 🔹 Material Preparation
- Staging of raw materials for production

#### 🔹 Processing Zone (Cleanroom ISO Class 6 & 7)
- Die bonding  
- Wire/Flip-chip bonding  
- Encapsulation  
- RDL formation

#### 🔹 Testing Zone
- Electrical characterization  
- Burn-in and reliability testing

#### 🔹 Warehouse & Utilities
- Packaged IC storage and infrastructure support

![image](/images/Screenshot%20(34).png)

</details>

<details>
<summary>Wafer Pre-Preparation – Grinding and Dicing </summary>

### Wafer Preparation in the Cleanroom

The wafer preparation process, performed in an **ISO Class 7 cleanroom**, ensures wafer integrity during handling and processing.

#### 🔄 Process Flow

1. **Incoming Wafer Carrier** – Protective handling for contamination control  
2. **Inspection** – Visual and optical checks  
3. **Front-Side Tape Lamination** – Protection for grinding and dicing  
4. **Backside Grinding** – Thickness reduction for thermal/mechanical performance  
5. **Tape Frame Mounting** – Stabilizes dies using adhesive ring frame  
6. **Two-Step Dicing** –  
   - **Laser Grooving**: Weakens scribe lines  
   - **Blade Dicing**: Separates dies with high precision

![image](/images/Screenshot%20(35).png)

</details>

<details>
<summary>Wire Bond Packaging – From Die Attach to Molding</summary>

### 🛠️ Cleanroom Activities: Wire Bond Packaging

This section details the process flow for **wire bond packaging**, a widely used technique in semiconductor assembly.

#### ⚙️ Process Steps

1. **Die Attach** – Epoxy dispensing, chip pick and place  
2. **Curing** – Heat to secure epoxy bond  
3. **Wire Bonding** –  
   - Ball bond (EFO spark), wire loop, and crescent bond  
4. **Transfer Molding** – Encapsulation using resin  
5. **Laser Marking** – Engraving identification  
6. **Singulation** – Precision dicing of molded units

<img src="images/Screenshot (38).png" alt="Wire Bond Packaging" width="600"/>

</details>

<details>
<summary>Flip Chip Assembly – Bump Formation and Underfill</summary>

### 📦 Cleanroom Process: Flip Chip Packaging

Flip chip packaging enhances electrical performance and I/O density by mounting the die face-down on the substrate.

#### 🔩 Process Steps

1. **Bump Formation** – Solder bump deposition and reflow  
2. **Chip Flip and Placement** – Alignment with flux  
3. **Reflow** – Forms die-substrate solder joints  
4. **Flux Cleansing** – Solvent spray to prevent corrosion  
5. **Underfill Application and Cure** – Mechanical and thermal enhancement  
6. **Molding and Marking** – Encapsulation and traceability  
7. **Ball Mounting and Final Reflow** – External connections formed

<img src="images/Screenshot (39).png" alt="Flip Chip Process" width="600"/>

</details>

<details>
<summary>Wafer-Level Packaging and Final Steps</summary>

### 🧩 Wafer-Level Packaging (WLP)

WLP enables IC packaging directly on the wafer, offering reduced size and cost benefits.

#### 🔁 Reconstitution Workflow

1. **Die Placement** – Good dies placed on temporary carrier  
2. **Molding** – Formation of reconstituted wafer  
3. **Carrier Release** – Final molded structure

#### 🔧 RDL Steps

1. **Dielectric & Metal Coating**  
2. **RDL Patterning**  
3. **Solder Ball Attachment**  
4. **Laser Marking & Singulation**

<img src="images/Screenshot (43).png" alt="Wafer Level Packaging" width="600"/>

</details>


<summary> <h2> Module 3: Lab 1 - Thermal Simulation of Semiconductor Packages with ANSYS </h2> </summary>

### 🧊 Ansys Icepak Lab – Initial Setup & Flipchip BGA Package Creation

This lab guide provides a detailed walkthrough for setting up a thermal simulation in **Ansys Icepak**, focused on a **Flipchip BGA package**. The simulation is conducted for a **1 W power input** to evaluate thermal performance.

---

### Step-by-Step Thermal Analysis in Ansys Icepak

#### Step 1: Insert Icepak Design
- Launch **Ansys Workbench**
- Go to `Project` → `Insert Icepak Design`

---

#### Step 2: Open Icepak Layout
- Click the **Icepak** tab to access the layout environment

---

#### Step 3: Create a Flipchip BGA Package
- Navigate to `Icepak` → `Toolkit` → `Geometry` → `Packages` → `Flipchip_BGA`
- In the configuration window, set:
  - **xLength**: 15 mm
  - **yLength**: 15 mm
  - **Package Thickness**: 3 mm
  - **Model Type**: Detailed
  - **Symmetry**: Full
- Click **OK** to generate and visualize the model

---

#### Step 4: Review the Model Structure
- Expand the **Solids** section in the **Model Tree** to inspect:
  - `Substrate`
  - `Die`
  - `Underfill`, and others

---

####  Step 5: Assign Thermal Power
- Go to `Project Manager` → `Thermal`
- Set **Power** input to `1 W` → Click **OK**

---

####  Step 6: Define Thermal Sources
- In **Solids**, select `Flipchip-BGA1_substrate`
  - Right-click → `Assign Thermal` → `Source`
  - Set **Thermal Condition** to `Ambient Temperature` → Click **OK**
- Remove unnecessary elements (e.g., `Flipchip_BGA_trace1` under Thermal)

---

#### Step 7: Assign Temperature Monitors
- In `Solids`, assign temperature monitors to:
  - `Substrate`
  - `Die`
  - `Underfill`

---

#### Step 8: Generate Mesh
- Navigate to the **Mesh** tab
- Go to `Simulation` → `Generate Mesh`
- Save the file when prompted

---

#### Step 9: Verify Mesh Quality
- In **Mesh Visualization**, use `Quality` tools to check:
  - Face Alignment
  - Skewness
  - Volume parameters

---

#### Step 10: Validate Setup
- Click `Validate` from the main toolbar
- Ensure all configuration checks return green status

---

#### Step 11: Run Simulation & Plot Results
- Click `Analyze All` from the top menu
- Select `Flipchip BGA` package
- Go to `Plot Field` → `Temperature` → `Temperature`

##### Output Configuration:
- Enable:
  - `Specify Name`
  - `Specify Folder`
  - `Plot on Surface Only`
- Under **Surface Smoothing**, select **Gaussian Smoothing**
- Confirm with **OK**, then click **Done**

---

### Final Output

The thermal simulation for the **Flipchip BGA package** at **1 W input** completes successfully, with temperature field visualization.

---

### 📸 Simulation Screenshots

<table>
  <tr>
    <td><img src="images/1_Lab/Screenshot (52).png" width="1500"/></td>
    <td><img src="images/1_Lab/Screenshot (53).png" width="1500"/></td>

  </tr>
  <tr>
    <td><img src="images/1_Lab/Screenshot (55).png" width="250"/></td>
    <td><img src="images/1_Lab/Screenshot (56).png" width="250"/></td>
    <td><img src="images/1_Lab/Screenshot (57).png" width="250"/></td>
  </tr>
  <tr>
    <td><img src="images/1_Lab/Screenshot (58).png" width="250"/></td>
    <td><img src="images/1_Lab/Screenshot (59).png" width="250"/></td>
    <td><img src="images/1_Lab/Screenshot (60).png" width="250"/></td>
  </tr>
  <tr>
    <td><img src="images/1_Lab/Screenshot (62).png" width="250"/></td>
    <td><img src="images/1_Lab/Screenshot (63).png" width="250"/></td>
    <td><img src="images/1_Lab/Screenshot (64).png" width="250"/></td>
  </tr>
  <tr>
    <td><img src="images/1_Lab/Screenshot (65).png" width="250"/></td>
    <td><img src="images/1_Lab/Screenshot (66).png" width="250"/></td>
    <td><img src="images/1_Lab/Screenshot (67).png" width="250"/></td>
  </tr>
  <tr>
    <td><img src="images/1_Lab/Screenshot (68).png" width="250"/></td>
    <td><img src="images/1_Lab/Screenshot (69).png" width="250"/></td>
    <td><img src="images/1_Lab/Screenshot (70).png" width="250"/></td>
  </tr>
  <tr>
    <td><img src="images/1_Lab/Screenshot (72).png" width="250"/></td>
    <td><img src="images/1_Lab/Screenshot (73).png" width="250"/></td>
    <td><img src="images/1_Lab/Screenshot (74).png" width="250"/></td>
  </tr>
  <tr>
    <td><img src="images/1_Lab/Screenshot (75).png" width="250"/></td>
    <td><img src="images/1_Lab/Screenshot (76).png" width="250"/></td>
    <td><img src="images/1_Lab/Screenshot (77).png" width="250"/></td>
  </tr>
  <tr>
    <td><img src="images/1_Lab/Screenshot (78).png" width="250"/></td>
    <td><img src="images/1_Lab/Screenshot (79).png" width="250"/></td>
    <td><img src="images/1_Lab/Screenshot (80).png" width="250"/></td>
  </tr>
  <tr>
    <td><img src="images/1_Lab/Screenshot (82).png" width="250"/></td>
    <td><img src="images/1_Lab/Screenshot (83).png" width="250"/></td>
    <td><img src="images/1_Lab/Screenshot (84).png" width="250"/></td>
  </tr>
  <tr>
    <td><img src="images/1_Lab/Screenshot (85).png" width="250"/></td>
    <td><img src="images/1_Lab/Screenshot (86).png" width="250"/></td>
    <td><img src="images/1_Lab/Screenshot (87).png" width="250"/></td>
  </tr>
  <tr>
    <td><img src="images/1_Lab/Screenshot (88).png" width="250"/></td>
    <td><img src="images/1_Lab/Screenshot (89).png" width="250"/></td>
    <td><img src="images/1_Lab/Screenshot (90).png" width="250"/></td>
  </tr>
  <tr>
    <td><img src="images/1_Lab/Screenshot (92).png" width="250"/></td>
    <td><img src="images/1_Lab/Screenshot (93).png" width="250"/></td>
    <td><img src="images/1_Lab/Screenshot (94).png" width="250"/></td>
  </tr>
  <tr>
    <td><img src="images/1_Lab/Screenshot (95).png" width="250"/></td>
    <td><img src="images/1_Lab/Screenshot (96).png" width="250"/></td>
    <td><img src="images/1_Lab/Screenshot (97).png" width="250"/></td>
  </tr>
  <tr>
    <td><img src="images/1_Lab/Screenshot (98).png" width="250"/></td>
    <td><img src="images/1_Lab/Screenshot (99).png" width="250"/></td>
    <td><img src="images/1_Lab/Screenshot (100).png" width="250"/></td>
  </tr>
  <tr>
    <td><img src="images/1_Lab/Screenshot (100).png" width="250"/></td>
    <td><img src="images/1_Lab/Screenshot (101).png" width="250"/></td>
    <td><img src="images/1_Lab/Screenshot (102).png" width="250"/></td>
  </tr>
  <tr>
    <td><img src="images/1_Lab/Screenshot (105).png" width="250"/></td>
    <td><img src="images/1_Lab/Screenshot (106).png" width="250"/></td>
    <td><img src="images/1_Lab/Screenshot (107).png" width="250"/></td>
  </tr>
  
</table>

# Create the Semiconductor package cross-section in Ansys AEDT

<summary> <h2> Lab 2:Package Design and Modeling: Building a Semiconductor Package from Scratch </h2> </summary>

<table>
  <tr>
    <td><img src="images/2_Lab/Screenshot (109).png" width="250"/></td>
    <td><img src="images/2_Lab/Screenshot (110).png" width="250"/></td>
    <td><img src="images/2_Lab/Screenshot (111).png" width="250"/></td>
  </tr>
  <tr>
    <td><img src="images/2_Lab/Screenshot (112).png" width="250"/></td>
    <td><img src="images/2_Lab/Screenshot (113).png" width="250"/></td>
    <td><img src="images/2_Lab/Screenshot (114).png" width="250"/></td>
  </tr>
  <tr>
    <td><img src="images/2_Lab/Screenshot (115).png" width="250"/></td>
    <td><img src="images/2_Lab/Screenshot (116).png" width="250"/></td>
    <td><img src="images/2_Lab/Screenshot (117).png" width="250"/></td>
  </tr>
  <tr>
    <td><img src="images/2_Lab/Screenshot (118).png" width="250"/></td>
    <td><img src="images/2_Lab/Screenshot (119).png" width="250"/></td>
    <td><img src="images/2_Lab/Screenshot (120).png" width="250"/></td>
  </tr>
  <tr>
    <td><img src="images/2_Lab/Screenshot (121).png" width="250"/></td>
    <td><img src="images/2_Lab/Screenshot (122).png" width="250"/></td>
    <td><img src="images/2_Lab/Screenshot (123).png" width="250"/></td>
  </tr>
  <tr>
    <td><img src="images/2_Lab/Screenshot (124).png" width="250"/></td>
    <td><img src="images/2_Lab/Screenshot (125).png" width="250"/></td>
    <td><img src="images/2_Lab/Screenshot (126).png" width="250"/></td>
  </tr>
  <tr>
    <td><img src="images/2_Lab/Screenshot (127).png" width="250"/></td>
    <td><img src="images/2_Lab/Screenshot (128).png" width="250"/></td>
    <td><img src="images/2_Lab/Screenshot (129).png" width="250"/></td>
  </tr>
  <tr>
    <td><img src="images/2_Lab/Screenshot (130).png" width="250"/></td>
    <td><img src="images/2_Lab/Screenshot (131).png" width="250"/></td>
    <td><img src="images/2_Lab/Screenshot (132).png" width="250"/></td>
  </tr>
  <tr>
    <td><img src="images/2_Lab/Screenshot (133).png" width="250"/></td>
    <td><img src="images/2_Lab/Screenshot (134).png" width="250"/></td>
    <td><img src="images/2_Lab/Screenshot (135).png" width="250"/></td>
  </tr>
  <tr>
    <td><img src="images/2_Lab/Screenshot (136).png" width="250"/></td>
    <td><img src="images/2_Lab/Screenshot (137).png" width="250"/></td>
    <td><img src="images/2_Lab/Screenshot (138).png" width="250"/></td>
  </tr>
  <tr>
    <td><img src="images/2_Lab/Screenshot (139).png" width="250"/></td>
    <td><img src="images/2_Lab/Screenshot (140).png" width="250"/></td>
    <td><img src="images/2_Lab/Screenshot (141).png" width="250"/></td>
  </tr>
  <tr>
    <td><img src="images/2_Lab/Screenshot (142).png" width="250"/></td>
    <td><img src="images/2_Lab/Screenshot (143).png" width="250"/></td>
    <td><img src="images/2_Lab/Screenshot (144).png" width="250"/></td>
  </tr>
  <tr>
    <td><img src="images/2_Lab/Screenshot (145).png" width="250"/></td>
    <td><img src="images/2_Lab/Screenshot (146).png" width="250"/></td>
    <td><img src="images/2_Lab/Screenshot (147).png" width="250"/></td>
  </tr>
  <tr>
    <td><img src="images/2_Lab/Screenshot (148).png" width="250"/></td>
    <td><img src="images/2_Lab/Screenshot (149).png" width="250"/></td>
    <td><img src="images/2_Lab/Screenshot (150).png" width="250"/></td>
  </tr>
  <tr>
    <td><img src="images/2_Lab/Screenshot (151).png" width="250"/></td>
    <td><img src="images/2_Lab/Screenshot (152).png" width="250"/></td>
    <td><img src="images/2_Lab/Screenshot (153).png" width="250"/></td>
  </tr>
  <tr>
    <td><img src="images/2_Lab/Screenshot (154).png" width="250"/></td>
    <td><img src="images/2_Lab/Screenshot (155).png" width="250"/></td>
    <td><img src="images/2_Lab/Screenshot (156).png" width="250"/></td>
  </tr>
  <tr>
    <td><img src="images/2_Lab/Screenshot (157).png" width="250"/></td>
    <td><img src="images/2_Lab/Screenshot (158).png" width="250"/></td>
    <td><img src="images/2_Lab/Screenshot (159).png" width="250"/></td>
  </tr>
  <tr>
    <td><img src="images/2_Lab/Screenshot (161).png" width="250"/></td>
    <td><img src="images/2_Lab/Screenshot (162).png" width="250"/></td>
    <td><img src="images/2_Lab/Screenshot (163).png" width="250"/></td>
  </tr>
</table>
