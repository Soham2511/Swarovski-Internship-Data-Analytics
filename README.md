# Data Description

The dataset used in this project is proprietary and cannot be shared publicly.  
Below are sample structures of each dataset to help understand the schema.

---

## 1. CP Results (`cp_results.csv`)

Main dataset containing manufacturing batch data, defect counts, and yield (Okper).

### Sample Data

| Art | Code | BatchNo | wCPg | OkQty | Okper | GDper | RCDper | SFInDate | PackedDate |
|-----|------|--------|------|-------|-------|-------|--------|----------|------------|
| A.5810.MM10.0 | 650 | 910229063 | 143.676 | 10600 | 46.63 | 19.71 | 33.66 | 16/01/2023 | 12/01/2024 |
| A.5810.MM10.0 | 815 | 910216858 | 143.679 | 10500 | 52.28 | 16.37 | 31.35 | 10/02/2023 | 09/01/2024 |
| A.5810.MM6.0  | 296 | 910232755 | 30.76   | 47002 | 85.69 | 4.41  | 9.9   | 28/02/2023 | 02/01/2024 |
| A.5810.MM8.0  | 969 | 910221976 | 73.368  | 14751 | 54.26 | 17.24 | 28.5  | 10/06/2023 | 28/01/2024 |
| A.5810.MM8.0  | 650 | 910223903 | 73.368  | 19000 | 71.09 | 11.62 | 17.29 | 12/07/2023 | 15/01/2024 |

---
**Note:**  
- The dataset contains a large number of columns
- Only a subset is shown here for illustration.
  
---

## 2. Colour Code (`colour_code.csv`)

Mapping of colour codes to actual colour descriptions.

### Sample Data

| Color Code | Color |
|-----------|------|
| 160 | Mauve |
| 294 | Rosaline |
| 296 | Gold |
| 298 | Black |
| 300 | Peach |
| 301 | Burgundy |
| 302 | Lt. Blue |
| 305 | Powder Almond |
| 306 | Bright Gold |
| 335 | Mystic Black |

---

**Note:**  
- The dataset contains a large number of colour codes including metallic, pastel, neon, and special finish variants.  
- Only a subset is shown here for illustration.

---

## 3. Product Code (`product_code.csv`)

Mapping of product codes to product categories.

### Sample Data

| Code | Product |
|------|--------|
| 5810 | Through hole |
| 5811 | Big size hole |
| 5816 | Drops |
| 5817 | Tops |
| 5818 | Half hole |
| 5821 | Odd size |
| 5824 | Rice shape |
| 5860 | Coin |
| 5809 | No hole |
| 5841 | Odd size |

---

**Note:**  
- Product codes represent different bead shapes and drilling types.  
- Multiple codes may correspond to variations of similar categories (e.g., "Odd size").

---

## 4. Dictionary (`dictionary.csv`)

Metadata describing column meanings and manufacturing terms.

### Sample Data

This file describes the meaning of each column in the dataset.

---

### Core Features

| Column | Description |
|--------|------------|
| Art | Product number (includes product name and size) |
| Code | Colour code |
| BatchNo | Batch number from production |
| SysNo | Unique identifier for product + size + colour |
| RBFA | Raw bead batch number |
| wCPg | Weight count of 100 beads |
| SFINkg | Weight of semi-finished batch (kg) before coating |
| OkQty | Number of beads after coating |
| GDkg | Weight removed as glass defects |
| RCDkg | Weight removed as removing/coating defects |
| SFInDate | Production date |
| PackedDate | Packing date |

---

### Glass Defects (%)

| Column | Description |
|--------|------------|
| a110 | Scratches |
| b110 | Pinholes |
| c110 | Splitters |
| d110 | Waviness |
| e110 | Flattened Pole |

---

### Coating Defects (%)

| Column | Description |
|--------|------------|
| a111 | Color Change |
| b111 | Drops |
| c111 | Lines / Dust / Spot |
| d111 | Air Bubbles |
| e111 | Coating Scratches |
| f111 | Wrong Color |
| g111 | Bubble at Hole |
| h111 | Coating Circle |

---

### Removing Defects (%)

| Column | Description |
|--------|------------|
| a112 | Excess Cutting |
| b112 | Nose |
| c112 | Peeled Coating |
| d112 | Removing Scratches |

---

### Derived Metrics

| Column | Description |
|--------|------------|
| QtyTheo | Max beads processable (based on trays) |
| SFINNos | Semi-finished bead count |
| GDNos | Glass defect count |
| RCDNos | Coating defect count |
| QtyPer | (OkQty / QtyTheo) × 100 |
| Okper | (OkQty / SFINNos) × 100 |
| GDper | (GDNos / SFINNos) × 100 |
| RCDper | (RCDNos / SFINNos) × 100 |
| totqtyno | Same as SFINNos |

---

### Defect Counts (Absolute Numbers)

| Column | Description |
|--------|------------|
| a110no – e110no | Glass defect counts |
| a111no – h111no | Coating defect counts |
| a112no – d112no | Removing defect counts |

---

### Time Features

| Column | Description |
|--------|------------|
| PackMonth | Packaging month |
| SFINMonth | Production month |
| Packyr | Packaging year |
| SFInyr | Production year |

---

### Other

| Column | Description |
|--------|------------|
| Loss | % of beads lost due to misfitting pins |

---

## Note
- These samples are illustrative and do not represent actual data values.  
- Actual dataset must be placed in the `data/` folder to run the project.
