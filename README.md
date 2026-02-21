# Aviation Accident Severity Analysis (1948–2023)

## Project Overview

This project analyzes aviation accident data (1948–2023) to evaluate aircraft safety from an insurer’s perspective. The goal is to identify aircraft makes and models that demonstrate:

- Low fatal/serious passenger injury fractions  
- Low rates of total aircraft destruction  

The client is specifically interested in aircraft that are potentially still active, so the dataset was filtered to accidents occurring from 1983 onward (assuming a 40-year aircraft lifecycle).

This analysis evaluates **severity conditional on an accident occurring**, not overall accident probability.

---

## Methodology

### Data Cleaning

- Filtered data to 1983–2023
- Removed non-professional and amateur-built aircraft
- Cleaned categorical variables (Make, Model, Weather, Engines)
- Created derived metrics:
  - **Fatal/Serious Injury Fraction**  
    (Fatal + Serious Injuries) / Estimated Total Onboard
  - **Destroyed Rate**  
    Percentage of accidents classified as “Destroyed”

To ensure statistical robustness:
- Makes required ≥ 50 accidents
- Models required ≥ 10 accidents
- Factor comparisons required ≥ 50 observations per group

---

## Small vs Large Aircraft Classification

Aircraft were categorized as:

- **Small**: < 20 passengers (estimated onboard during accident)
- **Large**: ≥ 20 passengers

This classification is based on observed occupancy and does not reflect official aircraft seating capacity. Some misclassification may occur (e.g., large aircraft with low occupancy).

---

# Key Findings

---

## 1️⃣ Make-Level Recommendations

![alt text](image.png)

### Recommended Small Aircraft Makes

The following manufacturers demonstrated low injury severity and low destruction rates:

- Aviat Aircraft Inc
- Maule
- Grumman Acft Eng Cor-Schweizer
- Stinson
- Aeronca

These makes show injury fractions typically between 16–23% with relatively low destruction rates compared to other small-aircraft manufacturers.

---

### Recommended Large Passenger Aircraft Makes

Top-performing large aircraft manufacturers:

- **Embraer**
- **Boeing**

Both exhibit very low fatal/serious injury fractions (~10%) and relatively low destruction rates.

Airbus performs strongly but shows slightly higher destruction and injury metrics compared to Embraer and Boeing.

---

## 2️⃣ Model-Level Insights

![alt text](image-1.png)

![alt text](image-2.png)

Large commercial aircraft models show substantially lower severity:

Examples:

- Boeing 777 → ~0.2% injury fraction  
- Boeing 757 → ~0.3% injury fraction  
- Embraer EMB-145LR → ~1.5% injury fraction  

Small aircraft models, even strong performers, typically range between 6–19% injury fractions.

This suggests commercial jet aircraft are associated with significantly lower severity outcomes given an accident.

---

## 3️⃣ Factors Affecting Severity

### Weather Condition

![alt text](image-3.png)

IMC (poor visibility) accidents show dramatically worse outcomes:

- Injury fraction ≈ 64.7% (IMC) vs 23.7% (VMC)
- Destruction rate ≈ 36.4% (IMC) vs 7.2% (VMC)

Weather conditions are strongly associated with accident severity.

---

### Number of Engines

![alt text](image-4.png)

- Single-engine aircraft → 25.7% injury fraction
- Twin-engine aircraft → 32.5% injury fraction

Twin-engine aircraft show higher severity metrics within recorded accidents, though this may be influenced by operational differences.

---

# Overall Conclusion

Key conclusions for insurers:

- Large commercial aircraft models show substantially lower passenger injury severity.
- Certain small-aircraft manufacturers consistently outperform others in both injury and destruction metrics.
- Environmental conditions (especially IMC) are strongly associated with severe outcomes.
- Aircraft selection and operational context both materially affect severity risk exposure.

This analysis provides data-driven guidance for evaluating aircraft risk profiles based on historical accident severity outcomes.
