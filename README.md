# TransJakarta Passenger Transaction & Operational Analysis

A data-driven analytics project aimed at evaluating operational performance, passenger behavior, and service efficiency of the **TransJakarta** bus network. This project utilizes descriptive and inferential statistics to deliver actionable business insights and strategic recommendations.

---

## Project Overview
TransJakarta is the backbone of public transportation in Jakarta. However, operational bottlenecks often hinder its efficiency. This project focuses on analyzing real transaction data to identify pain points in passenger distribution, travel times, and system compliance.

Based on the data analysis and supporting operational contexts, this project highlights several core focus areas:
1. Passenger congestion and bus delays during peak hours.
2. Inconsistencies in corridor travel times and *headway* management.
3. System compliance issues, such as missing tap-out records and duplicate entries.
4. Passenger demographics and payment method utilization.

---

## Key Features & Analysis Modules

The analytical workflow within the project notebook is structured as follows:

### 1. Data Cleaning & Preprocessing
* Handled missing values, particularly the **1,344 transactions (3.55%)** with missing tap-out data.
* Checked for duplicate entries, discovering **4 precise duplicate transactions** (identical timestamps and tap-in stations).
* Validated data consistency across GPS coordinates and station naming conventions.

### 2. Descriptive Analytics
* **Temporal Analysis**: Evaluated passenger volume trends across weekdays vs. weekends.
* **Corridor & Station Performance**: Identified high-traffic hubs (e.g., *Halte Penjaringan, Garuda Taman Mini, BKN*) and underutilized routes.
* **Travel Time Distribution**: Measured average trip durations, highlighting that peak hour trips average **74.5 minutes**.

### 3. Inferential Statistical Testing
* **T-Test**: Conducted to statistically verify the impact of peak vs. non-peak hours on overall trip durations.
* **Chi-Square Test**: Applied to test hypotheses regarding electronic card usage behaviors, passenger demographics (gender/birth year), and potential card misuse.

### 4. Interactive Dashboard
* Integrated with **Tableau** to present a comprehensive *Origin-Destination (OD) Matrix*, mapping out the entire passenger flow across the DKI Jakarta region.

---

## Dataset & Attributes

The primary dataset consists of **37,900 transaction rows and 22 columns**, capturing granular tap-in and tap-out passenger movements.

### Key Data Insights Summary
* **Peak vs. Off-Peak**: Weekday passenger volume (~6,800/day) vastly outweighs weekend volume (~1,800/day).
* **Corridor Inconsistency**: The *"Rusun Marunda – Waduk Pluit"* corridor shows extreme travel time volatility with an Interquartile Range (IQR) of **~58 minutes**.
* **The "Kampung Rambutan - Blok M" Dilemma**: Records the highest average duration (**~85 minutes**) despite being among the top 10 *lowest* passenger volume corridors—indicating severe route bottlenecks.

---

## Strategic Business Recommendations

To optimize fleet utilization, maximize capacity, and improve passenger satisfaction, the following measures are recommended:

1. **Peak-Hour Fleet & Crew Optimization**
   * Increase bus frequency and tighten *headway* intervals during morning (06:00–09:00) and evening (16:00–19:00) peak hours.
   * Deploy additional station marshals at high-traffic entry points like *Halte Penjaringan* to manage boarding crowds.

2. **Demographic-Based Fleet Adjustments**
   * Since the passenger base is heavily dominated by adult females, expand the deployment of **"Bus Pink" (Female-Only Fleet)**. Currently restricted to corridors 2, 3, 5, 9, and 13, these should be scaled to other high-density regular lines.

3. **Smart Passenger Information Systems**
   * Introduce a real-time, GPS-backed passenger information application. Providing live ETA (Estimated Time of Arrival) updates allows passengers to plan trips around heavy delays.

4. **Vending Machine & Payment Strategy**
   * As **Bank DKI** remains the most dominant payment method used by commuters, TransJakarta must prioritize stocking Bank DKI cards in station vending machines while aggressively promoting alternative electronic payment channels.

5. **Route Rationalization & Station Evaluation**
   * Re-evaluate the 10 corridors and 10 stations that recorded $\le 54$ transactions (some with just 1 transaction). Investigate whether these routes are dormant due to active infrastructure construction or poor strategic placement.

---

## Requirements & Technical Stack

The analysis is completely built using Python's robust data science ecosystem:

* **Data Manipulation**: `pandas`, `numpy`
* **Statistical Modeling**: `scipy` (for T-Test and Chi-Square)
* **Visualization**: `matplotlib`, `seaborn`, and **Tableau** (for spatial OD matrices)
* **Environment**: Jupyter Notebook (`.ipynb`)
