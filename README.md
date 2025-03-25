# Pressure Equipment Thickness Calculator

## Overview
This web application provides engineering tools for calculating minimum required thickness for various pressure equipment components according to industry standards. The calculator includes modules for three major standards and a reference section for material allowable stress values.

## Main Modules

### 1. ASME Section VIII Calculator
Calculates minimum thickness for pressure vessel components according to ASME Boiler and Pressure Vessel Code, Section VIII, Division 1.

**Supported Components:**
- Cylindrical Shells
- Spherical Shells
- Elliptical Heads (2:1)
- Hemispherical Heads
- Torispherical Heads (ASME Flanged & Dished)
- Nozzles/Openings

**Key Formulas:**
- Cylindrical Shell: t = (P × R) / (S × E - 0.6 × P) + CA
- Spherical Shell: t = (P × R) / (2 × S × E - 0.2 × P) + CA
- Elliptical Head: t = (P × D × K) / (2 × S × E - 0.2 × P) + CA
- Torispherical Head: t = (0.855 × P × L) / (S × E - 0.1 × P) + CA

### 2. ASME B31.3 Calculator
Calculates minimum thickness for process piping according to ASME B31.3 standard.

**Key Formula:**
t = (P × D) / (2 × (S × E + P × Y)) + CA

Where:
- P = internal design pressure
- D = outside diameter
- S = allowable stress
- E = longitudinal weld joint factor
- Y = temperature coefficient (0.4 for ≤900°F, 0.7 for >900°F)
- CA = corrosion allowance

### 3. API 653 Calculator
Calculates minimum thickness for storage tank components according to API 653 standard.

**Supported Calculations:**
- Shell Course (1-Foot Method)
- Tank Bottom

**Key Formulas:**
- Shell Course: t = (2.6 × H × D × G × (H - h + 1)) / (S × E) + CA
- Tank Bottom: t = 0.039 × D × √G + CA

Where:
- H = height from bottom to maximum fluid height
- D = nominal tank diameter
- G = specific gravity of fluid
- h = height from bottom to center of shell course
- S = allowable stress
- E = joint efficiency
- CA = corrosion allowance

### 4. Allowable Stress Values
Provides reference tables of allowable stress values for various materials according to ASME Section II Part D.

**Material Categories:**
- Carbon Steels
- Stainless Steels
- Nickel Alloys

**Features:**
- Filterable by material type
- Searchable by keyword
- Temperature interpolation tool

## Input Parameters

### Common Inputs:
- Design pressure (P)
- Diameter (D) or radius (R)
- Allowable stress (S)
- Joint efficiency/factor (E)
- Corrosion allowance (CA)

### Special Inputs:
- Temperature coefficient (Y) for B31.3
- Specific gravity (G) for API 653
- Mill tolerance (%) for B31.3

## Units
The calculator supports both US Customary and Metric units:
- US Customary: psi, inches, feet
- Metric: MPa, mm, meters

## Technical Implementation
The web application is built using HTML, CSS, and JavaScript. It features:
- Tabbed interface for different standards
- Interactive form validation
- Calculation result display with formula breakdown
- Responsive design for different screen sizes
- Tooltips for parameter explanations
