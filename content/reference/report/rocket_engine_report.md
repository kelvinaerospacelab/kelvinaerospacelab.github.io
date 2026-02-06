# Rocket Engine Performance Report (200N)

**Date**: 2026-01-31  
**Author**: Kelvin Aerospace Lab

---

## Executive Summary

| Parameter | Value |
|-----------|-------|
| Thrust | 200.0 N |
| Specific Impulse (Isp) | 238.57 s |
| Chamber Pressure | 1800000 Pa (18.00 bar) |
| O/F Mass Ratio | 1.600 |
| Effective Exhaust Velocity (c) | 2340.32 m/s |
| Characteristic Velocity (c*) | 1734.00 m/s |
| Expansion Ratio (ε) | 3.893 |

---

## Propellant Flow Distribution

| Flow Parameter | Value |
|---|---|
| **Total Mass Flow** | 0.0855 kg/s (85.46 g/s) |
| **Fuel Mass Flow (Ethanol)** | 0.0329 kg/s (32.87 g/s) |
| **Oxidizer Mass Flow (GOX)** | 0.0526 kg/s (52.59 g/s) |

---

## Nozzle Design

### Throat Section
| Parameter | Value |
|---|---|
| Throat Area (At) | 8.232475e-5 m² (82.325 mm²) |
| Throat Diameter (dt) | 10.2381 mm |
| Throat Radius (rt) | 5.1191 mm |

### Exit Section
| Parameter | Value |
|---|---|
| Exit Area (Ae) | 3.204902e-4 m² (320.490 mm²) |
| Exit Diameter (de) | 20.2005 mm |
| Expansion Ratio (Ae/At) | 3.8930 |

---

## Combustion Chamber Design

| Parameter | Value |
|---|---|
| Characteristic Length (L*) | 1.5000 m (1500.0 mm) |
| Chamber Volume (Vc) | 1.234871e-4 m³ (123.5 cm³) |

### Chamber Geometry Options (Contraction Ratio Variants)
Shown for reference with L* = 1.5000 m:

| Ac/At | Ac (cm²) | dc (mm) | Hc (mm) | Vc (cm³) |
|-------|----------|---------|---------|----------|
| 3 | 2.47 | 12.5 | 500 | 123 |
| 5 | 4.12 | 16.2 | 300 | 123 |
| 7 | 5.76 | 19.2 | 214 | 123 |
| 10 | 8.23 | 22.9 | 150 | 123 |

---

## Ethanol Injector (Fuel)

### Input Parameters
| Parameter | Value | Unit |
|---|---|---|
| Mass Flow | 0.0329 | kg/s |
| Injection Temperature | 293.15 | K |
| Injection Pressure | 2160000 | Pa |
| Chamber Pressure | 1800000 | Pa |
| Pressure Drop (ΔP) | 360000 | Pa |
| Discharge Coefficient (Cd) | 0.600 | — |
| Specific Heat Ratio (γ) | 1.130 | — |
| Molar Mass | 46.07 | g/mol |
| Gas Constant (R) | 123.00 | J/(kg·K) |

### Calculated Properties
| Property | Value |
|---|---|
| Y-factor (compressibility) | 1.0000 |
| Injection Density (ρ) | 789.0000 m³/kg |
| State | Gaseous |

### Orifice Sizing
| Parameter | Value |
|---|---|
| Total Orifice Area | 2.298394e-6 m² (2.298 mm²) |
| Equivalent Single Orifice Diameter | 1.7107 mm |

**Formula Used**: $A_o = \frac{\dot{m}}{Y \cdot C_d \cdot \sqrt{2\rho \Delta P}}$

---

## GOX Injector (Oxidizer)

### Input Parameters
| Parameter | Value | Unit |
|---|---|---|
| Mass Flow | 0.0526 | kg/s |
| Injection Temperature | 293.15 | K |
| Injection Pressure | 2340000 | Pa |
| Chamber Pressure | 1800000 | Pa |
| Pressure Drop (ΔP) | 540000 | Pa |
| Discharge Coefficient (Cd) | 0.600 | — |
| Specific Heat Ratio (γ) | 1.400 | — |
| Molar Mass | 32.00 | g/mol |
| Gas Constant (R) | 259.80 | J/(kg·K) |
| Number of Orifices | 8 | — |

### Calculated Properties
| Property | Value |
|---|---|
| Y-factor (compressibility) | 0.9324 |
| Injection Density (ρ) | 30.7246 kg/m³ |
| Mode | Subsonic |

### Orifice Sizing
| Parameter | Value |
|---|---|
| Total Orifice Area | 1.631862e-5 m² (16.319 mm²) |
| Per-Orifice Area | 2.039828e-6 m² (2.040 mm²) |
| Per-Orifice Diameter | 1.6116 mm |

**Formula Used**: $A_o = \frac{\dot{m}}{Y \cdot C_d \cdot \sqrt{2\rho \Delta P}}$

---

## Thermodynamic Data

### Combustion Reaction
$$C_2H_5OH + 3\,O_2 \rightarrow 2\,CO_2 + 3\,H_2O$$

### Propellant Properties
| Property | Ethanol | GOX |
|---|---|---|
| Molar Mass | 46.07 g/mol | 31.998 g/mol |
| Specific Gas Constant | 123.0 J/(kg·K) | 259.8 J/(kg·K) |
| γ (specific heat ratio) | 1.130 | 1.400 |

---

## Report Generation Details

- Generated on: 2026-01-31
- Calculation System: KelvinAero Rocket Calculator
- Based on: Rust
- All calculations performed at sea level

