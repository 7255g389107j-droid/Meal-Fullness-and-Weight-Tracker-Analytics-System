# Meal-Fullness-and-Weight-Tracker-Analytics-System

A minimal, low-burden PHR protocol and Excel/VBA tracker that bridges behavioral science, compositional data statistics, and clinical medical screening for personalized medicine.

## Minimalist Nutrition & Clinical Screening Tracker (PHR Protocol)

An elegant, low-burden Personal Health Record (PHR) protocol and Excel/VBA implementation designed for personalized medicine. This system successfully resolves the historical trade-off between user compliance (low data-entry burden) and rigorous clinical utility.

By capturing only **5 to 6 data points per meal/day**, it leverages behavioral economics to prevent dropout, utilizes mathematical compositional data analysis to visualize dietary quality, and applies validated clinical criteria to screen for life-threatening pathologies.

---

## 💡 Core Philosophy & Interdisciplinary Framework

This protocol is a precise crossover of four distinct scientific domains:

1. **Behavioral Science & Cognitive Psychology**
   * **Cognitive Load Reduction:** Limits tracking to a magical number of 5–6 items, lowering friction and preventing data abandonment.
   * **Recall Bias Mitigation:** Enforces immediate post-meal logging for subjective satiety, while objective meal contents can be cross-verified post-hoc via photographs.

2. **Nutritional Science (The SV Method)**
   * Uses the **Serving (SV) Method** aligned with the dietary guidelines recommended by the Japanese Ministry of Health, Labour and Welfare and the Ministry of Agriculture, Forestry and Fisheries. It simplifies tracking into 3 core functional categories (Staple, Main, Side) without tedious gram or calorie counting.

3. **Mathematical & Statistical Analysis (Compositional Data Analysis - CoDA)**
   * Converts absolute dish counts into a **constant-sum ratio (summing to 100%)** to serve as a robust mathematical proxy for macronutrient (PFC) balance. 
   * Includes strict conditional handling (`IF Total Count > 0`) to mathematically eliminate division-by-zero errors during periods of fasting.

4. **Clinical Medicine & Epidemiology**
   * Continuously monitors baseline data for sudden deviations. When lifestyle factors (diet and exercise) remain stable, the system screens for critical hidden pathologies using internationally recognized thresholds (e.g., GLIM criteria for malnutrition).

---

## 🛠️ Data Input Protocol & 1-Count (SV) Standards

### Input Parameters
* **Date & Weight (kg):** Measured daily at a fixed time (preferably morning).
* **Staple Count:** (Carbohydrates/Energy) e.g., 1 bowl of rice, 1 slice of bread, 1 serving of noodles.
* **Main Dish Count:** (Proteins/Lipids) e.g., 1 plate of meat, 1 piece of fish, 1 egg dish, 1 soy product dish.
* **Side Dish Count:** (Vitamins/Minerals/Fiber) e.g., 1 plate of salad, 1 small side bowl, 1 cup of vegetable soup.
* **Fullness Level:** Subjective satiety scored *immediately* after eating:
  * `5` = Overeating / Stuffed
  * `3` = Appropriate / Satiated
  * `1` = Almost empty / Hungry
  * `0` = Skipped meal (Counts as 0)
* **Exercise Intensity:** Daily activity level scored from `1` (Sedentary) to `5` (High Intensity).

---

## 🚨 Automated Clinical Alert Logic (Red Flags)

The system automatically scans historical entries and triggers critical alerts when unexpected weight fluctuations occur despite a **constant** baseline of food intake and physical activity.

| Weight Fluctuation | Clinical Metric | Suspected Pathologies (Differential Diagnosis) |
| :--- | :--- | :--- |
| **Unintentional Loss** | <ul><li>≥ 5% weight loss within 6 months</li><li>OR ≥ 4.5 kg loss within 1 month</li></ul> | Malignancy (Cancer), Graves' disease (Hyperthyroidism), Worsening Diabetes Mellitus, Malabsorption Syndrome. |
| **Unintentional Gain** | <ul><li>Sudden gain of ≥ 2.0 kg within 3–7 days</li></ul> | Acute Heart Failure, Kidney Failure, Liver Failure (Edematous/Fluid-retention disorders), Hypothyroidism. |

---

## 💻 Excel/VBA Installation & Usage

This repository contains a native Excel VBA macro implementation tailored for `Sheet1`.

### Setup Instructions
1. Open your Excel workbook (Ensure the active sheet is named **`Sheet1`**).
2. Press `Alt + F11` (`Opt + F11` on Mac) to open the VBA Editor.
3. Click `Insert` > `Module` from the menu bar.
4. Paste the macro code provided in `Microsoft Excel (.xltm) Meal, Fullness, and Weight Tracker & Analytics System` into the window.
5. Close the VBA editor. 
6. (Optional) Insert a shape/button onto `Sheet1`, right-click it, select **Assign Macro**, and choose `ShowMealForm`.
7. Save the file as an **Excel Macro-Enabled Workbook (`*.xlsm`)**.

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](https://opensource.org) page for legal details.

This project is open-source. Feel free to fork, optimize, or adapt this protocol into mobile PHR applications, chat-bots, or clinical research pipelines.
