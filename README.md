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

<details>
<summary> Step-by-Step Thermal Analysis in Ansys Icepak </summary>

### 🧊 Ansys Icepak Lab – Initial Setup & Flipchip BGA Package Creation

This lab guide provides a detailed walkthrough for setting up a thermal simulation in **Ansys Icepak**, focused on a **Flipchip BGA package**. The simulation is conducted for a **1 W power input** to evaluate thermal performance.

---

### Step-by-Step Thermal Analysis Procedure

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
</details>

<details>
<summary> Final Output </summary>

The thermal simulation for the **Flipchip BGA package** at **1 W input** completes successfully, with temperature field visualization.

---

### 📸 Simulation Screenshots

<table>
  <tr>
    <td><img src="images/1_Lab/Screenshot (52).png" /></td>
    <td><img src="images/1_Lab/Screenshot (53).png" /></td>

  </tr>
  <tr>
    <td><img src="images/1_Lab/Screenshot (55).png" /></td>
    <td><img src="images/1_Lab/Screenshot (56).png" /></td>

  </tr>
  <tr>
    <td><img src="images/1_Lab/Screenshot (58).png" /></td>
    <td><img src="images/1_Lab/Screenshot (59).png" /></td>

  </tr>
  <tr>
    <td><img src="images/1_Lab/Screenshot (62).png" /></td>
    <td><img src="images/1_Lab/Screenshot (63).png" /></td>

  </tr>
  <tr>
    <td><img src="images/1_Lab/Screenshot (65).png" /></td>
    <td><img src="images/1_Lab/Screenshot (66).png" /></td>

  </tr>
  <tr>
    <td><img src="images/1_Lab/Screenshot (68).png" /></td>
    <td><img src="images/1_Lab/Screenshot (69).png" /></td>

  </tr>
  <tr>
    <td><img src="images/1_Lab/Screenshot (72).png" /></td>
    <td><img src="images/1_Lab/Screenshot (73).png" /></td>

  </tr>
  <tr>
    <td><img src="images/1_Lab/Screenshot (75).png" /></td>
    <td><img src="images/1_Lab/Screenshot (76).png" /></td>

  </tr>
  <tr>
    <td><img src="images/1_Lab/Screenshot (78).png" /></td>
    <td><img src="images/1_Lab/Screenshot (79).png" /></td>

  </tr>
  <tr>
    <td><img src="images/1_Lab/Screenshot (82).png" /></td>
    <td><img src="images/1_Lab/Screenshot (83).png" /></td>

  </tr>
  <tr>
    <td><img src="images/1_Lab/Screenshot (85).png" /></td>
    <td><img src="images/1_Lab/Screenshot (86).png" /></td>

  </tr>
  <tr>
    <td><img src="images/1_Lab/Screenshot (88).png" /></td>
    <td><img src="images/1_Lab/Screenshot (89).png" /></td>
 
  </tr>
  <tr>
    <td><img src="images/1_Lab/Screenshot (92).png" /></td>
    <td><img src="images/1_Lab/Screenshot (93).png" /></td>

  </tr>
  <tr>
    <td><img src="images/1_Lab/Screenshot (95).png" /></td>
    <td><img src="images/1_Lab/Screenshot (96).png" /></td>

  </tr>
  <tr>
    <td><img src="images/1_Lab/Screenshot (98).png" /></td>
    <td><img src="images/1_Lab/Screenshot (99).png" /></td>

  </tr>
  <tr>
    <td><img src="images/1_Lab/Screenshot (100).png" /></td>
    <td><img src="images/1_Lab/Screenshot (101).png" /></td>

  </tr>
  <tr>
    <td><img src="images/1_Lab/Screenshot (105).png" /></td>
    <td><img src="images/1_Lab/Screenshot (106).png" /></td>

  </tr>
  
</table>
</details>


<summary><h2>Module 4: Ensuring Package Reliability: Testing and Performance Validation</h2></summary>

<details>
<summary>Introduction to Package Testing and Electrical Functionality Checks</summary>

### Overview: Semiconductor Testing Across Manufacturing Stages

Comprehensive testing of semiconductor devices is essential to ensure performance, functionality, and long-term reliability. Testing is performed at multiple stages during manufacturing, including both the **Foundry** and **OSAT (Outsourced Semiconductor Assembly and Test)** phases.

---

###  Foundry-Level Testing

1. **Front-End Manufacturing**
   - Involves fabrication of integrated circuits on silicon wafers.
   - Emphasizes **process development** for high yield and quality assurance.

2. **Wafer Probe Test**
   - Electrical tests conducted on individual dies pre-dicing.
   - Identifies and marks non-functional dies.

3. **Wafer Sorting**
   - Functional dies are sorted for packaging; defective ones are discarded.

---

### OSAT-Level Testing

1. **Package Manufacturing**
   - Involves die bonding, wire or flip-chip bonding, and encapsulation.
   - Continued **process development** enhances packaging quality.

<img src="images/Screenshot (46).png"/>

2. **Package Testing**
   - Conducted in ISO Class 6/7 cleanroom conditions.
   - Includes:
     - **AOST (Assembly Open and Short Test)** – Detects shorts/opens
     - **Burn-in Testing** – Applies electrical and thermal stress
     - **Final Testing** – Verifies functionality across temperature extremes

<img src="images/Screenshot (47).png"/>

---

### 🧪 AOST: Assembly Open and Short Test

**Purpose**: Rapid identification of electrical opens or shorts in packaged devices.

- Performed post **Trim & Form** or **Singulation**
- Combines electrical testing with visual inspection (e.g., missing leads, damaged balls)
- Utilizes **Product Grade Sort (PGSRT)** to classify:
  - Best (1), Better (2, 3), Scrap (4)

**Common Defects**:
- Head on Pillow (HoP)
- Non-Wet Open (NWO)
- Bridging
- Die cracks
- Warpage (Concave/Convex)

<img src="images/Screenshot (48).png"/>

---

### 🧠 Summary

Testing at each manufacturing stage:
- Detects and eliminates defective units early
- Enhances product reliability and customer satisfaction
- Increases manufacturing yield and lowers failure rates

</details>

<details>
<summary>Reliability and Performance Testing of Semiconductor Packages</summary>

### IC Testing Procedures: Burn-in, Final Testing, and ATE Systems

This section details the core testing methodologies applied to packaged ICs, including **Burn-in**, **Final Electrical Testing**, and usage of **Automatic Test Equipment (ATE)**.

---

### Burn-in Testing

**Objective**: Identify latent defects under accelerated stress conditions (temperature, voltage, and power cycling).

- Targets early-life (infant mortality) failures
- Devices are mounted on **Burn-in boards** and subjected to oven heating
- Accelerated by high voltage and temperature
- Captures failure rates beyond the early wear-out phase

**Detected Failures**:
- Dielectric breakdown
- Metallization faults
- Electromigration

**Note**: Burn-in enhances reliability but may slightly reduce product lifespan.

<img src="images/Screenshot (49).png"/>

---

### ✅ Final Test

**Objective**: Validate the packaged IC under extreme temperature conditions as per datasheet specifications.

- Conducted with **temperature-controlled fixtures**
- Includes:
  - **Hot Test**: High-temperature electrical testing
  - **Cold Test**: Low-temperature electrical verification

**Example DUT**: LM741 Operational Amplifier (OPAMP)

<img src="images/Screenshot (50).png"/>

---

### Summary: ATE and Test Categories

**Automatic Test Equipment (ATE)** automates the electrical verification of packaged ICs through various test modes:

- **Parametric Tests**: Validate voltage/current performance
- **Functional Tests**: Ensure correct logical behavior
- **Speed Tests**: Determine maximum operating frequency

**Key Performance Indicators**:
- Yield
- Test time
- Test coverage

**Common ATE Tools**:
- In-Circuit Testers (ICT)
- Collaborative Robots (COBOT)
- Handler Units
- Teradyne Test Systems

<img src="images/Screenshot (51).png"/>

</details>



<summary> <h2> Module 5:Lab 2 - Package Design and Modeling: Building a Semiconductor Package from Scratch </h2> </summary>

<details>
<summary> Modeling Steps in AEDT </summary>

### Creating a Wire Bond Package Cross-Section in Ansys AEDT

This lab exercise guides the step-by-step construction of a semiconductor **wire bond package** using **Ansys Electronics Desktop (AEDT)**. The objective is to model the complete package cross-section, including the die, substrate, bonding wires, and mold compound.


#### 1. Start a New Project
- Launch **Ansys Electronics Desktop**
- Select **Q3D Layout Design** as the project type

#### 2. Create the Die
- Use **Modeler → Surface → Rectangle** to draw the die
- Set **thickness**: `0.2 mm`
- Rename the object to `die`
- Assign **material**: `Silicon`

#### 3. Create the Substrate
- Create another rectangle with dimensions: `5 mm x 5 mm`
- Apply a **thickness** of `-0.5 mm` to represent the substrate
- Rename as `substrate`
- Position the die on top using: `(x = -1, y = -1, z = -0.1)`

#### 4. Add Die Attach Layer
- Draw a rectangle of the same size as the die at the origin `(0, 0, 0)`
- Set **thickness**: `-0.1 mm`
- Assign **material**: `modified_epoxy` for thermal modeling

#### 5. Create the Die Pad
- Add a thin rectangle to represent the **die pad**
- Define **thickness**: `0.005 mm`

#### 6. Add Bond Pads
- Place bond pads on the die and substrate
- Assign **metallic materials** (e.g., gold or aluminum) to these pads

#### 7. Add Bond Wires
- Use the **Bondwire Tool** to create wire connections between die pads and substrate pads
- Select **gold wire** as the bonding material

#### 8. Add Mold Compound
- Create a rectangular enclosure around the die and wires
- Set **thickness**: `1.2 mm`
- Assign **material**: Epoxy mold compound for protection

</details>

<details>
<summary> Procedure in ANSYS</summary>

<table>
  <tr>
    <td><img src="images/2_Lab/Screenshot (109).png" /></td>
    <td><img src="images/2_Lab/Screenshot (110).png" /></td>

  </tr>
  <tr>
    <td><img src="images/2_Lab/Screenshot (112).png" /></td>
    <td><img src="images/2_Lab/Screenshot (113).png" /></td>

  </tr>
  <tr>
    <td><img src="images/2_Lab/Screenshot (115).png" /></td>
    <td><img src="images/2_Lab/Screenshot (116).png" /></td>

  </tr>
  <tr>
    <td><img src="images/2_Lab/Screenshot (118).png" /></td>
    <td><img src="images/2_Lab/Screenshot (119).png" /></td>

  </tr>
  <tr>
    <td><img src="images/2_Lab/Screenshot (121).png" /></td>
    <td><img src="images/2_Lab/Screenshot (122).png" /></td>

  </tr>
  <tr>
    <td><img src="images/2_Lab/Screenshot (124).png" /></td>
    <td><img src="images/2_Lab/Screenshot (125).png" /></td>

  </tr>
  <tr>
    <td><img src="images/2_Lab/Screenshot (127).png" /></td>
    <td><img src="images/2_Lab/Screenshot (128).png" /></td>

  </tr>
  <tr>
    <td><img src="images/2_Lab/Screenshot (130).png" /></td>
    <td><img src="images/2_Lab/Screenshot (131).png" /></td>

  </tr>
  <tr>
    <td><img src="images/2_Lab/Screenshot (133).png" /></td>
    <td><img src="images/2_Lab/Screenshot (134).png" /></td>

  </tr>
  <tr>
    <td><img src="images/2_Lab/Screenshot (136).png" ></td>
    <td><img src="images/2_Lab/Screenshot (137).png" /></td>

  </tr>
  <tr>
    <td><img src="images/2_Lab/Screenshot (139).png" /></td>
    <td><img src="images/2_Lab/Screenshot (140).png" /></td>

  <tr>
    <td><img src="images/2_Lab/Screenshot (142).png" /></td>
    <td><img src="images/2_Lab/Screenshot (143).png" /></td>

  </tr>
  <tr>
    <td><img src="images/2_Lab/Screenshot (145).png" /></td>
    <td><img src="images/2_Lab/Screenshot (146).png" /></td>

  </tr>
  <tr>
    <td><img src="images/2_Lab/Screenshot (148).png" /></td>
    <td><img src="images/2_Lab/Screenshot (149).png" /></td>

  </tr>
  <tr>
    <td><img src="images/2_Lab/Screenshot (151).png" /></td>
    <td><img src="images/2_Lab/Screenshot (152).png" /></td>

  </tr>
  <tr>
    <td><img src="images/2_Lab/Screenshot (154).png" /></td>
    <td><img src="images/2_Lab/Screenshot (155).png" /></td>

  </tr>
  <tr>
    <td><img src="images/2_Lab/Screenshot (157).png" /></td>
    <td><img src="images/2_Lab/Screenshot (158).png" /></td>

  </tr>
  <tr>
    <td><img src="images/2_Lab/Screenshot (161).png" /></td>
    <td><img src="images/2_Lab/Screenshot (162).png" /></td>

  </tr>
</table>

</details>
