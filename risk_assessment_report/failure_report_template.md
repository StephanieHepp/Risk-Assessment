# Failure Report

**CIP Engineer:** Marcus Chen

**Date:** 2025-10-02

**Incident ID:** INC-2025-0923-012

**Asset:** Pump #P-0177

**Chamber:** Chamber #CVD115 (AMAT - Centura - Chamber B)

**Analysis Method:** 8D / DMAIC

---

## Executive Summary

**Failure Mode**: Shaft broken due to excessive load on main bearing

**Impact**: Unplanned downtime of 8.5 hours, production loss of 45 wafers

**Root Cause**: Load on main bearing (MB) exceeded design limits due to combination of process byproduct accumulation and bearing wear

**Status**: Root cause investigation complete, corrective measures in implementation phase

---

## Incident Overview

| Parameter | Value |
|-----------|-------|
| **Failure Detected** | 2025-09-23 15:42 |
| **Detection Method** | Pump alarm + abnormal vibration |
| **Failure Type** | Mechanical failure - shaft fracture |
| **Risk Score** | 92% (Critical) |
| **Health Index** | 3.2 (Critical condition) |
| **RUL at Failure** | -120 hours (negative indicates overdue) |
| **Current Runtime** | 22,847 h (114% of target) |
| **Last Maintenance** | 2025-06-15 (15 weeks ago) |
| **MTBF** | 18,000 h (industry average for this model) |
| **Status** | Failure analysis complete, implementing corrective actions |

---

## Asset Information

| Parameter | Details |
|-----------|---------|
| **Tool ID** | CVD-115-P1 |
| **Pump S/N** | AP7856432 |
| **Pump Type** | HiPace 700 M |
| **Location/Area** | Fab 1, Bay 4-6, CVD Line |
| **Tool** | Applied Materials Centura |
| **Process** | PECVD Silicon Oxide |
| **ADP Frequency** | 50Hz |
| **Roots Frequency** | 50Hz |
| **N2 Flow** | 45 slm |
| **ADP Temperature** | 95°C |
| **Roots Temp Status** | Hot Root enabled |

---

## Operating Mode

- [x] Run to fail
- [ ] Preventive maintenance

**Next Maintenance Planned**: Not scheduled (run to fail mode)

**Operating Hours Since Last Service**: 3,847 hours

---

## Failure Timeline

| Time | Event | Action Taken |
|------|-------|--------------|
| 15:42 | Pump alarm triggered - high vibration detected | Automated alarm notification sent |
| 15:45 | Process chamber automatically shut down | Tool safety protocol activated |
| 15:50 | Technician arrived on site | Visual inspection initiated |
| 16:10 | Confirmed pump seized, shaft rotation blocked | Emergency pump removal authorized |
| 16:30 | Spare pump retrieval initiated | Logistics coordinated |
| 18:45 | New pump installed (S/N AP8012456) | Installation completed |
| 20:15 | System verification and process qualification | Tool released to production |
| 24:12 | Failed pump disassembly and analysis begun | Root cause investigation started |

**Total Downtime**: 8.5 hours

**Production Impact**: 45 wafers scrapped, $67,500 estimated loss

---

## Pump Condition / Observations

- [x] Abnormal noise
- [ ] Oil / fluid leaks
- [ ] No vacuum
- [x] Overheating
- [ ] Sudden shutdown
- [ ] No response to command
- [x] Vibrations
- [x] Other: Shaft rotation severely restricted

---

## Current Pump Condition

- [x] Broken down
- [ ] Under diagnosis
- [ ] Repaired
- [ ] Other

---

## Telemetry Data Analysis

### Key Performance Indicators Before Failure

| Metric | Value 7 Days Before | Value 24h Before | At Failure | Normal Range | Deviation |
|--------|---------------------|------------------|------------|--------------|-----------|
| **Health Index** | 1.8 | 2.9 | 3.2 | < 1.0 | +220% |
| **Vibration RMS** | 2.1 mm/s | 4.8 mm/s | 6.7 mm/s | < 2.5 mm/s | +168% |
| **Power Consumption** | 1850 W | 2140 W | 2450 W | 1800 W | +36% |
| **Bearing Temperature** | 68°C | 89°C | 112°C | < 75°C | +49% |
| **RUL** | 350 h | 45 h | -120 h | > 1000 h | Critical |

### Contributing Factors

- Progressive increase in vibration levels over 3-week period
- Elevated bearing temperatures indicating friction increase
- Power consumption trending upward suggesting mechanical resistance
- Health index degradation accelerating in final 48 hours

---

## Visual Inspection Findings

### Disassembly Observations

**Shaft Condition:**
- Complete fracture at main bearing location
- Fracture surface shows fatigue crack propagation
- Evidence of stress concentration at bearing seat

**Bearing Condition:**
- Severe wear on outer race
- Ball bearing discoloration indicating overheating
- Excessive radial play measured (0.8mm vs 0.15mm specification)

**Internal Contamination:**
- Significant process byproduct deposits in rotor assembly
- Deposits particularly heavy near exhaust stages
- Material analysis indicates silicon oxide particulates

---

## Pictures

*[Placeholder for failure images to be inserted]*

- Broken shaft components
- Worn bearing assembly
- Internal contamination deposits
- Fracture surface closeup

---

## Root Cause Analysis - 5 Whys

### Technical Analysis

**Why did the pump fail?**
→ Shaft fractured at main bearing location

**Why did the shaft fracture?**
→ Excessive cyclical stress loads on shaft

**Why were there excessive loads?**
→ Main bearing seized due to wear and contamination

**Why did the bearing seize?**
→ Bearing degraded from extended operation beyond service life with process contamination

**Why was it operated beyond service life?**
→ Run-to-fail operating mode with no preventive maintenance schedule

### Systemic Analysis

**Why is run-to-fail mode used?**
→ No established preventive maintenance program for this tool

**Why is there no PM program?**
→ Historical reliability assumed adequate; cost optimization priority

**Why was degradation not detected earlier?**
→ Telemetry monitoring in place but no proactive intervention protocol

**Why was no intervention taken despite telemetry alerts?**
→ Alerts noted but not escalated; no clear escalation threshold defined

**Root Cause**: Inadequate maintenance strategy combined with unclear escalation protocols for telemetry degradation indicators

---

## Ishikawa Diagram Analysis

### Materials
- Process byproduct accumulation (silicon oxide)
- Bearing material wear under extended duty cycle

### Method
- Run-to-fail maintenance approach
- Insufficient intervention thresholds for telemetry alerts

### Machine
- Pump exceeded target lifetime by 14%
- Bearing wear accelerated by contamination

### Environment
- PECVD process generates particulate byproducts
- Inadequate purge gas flow to prevent contamination

### Measurement
- Telemetry monitoring active but response protocol unclear
- No defined critical threshold for immediate action

### Manpower
- Unclear ownership of telemetry alert response
- Insufficient training on early intervention protocols

---

## Failure Mode Analysis

### Primary Failure Mode: Mechanical Fatigue

**Failure Mechanism**: High-cycle fatigue leading to shaft fracture

**Contributing Factors**:
1. Bearing wear creating uneven load distribution (40% contribution)
2. Extended operation beyond target lifetime (30% contribution)
3. Process contamination increasing friction (20% contribution)
4. Inadequate preventive maintenance (10% contribution)

### Secondary Observations

- Bearing outer race wear significantly exceeded inner race wear (indicates external load factors)
- Contamination deposits concentrated at high-temperature zones
- No evidence of lubrication degradation or oil contamination

---

## Validation of Potential Causes

| # | Probable Cause | Validation Method | Result | Pilot | Validation Date | Major Cause (Y/N) |
|---|----------------|-------------------|--------|-------|-----------------|-------------------|
| 1 | Bearing wear exceeding limits | Physical inspection + measurement | Confirmed: 0.8mm play vs 0.15mm spec | N/A | 2025-09-24 | Y |
| 2 | Process contamination buildup | Material analysis of deposits | Confirmed: Silicon oxide particulates | N/A | 2025-09-25 | Y |
| 3 | Overloading due to process upset | Process log review | Not confirmed: No process deviations | N/A | 2025-09-24 | N |
| 4 | Lubrication failure | Oil analysis | Not confirmed: Lubrication adequate | N/A | 2025-09-24 | N |
| 5 | Material defect in shaft | Metallurgical analysis | Not confirmed: Material per specification | N/A | 2025-09-26 | N |
| 6 | Extended operation beyond service life | Runtime data review | Confirmed: 114% of target lifetime | N/A | 2025-09-23 | Y |
| 7 | Inadequate purge gas flow | Process parameter review | Confirmed: Below recommended 60 slm | N/A | 2025-09-25 | Y |

---

## Containment Actions (D3)

### Immediate Actions Taken

1. **Emergency Pump Replacement**
   - Failed pump removed and replaced with spare unit
   - Completed: 2025-09-23 20:15
   - Status: Tool returned to production

2. **Fleet-Wide Assessment**
   - All similar pumps on PECVD tools inspected for health index > 2.0
   - 3 additional pumps identified for proactive replacement
   - Status: In progress

3. **Enhanced Monitoring**
   - Health index alert threshold lowered from 2.5 to 1.8
   - Daily review of at-risk assets implemented
   - Status: Active

---

## Corrective Actions (D5)

### Short-Term Actions (0-30 Days)

1. **Implement Preventive Maintenance Schedule**
   - Establish 18,000 hour service interval for this pump model
   - Owner: Maintenance Team Lead
   - Target Date: 2025-10-15
   - Status: In development

2. **Increase N2 Purge Flow**
   - Adjust purge gas from 45 slm to 60 slm per manufacturer recommendation
   - Owner: Process Engineering
   - Target Date: 2025-10-10
   - Status: Process change request submitted

3. **Define Telemetry Response Protocol**
   - Create escalation matrix for health index thresholds
   - Health Index > 1.5: Weekly review
   - Health Index > 2.0: Immediate engineering assessment
   - Health Index > 2.5: Mandatory pump exchange within 48 hours
   - Owner: CIP Engineering Team
   - Target Date: 2025-10-20
   - Status: Draft in review

### Long-Term Actions (30-90 Days)

4. **Transition to Condition-Based Maintenance**
   - Implement predictive maintenance program for all critical pumps
   - Integrate RUL calculations into maintenance planning
   - Owner: Reliability Engineering
   - Target Date: 2025-12-31
   - Status: Project initiated

5. **Enhance Process Contamination Control**
   - Evaluate additional filtration or abatement options
   - Consider periodic in-situ cleaning procedures
   - Owner: Process Engineering
   - Target Date: 2025-12-15
   - Status: Feasibility study phase

---

## Implementation Plan (D6)

| Action Item | Owner | Target Date | Resources Required | Success Criteria | Status |
|-------------|-------|-------------|-------------------|------------------|--------|
| PM Schedule Implementation | Maint. Team | 2025-10-15 | CMMS update, scheduling tool | All pumps scheduled | In Progress |
| N2 Flow Increase | Process Eng | 2025-10-10 | Process qualification | Flow at 60 slm verified | Pending |
| Telemetry Protocol | CIP Team | 2025-10-20 | Training materials | Protocol documented + trained | In Progress |
| Predictive Maintenance | Reliability | 2025-12-31 | Software integration | System live + validated | Initiated |
| Contamination Control | Process Eng | 2025-12-15 | Capital budget approval | Solution identified | Planning |

---

## Preventive Measures (D7)

### Process Changes

1. **Purge Gas Flow Optimization**
   - Increase from 45 slm to 60 slm across all PECVD tools
   - Reduces contamination ingress by estimated 35%

2. **Service Interval Establishment**
   - 18,000 hour mandatory service interval
   - Prevents operation beyond bearing design life

### Monitoring Enhancements

3. **Enhanced Telemetry Response**
   - Proactive intervention at Health Index 2.0
   - Prevents progression to critical failure modes

4. **Weekly Fleet Health Review**
   - Dedicated review of all at-risk assets (HI > 1.5)
   - Early identification of degradation trends

### Documentation

5. **Updated Operating Procedures**
   - Clear escalation paths for telemetry alerts
   - Defined roles and responsibilities for response

6. **Lessons Learned Distribution**
   - Share findings with all sites using similar equipment
   - Update training materials for technicians and engineers

---

## Standardization (D8)

### Knowledge Transfer

1. **Cross-Functional Review Meeting**
   - Present findings to maintenance, process, and engineering teams
   - Scheduled: 2025-10-12

2. **Best Practices Documentation**
   - Update maintenance standards for vacuum pump fleet
   - Include in onboarding materials for new engineers

3. **Similar Equipment Assessment**
   - Review all pumps in run-to-fail mode
   - Prioritize transition to condition-based maintenance

### Continuous Improvement

4. **KPI Monitoring**
   - Track MTBF improvement post-implementation
   - Monitor unplanned downtime reduction
   - Target: 50% reduction in pump-related failures within 6 months

5. **Quarterly Review**
   - Assess effectiveness of corrective actions
   - Adjust protocols based on field performance data

---

## Key Performance Impact

| KPI | Before Failure | After Implementation | Target | Expected Improvement |
|-----|----------------|---------------------|--------|---------------------|
| Pump MTBF | 18,000 h | 24,000 h | 25,000 h | +33% |
| Unplanned Downtime | 45 h/year | 18 h/year | 15 h/year | -60% |
| Health Index Response Time | None | < 24 h | < 12 h | New metric |
| Preventive Maintenance Coverage | 0% | 100% | 100% | New program |
| Cost per Failure Event | $67,500 | $8,500 | < $10,000 | -87% |

---

## Lessons Learned

### Technical Lessons

1. **Extended Operation Risks**: Operating equipment beyond target lifetime without enhanced monitoring significantly increases failure risk
2. **Contamination Impact**: Process byproduct accumulation accelerates wear even in sealed systems
3. **Bearing Wear Patterns**: Asymmetric bearing wear indicates external loading factors requiring investigation

### Operational Lessons

4. **Telemetry Value**: Early indicators were present but not acted upon; clear escalation protocols essential
5. **Run-to-Fail Limitations**: Run-to-fail may be cost-effective for non-critical assets but inappropriate for production-critical equipment
6. **Proactive Intervention**: Small investments in preventive measures avoid large failure costs

---

## Cost Analysis

### Failure Costs

| Cost Category | Amount |
|---------------|--------|
| Production Loss (45 wafers) | $67,500 |
| Replacement Pump | $18,000 |
| Emergency Labor (overtime) | $3,200 |
| Investigation & Analysis | $2,800 |
| **Total Failure Cost** | **$91,500** |

### Preventive Program Costs (Annual)

| Cost Category | Amount |
|---------------|--------|
| Scheduled Maintenance (4 pumps) | $28,000 |
| Enhanced Telemetry Monitoring | $5,000 |
| Process Modifications | $12,000 |
| Training & Documentation | $3,000 |
| **Total Annual Prevention Cost** | **$48,000** |

**ROI Calculation**: Break-even after 1 prevented failure event per 2 years

---

## Additional Comments

The failure analysis clearly demonstrates the value of transitioning from reactive to proactive maintenance strategies. While the immediate failure was caused by mechanical factors (bearing wear and shaft fracture), the systemic root cause was inadequate maintenance planning and unclear response protocols for available telemetry data.

The corrective actions address both the technical failure modes and the organizational factors that allowed the failure to progress. Implementation of these measures is expected to significantly improve equipment reliability and reduce unplanned downtime across the vacuum pump fleet.

---

## Approvals

| Role | Name | Signature | Date |
|------|------|-----------|------|
| **CIP Engineer** | Marcus Chen | | |
| **Maintenance Manager** | | | |
| **Process Engineering** | | | |
| **Quality Manager** | | | |
| **Site Manager** | | | |

---

**Report Generated**: 2025-10-02 14:30 UTC  
**Report Status**: Final - Approved for Implementation  
**Next Review Date**: 2025-11-15  
**Document Control**: Version 1.0 | Classification: Internal Use | FAR-P-0177-001
