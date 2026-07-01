# MASTER CONTENT — Centro Médico del Bajío · Unit II Project Execution

> Working content document. Everything below feeds the Report PDF, Project Plan PDF, Gantt chart, and Presentation PPTX.

---

## 0. Fixed / corrected Activity Table (10 activities)

**Fixes applied:**
- C4 renamed: it is NOT a software purchase. It combines cloud-hosting provider evaluation (via weighted criteria table) + digitalization equipment acquisition. This procurement effort is what generates the 6 evidence documents.
- Kept 10 activities (rubric allows 7–10).

| ID | Activity | Pred. | Dur. | Responsible |
|----|----------|-------|------|-------------|
| C1 | Define cloud hosting environment and storage requirements | — | 3 d | PM, Cloud Specialist |
| C2 | Analyze medical records and document types from the 3 branches | C1 | 4 d | PM, Medical Staff |
| C3 | Design cloud database and storage architecture | C2 | 4 d | Cloud Specialist |
| C4 | Evaluate cloud hosting providers (criteria table) and acquire digitalization equipment | C3 | 5 d | PM, Procurement |
| C5 | Install and configure equipment in the 3 branches | C4 | 3 d | Implementation Team |
| C6 | Digitize patient clinical records | C5 | 5 d | Digitization Team |
| C7 | Digitize clinical analyses and complementary documents | C6 | 5 d | Digitization Team |
| C8 | Migrate and upload digitized records to the cloud platform | C7 | 4 d | Cloud Specialist, IT |
| C9 | Analyze and remove duplicate records | C8 | 3 d | IT Team |
| C10 | Integration and validation testing | C9 | 2 d | PM, IT Team |

- **Critical Path:** C1→C2→C3→C4→C5→C6→C7→C8→C9→C10 (fully sequential)
- **Baseline duration:** 38 business days (8-week window = 40 business days → 2 days slack)

---

## 1. Budget allocation (BAC = $147,900 MXN)

| ID | Activity | Budget (MXN) |
|----|----------|-------------:|
| C1 | Define cloud environment | 8,000 |
| C2 | Analyze records | 10,000 |
| C3 | Design architecture | 12,000 |
| C4 | Provider selection + equipment | 55,000 |
| C5 | Install equipment | 12,000 |
| C6 | Digitize patient records | 15,000 |
| C7 | Digitize analyses | 15,000 |
| C8 | Migrate to cloud | 10,000 |
| C9 | Remove duplicates | 6,900 |
| C10 | Testing | 4,000 |
| | **TOTAL (BAC)** | **147,900** |

---

## 2. Week 4 Review Meeting — the 5 events (June 26, 2026)

| # | Event | Interpretation | Impact |
|---|-------|----------------|--------|
| 1 | Person in charge of initial activity (C1) got sick, returned after 2 days | C1 took 5 d instead of 3 d | +2 d slip on the whole critical path (schedule) |
| 2 | 3 deliverables not yet released | Purchase Order, Invoice, Installation Report pending (C4/C5 delayed) | 3 pending deliverables logged |
| 3 | Software start-up brought forward 1 week (management) | Go-live deadline compressed by 5 business days | Requires crashing / fast-tracking |
| 4 | Longest critical activity needs +3 days | C6 (Digitize patient records, highest volume) 5 d → 8 d | +3 d slip (schedule) |
| 5 | Materials & equipment cost +4% (inflation) | Equipment-heavy lines (C4) +4% | +~$2,200–2,680 cost (budget) |

---

## 3. Earned Value Analysis @ Week 4 (day 20 = June 26)

**Planned position at day 20:** C1–C5 complete + C6 first day → PV = $100,000
**Actual position at day 20 (after +2 d sick delay):** C1–C4 complete, C5 at 2/3 → EV = $93,000
**Actual cost (C1 overrun + C4 +4% inflation):** AC = $97,200

| Metric | Formula (corrected PMBOK) | Value |
|--------|---------------------------|------:|
| PV (BCWS) | Planned value at day 20 | $100,000 |
| EV (BCWP) | Earned value at day 20 | $93,000 |
| AC (ACWP) | Actual cost at day 20 | $97,200 |
| **SV** | **EV − PV** (BCWP − BCWS) | **−$7,000** → behind schedule |
| **CV** | **EV − AC** (BCWP − ACWP) | **−$4,200** → over budget |
| SPI | EV / PV | 0.93 |
| CPI | EV / AC | 0.957 |
| EAC | BAC / CPI | ≈ $154,545 |

**⚠️ FORMULA CORRECTION (whiteboard had them swapped):**
- Whiteboard wrote: "Schedule variance = BCWP − ACWP" ❌ (that is actually Cost Variance)
- Whiteboard wrote: "Cost variance = BCWP − BCWS" ❌ (that is actually Schedule Variance)
- **Correct:** SV = BCWP − BCWS = EV − PV · CV = BCWP − ACWP = EV − AC

**Interpretation:** SPI 0.93 and CPI 0.957 → the project is both slightly behind schedule (sick-leave delay) and slightly over budget (equipment inflation). Corrective action (crashing the critical path + contingency reserve) is required, especially given management's request to move go-live one week earlier.

---

## 4. Schedule reconciliation (net effect)

| Item | Days |
|------|-----:|
| Baseline finish | day 38 |
| + Event 1 (C1 sick) | +2 → 40 |
| + Event 4 (C6 extension) | +3 → 43 |
| Management target (Event 3: 1 week earlier) | target moves to day 33 |
| **Recovery needed via crashing/fast-tracking** | **−10 days to hit target** |

**Response (Change Control):** approved crashing on C6/C7 (add a 2nd digitization crew) and fast-tracking C8/C9 partial overlap, funded from contingency reserve.

---

## 5. Supplier selection — Weighted Criteria Table (Activity C4)

| Criterion | Weight | Prov. 1 | Prov. 2 | Prov. 3 |
|-----------|:------:|:-------:|:-------:|:-------:|
| Cost | 40% | 10 | 5 | 7 |
| Delivery Time | 30% | 5 | 10 | 5 |
| Quality | 20% | 8 | 7 | 10 |
| Post-Service | 10% | 7 | 5 | 0 |
| **Weighted Total** | **100%** | **7.8** ✅ | 6.9 | 6.3 |

Calc check: Prov.1 = 10(.4)+5(.3)+8(.2)+7(.1) = 4.0+1.5+1.6+0.7 = **7.8** → **Provider 1 selected** (best cost + post-service).

---

## 6. Change Requests log (Week 4)

| CR ID | Description | Type | Impact | Status |
|-------|-------------|------|--------|--------|
| CR-01 | Extend C6 duration 5→8 d (data volume) | Schedule | +3 d | Approved |
| CR-02 | Bring software go-live forward 1 week | Scope/Schedule | −5 d target | Approved |
| CR-03 | Budget increase for +4% equipment inflation | Cost | +$2,680 | Approved (contingency) |
| CR-04 | Add 2nd digitization crew to crash C6/C7 | Resource | recover delay | Approved |

---

## 7. Deliverables per activity (evidence documents)

| # | Document | Generated by |
|---|----------|--------------|
| 1 | Technical Report (Informe Técnico) | C1–C3 |
| 2 | 3 Quotations (cotizaciones) | C4 |
| 3 | Criteria Table (Tabla de Criterios) | C4 |
| 4 | Purchase Order (Pedido) | C4 |
| 5 | Invoice (Factura) | C4 |
| 6 | Installation Report (Reporte de instalación) | C5 |

---

## 8. Review meetings list

| Meeting | Date | Purpose |
|---------|------|---------|
| Kick-off | Jun 1, 2026 | Charter approval, team alignment |
| Week 4 Review | Jun 26, 2026 | Milestone review, change requests, EVA |
| Closure | Jul 31, 2026 | Go-live sign-off, lessons learned |

---

## 9. Project Charter — full 13 sections (7.8.2.1 – 7.8.2.13)

### 7.8.2.1 Identification Section
- **Project Name:** Medical Information System — Centralized Cloud Migration
- **Project Sponsor:** Dr. Alejandro Vance de la Vega, CEO & Chairman of the Board
- **Date:** June 1, 2026
- **Revision:** 1.0
- **Project Manager:** José Manuel Ortiz Medrano

### 7.8.2.2 Overview of the Project
Implementation of a centralized cloud-based medical information system and data migration for the three hospital branches of Centro Médico del Bajío (Aguascalientes, León, Morelia), consolidating all clinical documentation into a single virtualized platform.

### 7.8.2.3 Objective
To implement a centralized medical information system across the 3 hospital branches between June 1 and July 31, 2026, consolidating data onto a cloud platform, reducing active patient-record redundancy to 0%, achieving query response under 2.0 s, within the approved budget of $147,900 MXN.

### 7.8.2.4 Scope (In-Scope)
- Configure and deploy 1 centralized cloud database environment (4 VMs, 32 GB RAM) serving the 3 branches.
- Design and run automated deduplication scripts to reach 0% redundancy on active patient records.
- Migrate the full annual volume of 53,208 clinical analyses and 34,818 consultations to the cloud.
- Acquire and install digitalization equipment across the 3 branches.
- Complete all cloud provisioning, data cleaning and integration within $147,900 MXN.

### 7.8.2.5 Major Milestones (with dates)
- M1 — Cloud environment & requirements defined: Jun 3, 2026
- M2 — Cloud architecture designed & provider selected: Jun 22, 2026
- M3 — Equipment installed in the 3 branches: Jun 25, 2026
- M4 — Digitization completed: Jul 9, 2026
- M5 — Migration & deduplication completed: Jul 18, 2026
- M6 — System validated & Go-Live: Jul 31, 2026

### 7.8.2.6 Major Deliverables (quantified)
- 1 centralized cloud database (4 VMs, 32 GB RAM) serving 3 branches
- 53,208 clinical analyses + 34,818 consultations migrated
- 0% duplicate active patient records (from 53,208 duplicated records eliminated)
- Digitalization equipment installed at 3 branches
- 6 evidence documents (technical report, 3 quotations, criteria table, purchase order, invoice, installation report)

### 7.8.2.7 Assumptions
- The 3 branches share the same clinical document taxonomy.
- Cloud hosting is procured as a service; no physical servers are purchased.
- Digitization staff are available Monday–Friday during the 8-week window.
- Branch access for equipment installation is granted on the agreed schedule.
- Historical data provided by the branches is complete and available for migration.

### 7.8.2.8 Constraints
- Hard deadline: Go-Live no later than July 31, 2026.
- Fixed budget of $147,900 MXN; scope changes require CCB approval.
- Total project activities must remain between 7 and 10.
- No physical servers — solution must run on cloud infrastructure.

### 7.8.2.9 Business Need or Opportunity (Benefits)
Centro Médico del Bajío operates decentralized local servers per branch, causing duplicated clinical records, inconsistent patient histories, saturation, low performance and high maintenance/security costs. Centralizing on the cloud eliminates redundancy, improves data integrity and availability, reduces operating costs and supports the organization's digital transformation.

### 7.8.2.10 Preliminary Cost for the Project
The procurement team obtains cost proposals from 3 cloud-hosting providers during Week 1, evaluated with a weighted criteria table. Equipment and migration costs are consolidated by the PM. Total approved budget: $147,900 MXN, subject to a +4% adjustment on materials/equipment due to inflation (contingency reserve).

### 7.8.2.11 Project Risks
- Migration failure or data loss during cloud transfer.
- Vendor/equipment delivery delays.
- User resistance to the new centralized system.
- Connectivity failure between branches during cutover.
- Cybersecurity incident affecting sensitive patient data.

### 7.8.2.12 Project Charter Acceptance
| Name & Title | Signature | Date |
|--------------|-----------|------|
| José Manuel Ortiz Medrano, Project Manager | __________ | ______ |
| Dr. Alejandro Vance de la Vega, CEO & Sponsor | __________ | ______ |
| Centro Médico del Bajío Representative | __________ | ______ |

### 7.8.2.13 Project Stakeholders
| Function | Name | Role |
|----------|------|------|
| Project Manager | José Manuel Ortiz Medrano | Leads the project |
| Sponsor | Dr. Alejandro Vance de la Vega | Approves budget & scope |
| Cloud Specialist | (assigned) | Designs cloud architecture |
| Procurement | (assigned) | Manages purchasing |
| IT Team | (assigned) | Migration & deduplication |
| Medical Staff | (assigned) | Provides records & validation |
| Cloud Provider | Provider 1 (selected) | Hosting service |
| End Beneficiary | Centro Médico del Bajío | Patients & clinical staff |

---

## 10. Project Closure Report

**Hits (3–5 done right):**
1. Successful deployment of the centralized cloud infrastructure (4 VMs, 32 GB RAM).
2. 100% elimination of the 53,208 duplicated records.
3. Query response time achieved under 2.0 s across the 3 branches.
4. Weighted criteria table gave an objective, defensible provider selection (Provider 1).
5. Change control absorbed the Week-4 disruptions without missing Go-Live.

**Failures (3–5 wrong):**
1. Initial activity (C1) delayed 2 days by staff sick leave — no backup assigned.
2. 3 procurement deliverables were late at the Week-4 review.
3. C6 underestimated — patient-record volume required +3 days.
4. EVA formulas were initially recorded incorrectly (SV/CV swapped) at review.

**Improvements (3–5 for next time):**
1. Assign a backup owner for every critical-path activity.
2. Estimate digitization with a per-record parametric model, not a flat 5 days.
3. Pre-qualify vendors and lock delivery-time SLAs in Week 1.
4. Standardize EVA templates so SV/CV formulas cannot be swapped.
5. Keep the short stand-up alignment meetings introduced during the rework.

**Goals (objective achievement):**
The strategic objective — consolidating the 3 branches onto a centralized cloud platform with 0% record redundancy, sub-2s response, within budget by July 31, 2026 — was achieved at 100% compliance despite the Week-4 disruptions.

---

## 11. Minutas (Spanish) — for appendices

### Minuta 1 — Reunión de Arranque (1 de junio de 2026)
- Se aprobó el Project Charter y se alineó al equipo.
- Se confirmó presupuesto de $147,900 MXN y fecha de Go-Live 31 de julio.
- Acuerdos: iniciar C1 (definición de entorno cloud).

### Minuta 2 — Reunión de Revisión Semana 4 (26 de junio de 2026)
- El responsable de la actividad inicial (C1) se enfermó y regresó tras 2 días → retraso de 2 días.
- 3 entregables pendientes de liberar (pedido, factura, reporte de instalación).
- Gerencia solicitó adelantar el arranque del software 1 semana.
- La actividad crítica más larga (C6) requiere 3 días adicionales.
- Costo de materiales y equipo aumentó 4% por inflación.
- Se aprobaron 4 solicitudes de cambio (CR-01 a CR-04) y uso de reserva de contingencia.
- EVA: SPI 0.93, CPI 0.957 → proyecto ligeramente atrasado y sobre presupuesto; se aplica crashing.

### Minuta 3 — Reunión de Cierre (31 de julio de 2026)
- Go-Live ejecutado; sistema validado (respuesta < 2 s, 0% duplicados).
- Firmas de aceptación del sponsor y representante del cliente.
- Lecciones aprendidas documentadas.
