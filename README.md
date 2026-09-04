# Manufacturing Capacity Planning & Production Optimization

## A AUTO COMPONENTS PVT. LTD.

Excel-based manufacturing capacity planning, production optimization, bottleneck analysis and scenario modelling project for a simulated automotive components manufacturer.

---

##  Project Overview

This project develops an end-to-end **manufacturing capacity planning and production optimization model** for a simulated automotive components company, **A Auto Components Pvt. Ltd.**

The objective is to determine whether current manufacturing capacity is sufficient to meet forecast demand, identify machine-level bottlenecks, evaluate Overall Equipment Effectiveness (OEE), prioritize production based on economic contribution and criticality, and test alternative capacity improvement scenarios.

The project was developed entirely in **Microsoft Excel**, using structured datasets, formulas, analytical models, scenario analysis and a management dashboard.

---

##  Business Problem

A manufacturing company needs to answer several operational questions:

- Is current machine capacity sufficient to meet forecast demand?
- Which machines are operating beyond their available capacity?
- Where are the major production bottlenecks?
- Are capacity constraints caused by insufficient machine hours, downtime or production efficiency?
- Which components should receive higher production priority?
- Which components generate the highest contribution relative to the machine time they consume?
- Can operational improvements solve capacity shortages without immediately adding machines?
- What would happen if scheduled hours increased or downtime and inefficiencies were reduced?

This project addresses these questions through an integrated production planning and capacity analysis framework.

---

#  Analytical Framework

The project follows the following analytical flow:

**Demand Planning**
↓  
**Inventory & Production Requirements**
↓  
**Machine Capacity Analysis**
↓  
**OEE Analysis**
↓  
**Bottleneck Identification**
↓  
**Economic Contribution Analysis**
↓  
**Production Priority**
↓  
**Capacity Scenario Analysis**
↓  
**Management Dashboard & Recommendations**

---

#  Dataset

The project uses simulated manufacturing data representing an automotive components company.

### Dataset Scope

| Metric | Value |
|---|---:|
| Total Components | 500 |
| Make Components | 300 |
| Buy Components | 200 |
| Total Machines | 25 |

The 300 internally manufactured components are used for machine capacity and production planning analysis.

The 200 externally sourced components remain part of the demand and inventory planning structure but are not included in internal machine-capacity calculations.

---

#  Manufacturing Data

The component dataset contains information including:

- Component ID
- Component Name
- Product Family
- Category
- Component Size
- Sourcing Type
- Criticality
- Monthly Demand
- Demand Growth Rate
- Forecast Demand
- Opening Inventory
- Safety Stock
- Assigned Machine
- Ideal Cycle Time
- Actual Cycle Time
- Setup Time
- Changeover Time
- Operators Required
- Labour Hours per Unit
- Defect Rate
- Labour Efficiency
- Cost information
- Selling Price
- Contribution
- Machine Hours
- Production Requirements
- Quality Rate
- Performance Rate
- Availability Rate
- OEE

Machine-level data includes:

- Scheduled Hours
- Planned Downtime
- Unplanned Downtime
- Available Production Hours
- Required Production Units
- Required Machine Hours
- Capacity Surplus / Shortage
- Machine Utilization
- Capacity Status

---

#  Analyses Performed

## 1. Demand Planning

Forecast demand was incorporated into production planning to determine the expected production requirement for each component.

Demand planning considers:

- Current demand
- Demand growth
- Forecast demand
- Opening inventory
- Safety stock

---

## 2. Inventory & Production Requirement

Inventory levels were incorporated into production requirements to determine how many units need to be manufactured internally.

The model considers:

- Forecast demand
- Opening inventory
- Safety stock
- Net requirement
- Required good units
- Gross requirement
- Planned production

This converts demand information into an operational production requirement.

---

#  3. Machine Capacity Analysis

Machine capacity was evaluated by comparing available machine hours with the machine hours required to manufacture the planned production volume.

### Base Capacity Results

| Metric | Result |
|---|---:|
| Total Available Machine Capacity | 104,309.28 hours |
| Total Required Machine Hours | 104,382.33 hours |
| Overall Utilization | 100.07% |
| Machines in Capacity Shortage | 13 |
| Machines with Spare Capacity | 0 |

The analysis shows that the current production plan requires slightly more machine time than the available capacity.

Although the overall gap is relatively small, the shortage is concentrated across specific machines, creating operational bottlenecks.

---

# 4. Bottleneck Analysis

Machine utilization and capacity shortage were combined with OEE information to identify the most critical bottleneck machines.

### Critical Bottleneck Machines

| Machine | Utilization | Capacity Shortage |
|---|---:|---:|
| M020 | 104.32% | -172.95 hrs |
| M002 | 103.95% | -158.46 hrs |
| M006 | 103.11% | -125.83 hrs |
| M019 | 102.92% | -118.55 hrs |
| M004 | 102.35% | -95.69 hrs |

These machines represent the most significant capacity constraints in the current production configuration.

### Key Finding

The issue is not simply a lack of total machine capacity.

The more important operational issue is **how production requirements are distributed across individual machines**.

Several machines are operating above 100% utilization while other machines have relatively more available capacity.

This indicates that machine loading and capacity balancing should be considered before immediately investing in additional equipment.

---

#  5. Overall Equipment Effectiveness (OEE)

OEE was calculated using:

**OEE = Availability × Performance × Quality**

The model evaluates:

- Availability
- Performance
- Quality
- Overall Equipment Effectiveness
- OEE Loss
- OEE Status

### Overall OEE Result

**Average OEE = 76.86%**

The majority of machines fall into the **Moderate OEE** category.

This indicates that there is meaningful room for operational improvement, particularly through reducing downtime and improving machine performance.

---

#  6. Availability & Downtime

Availability was identified as an important loss driver among the critical bottleneck machines.

This suggests that reducing downtime can potentially release additional effective production capacity without purchasing new machinery.

Potential operational actions include:

- Reducing unplanned downtime
- Improving preventive maintenance
- Reducing planned downtime where operationally feasible
- Improving machine changeover practices
- Improving maintenance scheduling
- Investigating recurring machine stoppages

---

#  7. Cost & Contribution Analysis

Production economics were evaluated using contribution per unit and contribution generated relative to machine time.

The model calculates:

**Contribution per Unit**

= Selling Price − Variable Cost

and:

**Contribution per Machine Hour**

= Contribution per Unit ÷ Machine Hours per Unit

This helps identify components that generate relatively high economic value for the machine time they consume.

---

# Top Components by Contribution per Machine Hour

| Rank | Component | Contribution / Machine Hour | Criticality | Assigned Machine |
|---:|---|---:|---|---|
| 1 | C027 | ₹50,015.71 | Critical | M010 |
| 2 | C004 | ₹28,138.52 | High | M008 |
| 3 | C102 | ₹27,731.09 | Medium | M007 |
| 4 | C176 | ₹18,615.09 | High | M007 |
| 5 | C235 | ₹18,382.89 | Medium | M025 |
| 6 | C155 | ₹17,569.77 | Low | M010 |
| 7 | C141 | ₹17,260.23 | Low | M008 |
| 8 | C215 | ₹16,675.42 | Critical | M010 |
| 9 | C005 | ₹16,230.27 | Medium | M009 |
| 10 | C089 | ₹15,248.94 | Low | M013 |

---

#  8. Production Priority

Production priority was determined using two dimensions:

1. **Economic Priority**
2. **Component Criticality**

Economic priority was based on contribution generated per machine hour.

Criticality was then incorporated to prevent economically attractive but operationally less important components from automatically receiving the highest priority.

### Priority Logic

| Economic Priority | Criticality | Final Priority |
|---|---|---|
| High | Critical | Critical Priority |
| High | High / Medium / Low | High Priority |
| Medium | Critical | Critical Priority |
| Medium | High | High Priority |
| Medium | Medium / Low | Medium Priority |
| Low | Critical | Critical Priority |
| Low | High | High Priority |
| Low | Medium | Medium Priority |
| Low | Low | Low Priority |

Buy components are classified as:

**Not Applicable**

because they are not manufactured internally.

---

#  9. Capacity Scenario Analysis

Four scenarios were tested to determine whether capacity shortages could be reduced through operational improvements.

---

## Scenario 1 — Increase Scheduled Hours by 500 Hours

Scheduled machine hours were increased by 500 hours per machine.

### Result

- Available capacity increased significantly.
- Overall utilization decreased to approximately **89.36%**.
- Capacity shortages were reduced from **13 machines to 0**.

### Interpretation

Increasing scheduled operating hours is highly effective in resolving the modeled capacity shortage.

However, this solution may require additional shifts, overtime, or increased operating time.

---

## Scenario 2 — Reduce Planned Downtime by 10%

Planned downtime was reduced by 10%.

### Result

- Overall utilization decreased to approximately **99.21%**.
- Machines in capacity shortage decreased from **13 to 8**.

### Interpretation

Reducing planned downtime improves effective machine availability and partially resolves capacity constraints.

---

## Scenario 3 — Reduce Unplanned Downtime by 20%

Unplanned downtime was reduced by 20%.

### Result

- Overall utilization decreased to approximately **98.82%**.
- Machines in capacity shortage decreased from **13 to 6**.

### Interpretation

Reducing unplanned downtime provides a meaningful increase in usable production capacity.

This highlights the importance of preventive maintenance and downtime reduction.

---

## Scenario 4 — Improve Production Efficiency by 5%

Required machine hours were reduced by 5% to simulate an improvement in production efficiency.

### Result

- Required machine hours decreased to approximately **99,411.75 hours**.
- Overall utilization decreased to approximately **95.30%**.
- Capacity shortages were reduced from **13 machines to 0**.

### Interpretation

A relatively small improvement in production efficiency can eliminate the modeled capacity shortage without increasing machine capacity.

This makes operational efficiency improvement one of the most attractive interventions in the model.

---

#  Scenario Comparison

| Scenario | Overall Utilization | Machines in Shortage |
|---|---:|---:|
| Base Case | 100.07% | 13 |
| +500 Scheduled Hours | 89.36% | 0 |
| -10% Planned Downtime | 99.21% | 8 |
| -20% Unplanned Downtime | 98.82% | 6 |
| +5% Efficiency | 95.30% | 0 |

---

#  Management Recommendations

Based on the analysis, the following actions are recommended.

## 1. Prioritize the Critical Bottleneck Machines

Immediate attention should be given to:

- **M020**
- **M002**
- **M006**
- **M019**
- **M004**

These machines have the highest capacity utilization and largest modeled capacity shortages.

---

## 2. Focus on Availability Improvement

Availability and downtime are important contributors to the capacity constraints.

Management should investigate:

- Unplanned machine failures
- Preventive maintenance effectiveness
- Planned maintenance scheduling
- Changeover duration
- Repeated downtime causes

Reducing downtime can create additional effective production hours without purchasing additional equipment.

---

## 3. Improve Production Efficiency

The scenario analysis indicates that a **5% efficiency improvement eliminates the modeled machine shortages**.

Potential improvements include:

- Standardized operating procedures
- Cycle-time reduction
- Operator training
- Setup optimization
- Changeover reduction
- Process improvement
- Preventive maintenance

---

## 4. Evaluate Additional Scheduled Hours

Adding **500 scheduled hours per machine** eliminates modeled capacity shortages and reduces utilization to approximately 89.36%.

This could be considered through:

- Additional shifts
- Overtime
- Extended operating schedules

However, the additional labour and operating cost should be evaluated before implementation.

---

## 5. Protect High-Value Production

Components generating high contribution per machine hour should receive careful production planning attention.

For example:

- **C027** generates approximately ₹50,015.71 contribution per machine hour.
- **C004** generates approximately ₹28,138.52 contribution per machine hour.
- **C102** generates approximately ₹27,731.09 contribution per machine hour.

Critical components such as **C027** and **C215** should also receive elevated priority because of their operational importance.

---

## 6. Consider Capacity Balancing Before Capital Investment

The analysis shows that total capacity is only slightly below total requirements.

However, individual machines experience significant shortages while some machines retain spare capacity.

Therefore, management should first investigate:

- Production reallocation
- Alternate machine capability
- Scheduling changes
- Load balancing
- Changeover optimization
- Downtime reduction

before immediately investing in additional machinery.

---

# Workbook Structure

The Excel workbook contains the following analytical sections:

| Sheet | Purpose |
|---|---|
| `01_README` | Project overview and instructions |
| `02_data_dictionary` | Definitions of variables and fields |
| `03_raw_components` | Component master data |
| `04_raw_machines` | Machine master data |
| `05_raw_supplier` | Supplier reference data |
| `06_raw_machine_oee` | Machine OEE input data |
| `07_raw_labour` | Labour-related data |
| `08_demand_planning` | Demand and forecast analysis |
| `09_inventory_production_reqmnt` | Inventory and production requirements |
| `10_machine_capacity` | Machine capacity and utilization |
| `11_oee_analysis` | OEE analysis |
| `12_bottleneck_analysis` | Bottleneck identification |
| `13_cost_contribution` | Contribution and production economics |
| `14_capacity_scenarios` | Capacity scenario modelling |
| `15_management_dashboard` | Executive dashboard |
| `16_Project_Conclusion` | Findings and recommendations |

---

# Management Dashboard

The project includes an executive management dashboard summarizing the major operational findings.

### Key Dashboard KPIs

- Total Components
- Make Components
- Buy Components
- Number of Machines
- Machines in Capacity Shortage
- Average OEE

### Dashboard Visualizations

The dashboard includes:

- Machines in Capacity Shortage by Scenario
- Bottleneck Machines
- Production Priority Analysis
- Economic Contribution Analysis

The dashboard is designed as a presentation layer for management rather than as a separate calculation engine.

---

#  Tools & Skills Demonstrated

## Microsoft Excel

- Excel Tables
- Structured References
- `SUMIFS`
- `SUMPRODUCT`
- `COUNTIFS`
- `COUNTIF`
- `AVERAGE`
- `MAX`
- `MIN`
- `IF`
- `IFERROR`
- Pivot-style analysis
- Conditional formatting
- Scenario modelling
- Dashboard design

## Analytical Skills

- Demand forecasting
- Inventory planning
- Production requirement calculation
- Capacity planning
- Machine utilization analysis
- OEE analysis
- Bottleneck identification
- Cost and contribution analysis
- Production prioritization
- Scenario analysis
- Management decision support

---

#  Assumptions & Limitations

This project uses simulated manufacturing data created for analytical and portfolio purposes.

Important assumptions include:

- Component demand is simulated.
- Machine assignments are predetermined.
- Machine capacity is evaluated using available production hours.
- Production requirements are based on forecast demand and inventory considerations.
- Capacity calculations focus on internally manufactured components.
- Buy components are not included in internal machine-hour calculations.
- Scenario analysis represents simplified operational changes rather than detailed implementation plans.
- Labour availability, overtime cost, machine qualification constraints and detailed production sequencing are not fully modelled.
- Alternate-machine routing is not explicitly optimized.
- The model does not represent a live manufacturing execution system.

Therefore, the results should be interpreted as **decision-support outputs from a simulated manufacturing environment**, rather than as actual company operating results.

---

#  Future Improvements

The project could be extended by incorporating:

- Machine-to-machine production routing optimization
- Linear programming / optimization
- Detailed production scheduling
- Shift-level planning
- Labour capacity constraints
- Overtime cost modelling
- Setup and changeover optimization
- Preventive maintenance optimization
- Multi-period capacity planning
- Inventory holding cost
- Service-level constraints
- Supplier lead-time modelling
- Make-or-buy optimization
- Sensitivity analysis
- Python-based optimization
- Power BI reporting

---

#  Key Insights

The major insights from the model are:

### 1. Capacity is slightly insufficient overall

Required machine hours of approximately **104,382.33 hours** exceed available capacity of approximately **104,309.28 hours**.

This results in overall utilization of approximately **100.07%**.

---

### 2. The problem is concentrated rather than uniform

There are **13 machines showing capacity shortages**, with the largest constraints concentrated around:

**M020, M002, M006, M019 and M004.**

This means that machine-level capacity balancing is more important than simply looking at total plant capacity.

---

### 3. OEE indicates improvement potential

Average OEE is approximately **76.86%**, indicating moderate overall equipment effectiveness and room for operational improvement.

---

### 4. Downtime reduction can release capacity

Reducing planned and unplanned downtime reduces the number of machines experiencing capacity shortages.

This suggests that operational improvements can partially address capacity constraints without immediate capital investment.

---

### 5. Efficiency improvement can eliminate shortages

The +5% efficiency scenario reduces required machine hours sufficiently to eliminate the modeled capacity shortages.

This demonstrates the potential value of productivity improvement initiatives.

---

### 6. Economic contribution can support production prioritization

Contribution per machine hour provides a useful economic perspective for deciding which internally manufactured components should receive higher production priority when capacity is constrained.

For example, **C027** has the highest contribution per machine hour in the analysis at approximately **₹50,015.71 per machine hour**.

---

#  Final Conclusion

The analysis indicates that A Auto Components Pvt. Ltd. is operating very close to its total manufacturing capacity, with required machine hours slightly exceeding available capacity.

However, the primary concern is not simply the total amount of capacity available. The more important issue is the concentration of production requirements across specific machines.

The critical bottlenecks identified are:

**M020, M002, M006, M019 and M004.**

At the same time, average OEE of approximately **76.86%** indicates that operational improvements may provide meaningful additional capacity.

Scenario analysis shows that both:

- a **5% improvement in production efficiency**, and
- an increase of **500 scheduled hours per machine**

can eliminate the modeled capacity shortages.

Therefore, the recommended strategy is to first focus on **bottleneck management, downtime reduction, production efficiency and capacity balancing**, before considering major capital investment.

The combination of operational capacity analysis and economic contribution analysis also provides management with a framework for deciding **where limited production capacity should be allocated to maximize operational and economic value**.

---

#  Project Takeaway

> **The key lesson from the analysis is that capacity shortage does not always mean that a company immediately needs more machines. Improving machine availability, production efficiency and capacity allocation can potentially unlock significant usable capacity from the existing manufacturing system.**

---

##  Project Type

**Portfolio Project — Manufacturing Analytics / Operations Management / Production Planning**

### Built With

**Microsoft Excel**

### Domain

**Manufacturing | Automotive Components | Operations Analytics | Capacity Planning | Production Optimization**
