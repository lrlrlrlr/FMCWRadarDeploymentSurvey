# FMCW Radar Deployments in Production Vehicles

This repository provides a **systematic survey and curated dataset of FMCW radar deployments in real-world production vehicles**, with a focus on **radar count, radar type, mounting location, and supported ADAS functions**.  
It is intended to support research on **automotive radar perception, interference, security, and system design**, and to provide empirical grounding for studies that move beyond idealised single-radar assumptions.

The dataset and analysis presented here underpin our academic work on **automotive radar deployment trends**, particularly in the context of **multi-radar systems**, **interference**, and **robust perception**.

---

## Data Sources and Methodology

To characterise real-world radar configurations, we compiled deployment information for representative production vehicles using **four complementary sources**, followed by cross-validation and consolidation.

### 1. Manufacturer Documentation
Owner’s manuals, official technical brochures, and OEM websites were used to identify:
- Available ADAS features
- The presence of radar-based sensing
- Approximate sensor locations on the vehicle body (when disclosed)

### 2. Spare-Part Catalogues and Teardown Reports
Online parts catalogues, repair manuals, and teardown analyses were used to:
- Map OEM part numbers to specific radar modules
- Identify Tier-1 suppliers
- Infer radar class (e.g., LRR vs SRR/MRR)
- Determine mounting positions (front, rear, corner, etc.)

### 3. Regulatory Filings
Public regulatory databases (e.g., FCC and equivalent authorities in other regions) were consulted to:
- Confirm operating frequency bands
- Extract technical characteristics such as antenna configuration and output power
- Validate the use of automotive FMCW radar in the 76–81 GHz band

### 4. Cross-Checking and Consolidation
Information from all sources was cross-validated to:
- Resolve inconsistencies across documentation
- Construct a consolidated view of radar **counts**, **types**, and **locations**
- Ensure internal consistency across vehicle models and trims

All collected and processed data are made available in this repository.

---

## Key Observations from Deployment Data

Analysis of the compiled dataset reveals **clear and consistent deployment patterns** across vehicle segments.

### Entry-Level and Mid-Range Vehicles
- Typically deploy **a single front-facing Long-Range Radar (LRR)**
- Support core longitudinal ADAS functions such as:
  - Adaptive Cruise Control (ACC)
  - Basic Automatic Emergency Braking (AEB)
- Lateral awareness (e.g., blind-spot monitoring) is often:
  - Implemented using ultrasonic sensors, or
  - Not provided at all

### Premium and High-End Vehicles
- Increasingly adopt **multi-radar configurations**
- A common architecture includes:
  - **One front LRR**
  - **Four corner-mounted SRR/MRR units**
- This configuration enables near-**360° radar coverage**, supporting:
  - Lane-change assist
  - Blind-spot detection
  - Rear cross-traffic alert
  - Advanced parking assistance
  - Supervised highway driving features

### Emerging Trends
- Some luxury and next-generation platforms deploy **additional radars** to:
  - Improve redundancy
  - Enhance coverage of specific zones
  - Support higher-resolution perception and fault tolerance

These trends indicate a clear shift toward **radar-dense vehicles**, with important implications for **interference management, sensor fusion, and radar security**.

---
## Radar Manual References

- **Audi**
  - [AUDI OEM DELPHI.pdf](radar%20manual/AUDI%20OEM%20DELPHI.pdf)

- **Mercedes-Benz**
  - [MECEDES OEM ARS4-A.pdf](radar%20manual/MECEDES%20OEM%20ARS4-A.pdf)
  - [BENZ OEM.png](radar%20manual/BENZ%20OEM.png)

- **BMW**
  - [BMW Front OEM OAYARS5B.pdf](radar%20manual/BMW%20Front%20OEM%20OAYARS5B.pdf)
  - [BMW Front OEM OAYARS5B.png](radar%20manual/BMW%20Front%20OEM%20OAYARS5B.png)
  - [BMW REAR OEM LTQB4TR.pdf](radar%20manual/BMW%20REAR%20OEM%20LTQB4TR.pdf)
  - [BMW REAR OEM LTQB5TR.pdf](radar%20manual/BMW%20REAR%20OEM%20LTQB5TR.pdf)

- **Bosch**
  - [Bosch LRR4.pdf](radar%20manual/Bosch%20LRR4.pdf)
  - [BoschRear.pdf](radar%20manual/BoschRear.pdf)

- **Continental**
  - [Continental ARS4-B.pdf](radar%20manual/Continental%20ARS4-B.pdf)

- **Denso**
  - [Denso DNMWR006.pdf](radar%20manual/Denso%20DNMWR006.pdf)
  - [Denso DNMWR009.pdf](radar%20manual/Denso%20DNMWR009.pdf)

- **Mando**
  - [Mando MRR20.pdf](radar%20manual/Mando%20MRR20.pdf)

- **Bosch / Aptiv**
  - [MRREVO14F.pdf](radar%20manual/MRREVO14F.pdf)

- **Volvo**
  - [VOLVO FRONT WU877V12FLR.pdf](radar%20manual/VOLVO%20FRONT%20WU877V12FLR.pdf)
  - [VOLVO REAR L2C0055TR.pdf](radar%20manual/VOLVO%20REAR%20L2C0055TR.pdf)
  - [VOLVO REAR L2C0055TR.png](radar%20manual/VOLVO%20REAR%20L2C0055TR.png)

- **Hyundai / Kia**
  - [hyundai rear LTQFI7.pdf](radar%20manual/hyundai%20rear%20LTQFI7.pdf)
  - [hyundai rear.png](radar%20manual/hyundai%20rear.png)


---
## Radar Deployment Summary

| Car Model                  | # of Radars | Radar Position, Type, Model                                                     | Enabled Applications                              |
| -------------------------- | ----------- | ------------------------------------------------------------------------------- | ------------------------------------------------- |
| BMW 4 Series / X Series    | 1           | 1× Front bumper LRR (Bosch LRR4)                                                | ACC, CA, AEB                                      |
| Volkswagen Passat          | 1           | 1× Front bumper LRR (Continental ARS4-B)                                        | ACC, CA, AEB                                      |
| MG HS                      | 1           | 1× Front bumper MRR (Bosch MRRevo14F)                                           | ACC, CA, AEB                                      |
| Tesla Model 3 / Model Y    | 1           | 1× Front bumper LRR (Continental ARS4-B or Tesla “Phoenix”)                     | ACC, CA, Autopilot                                |
| BMW 3 Series               | 1           | 1× Front bumper LRR (Continental ARS4-B)                                        | ACC, CA, AEB                                      |
| Volkswagen Tiguan          | 1           | 1× Front bumper LRR (Continental ARS4-B)                                        | ACC, CA, AEB                                      |
| Toyota RAV4                | 1           | 1× Front bumper LRR (Denso DNMWR009)                                            | ACC, CA                                           |
| Mazda 3                    | 1           | 1× Front bumper LRR (Denso DNMWR006 or DNMWR011)                                | ACC, CA, AEB                                      |
| Mazda CX Series            | 1           | 1× Front bumper LRR (Denso DNMWR006)                                            | ACC, CA, AEB                                      |
| Toyota Camry               | 1           | 1× Front bumper LRR (Denso DNMWR009)                                            | ACC, CA                                           |
| Toyota Corolla             | 1           | 1× Front bumper LRR (Denso DNMWR011)                                            | ACC, CA                                           |
| Hyundai / Kia              | 1           | 1× Front bumper MRR (Mando MRR20 series)                                        | ACC, CA, AEB                                      |
| Ford F Series              | 1           | 1× Front bumper LRR (OEM ML3T-9G768-AL)                                         | ACC, CA, AEB                                      |
| Mercedes GLC Series        | 2           | 2× Front bumper MRR (Left + Right, Bosch MRRevo14F)                             | ACC, CA, AEB                                      |
| Lexus LX Series            | 3           | 1× Front LRR (Denso DNMWR009) + 2× Rear bumper SRR                              | ACC, CA, BSD, RCTA, Parking                       |
| Hyundai Ioniq 5 / 6        | 3           | 1× Front LRR (Mando MRR20) + 2× Rear corner SRR (Aptiv 42367)                   | ACC, BSD, CA, RCTA, AEB                           |
| Audi A6–A8 / S6–S8 / Q7–Q8 | 5           | 1× Front LRR (Bosch LRR4) + 4× Corner SRR (Delphi R3TR)                         | ACC, CA, BSD, LCA, RCTA, Turn Assist, Park Assist |
| Porsche Taycan             | 5           | 1× Front LRR (Bosch LRR4) + 4× Corner SRR (Delphi R3TR)                         | ACC, CA, BSD, LCA, RCTA, Turn Assist, Park Assist |
| Mercedes S-Class           | 5           | 1× Front LRR (Continental ARS4-A) + 4× Corner SRR (Bosch MRRevo14)              | ACC, CA, BSD, Parking, RCTA                       |
| BMW iX / 7 Series          | 5           | 1× Front imaging LRR (Continental ARS5) + 4× Corner SRR (Aptiv B4TR)            | ACC, LCA, AD Level-2+                             |
| Volvo XC90 / EX90          | 8           | 1× Front LRR (Veoneer 77V12FLR) + 4× Corner SRR (Delphi SRR2) + 3× Interior SRR | ACC, CA, BSD, Occupant / pet detection            |





 
