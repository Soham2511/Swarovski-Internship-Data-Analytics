# Data Description

The dataset used in this project is proprietary and cannot be shared publicly.  
Below are sample structures of each dataset to help understand the schema.

---

## 1. CP Results (`cp_results.csv`)

Main dataset containing manufacturing batch data, defect counts, and yield (Okper).

### Sample Data

| Art | Code | BatchNo | wCPg | OkQty | Okper | GDper | RCDper | SFInDate | PackedDate |
|-----|------|--------|------|-------|-------|-------|--------|----------|------------|
| A.XXXX.MM10.0 | 650 | B001 | 143.676 | 10600 | 46.63 | 19.71 | 33.66 | 16/01/2023 | 12/01/2024 |
| A.XXXX.MM10.0 | 815 | B002 | 143.679 | 10500 | 52.28 | 16.37 | 31.35 | 10/02/2023 | 09/01/2024 |
| A.XXXX.MM6.0  | 296 | B003 | 30.76   | 47002 | 85.69 | 4.41  | 9.9   | 28/02/2023 | 02/01/2024 |
| A.XXXX.MM8.0  | 969 | B004 | 73.368  | 14751 | 54.26 | 17.24 | 28.5  | 10/06/2023 | 28/01/2024 |
| A.XXXX.MM8.0  | 650 | B005 | 73.368  | 19000 | 71.09 | 11.62 | 17.29 | 12/07/2023 | 15/01/2024 |

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
| 101 | Color_A |
| 102 | Color_B |
| 103 | Color_C |
| 104 | Color_D |
| 105 | Color_E |
| 106 | Color_F |
| 107 | Color_G |
| 108 | Color_H |
| 109 | Color_I |
| 110 | Color_J |

---

**Note:**  
- Color codes and names have been anonymized for confidentiality.  
- Original dataset contains detailed color mappings used in production.

---

## 3. Product Code (`product_code.csv`)

Mapping of product codes to product categories.

### Sample Data

| Code | Product |
|------|--------|
| P101 | Type_A |
| P102 | Type_B |
| P103 | Type_C |
| P104 | Type_D |
| P105 | Type_E |
| P106 | Type_F |
| P107 | Type_G |
| P108 | Type_H |
| P109 | Type_I |
| P110 | Type_J |

---

**Note:**  
- Product codes and descriptions have been anonymized for confidentiality.  
- Original dataset contains detailed product types based on bead shape and drilling configuration.

---

## 4. Data Dictionary (`dictionary.csv`)

This file provides a high-level description of features used in the dataset.

---

### Core Features

| Feature Type | Description |
|-------------|------------|
| Product Information | Includes product type, size, and identifiers |
| Batch Information | Production batch and tracking identifiers |
| Weight Metrics | Measurements related to bead weight and processing |
| Quantity Metrics | Counts of processed and accepted beads |
| Date Features | Production and packaging timestamps |

---

### Defect Features

| Feature Type | Description |
|-------------|------------|
| Glass Defects (%) | Percentage of defects observed in initial material stage |
| Coating Defects (%) | Percentage of defects during coating process |
| Removing Defects (%) | Percentage of defects during finishing/removal stage |

---

### Derived Metrics

| Feature Type | Description |
|-------------|------------|
| Yield Metrics | Percentage of accepted beads (target variable: Okper) |
| Defect Ratios | Relative proportion of defects across stages |
| Process Efficiency | Ratios comparing output vs theoretical capacity |

---

### Defect Counts

| Feature Type | Description |
|-------------|------------|
| Absolute Defect Counts | Number of defects observed across different stages |

---

### Time Features

| Feature Type | Description |
|-------------|------------|
| Production Time | Month and year of manufacturing |
| Packaging Time | Month and year of packaging |

---

### Other

| Feature Type | Description |
|-------------|------------|
| Loss | Percentage of material loss during handling |

---

## Note
- These samples are illustrative and do not represent actual data values.  
- Actual dataset must be placed in the `data/` folder to run the project.
