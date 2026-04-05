# ANTS Autopilot v2 — Product Roadmap & Improvement Plan

## สังเคราะห์จาก Customer Feedback 400,000 Users

**Document Version:** 2.0
**Date:** 6 April 2569 (2026)
**Authored by:** 40 Chief Product Officers & Product Owners
**Data Source:** 120+ issues from 400,000 user feedback sessions
**Target:** All module satisfaction scores from current <3.0 to 4.5+

---

## Table of Contents

1. [Executive Summary — 7 Key Findings](#1-executive-summary--7-key-findings)
2. [Top 10 Critical Issues](#2-top-10-critical-issues-ปัญหาวิกฤตกระทบมากที่สุด)
3. [Module Satisfaction Heatmap & Target Scores](#3-module-satisfaction-heatmap--target-scores)
4. [Issue Resolution Plan — Sprint Allocation](#4-issue-resolution-plan--sprint-allocation)
5. [Top 20 Recommendations Ranked by Impact](#5-top-20-recommendations-ranked-by-impact)
6. [Quick Wins — Implement in < 2 Days](#6-quick-wins--implement-in--2-days-each)
7. [Engineering Task Assignment](#7-engineering-task-assignment)

---

## 1. Executive Summary — 7 Key Findings

จากการวิเคราะห์ feedback ของผู้ใช้ 400,000 คน พบ 7 ปัญหาหลักที่ต้องแก้ไขเร่งด่วน:

### Finding 1: Thai Business Workflow Gap (71.9% / 287,600 users)

ระบบไม่มี workflows สำหรับธุรกิจไทยที่จำเป็น:
- **สำรองจ่ายล่วงหน้า (Advance Payment):** 198,400 users (49.6%) ไม่มีระบบ — CROSS-030
- **e-Tax Invoice ตามมาตรฐานกรมสรรพากร:** 187,200 users (46.8%) — CROSS-031
- **PromptPay QR Code integration:** 176,800 users (44.2%) — EX-010
- **Per diem อัตโนมัติตามอัตราราชการ:** 154,200 users (38.6%) — EX-011
- **e-Slip จากธนาคาร (SCB, KBANK, BBL):** 148,600 users (37.2%) — EX-012
- **Withholding tax คำนวณอัตโนมัติ:** 134,200 users (33.6%) — SD-011

**Impact:** ทำให้ผู้ใช้ต้องทำงานนอกระบบ 60%+ ของ workflow ทางการเงินไทย เสียเวลาเฉลี่ย 2.3 ชม./วัน

### Finding 2: Navigation & UX Complexity (71.4% / 284,700 users)

- **Navigation ลึกเกิน 4.7 คลิก** (benchmark: 2.3 คลิก) — CROSS-001: 284,700 users
- **ไม่มี global search:** 245,600 users (61.4%) — CROSS-002
- **ไม่มี breadcrumb navigation:** 189,100 users (47.3%) — CROSS-011
- **ไม่มี Undo/Redo:** 172,300 users (43.1%) — CROSS-007
- **ไม่มี recently visited items:** 167,800 users (42.0%) — CROSS-008

**Impact:** Task completion rate ต่ำกว่า benchmark 34%, user drop-off rate 23% ต่อ session

### Finding 3: Integration Desert (66.8% / 256,700 users)

ไม่เชื่อมต่อระบบที่ธุรกิจไทยใช้ประจำ:
- **Connector setup ซับซ้อนเกินไป:** 256,700 users (64.2%) — CN-001
- **ไม่มี LINE Official Account integration:** 213,400 users (53.4%) — SY-004
- **ไม่เชื่อมต่อ Express/PEAK/Prosoft accounting:** 198,400 users (49.6%) — FD-011
- **ไม่มี pre-built connectors สำหรับระบบไทย:** 189,100 users (47.3%) — CN-002
- **ไม่เชื่อมต่อ Kerry/Flash/J&T/Thailand Post:** 142,600 users (35.7%) — LG-010

**Impact:** Connectors module ได้คะแนนต่ำสุด 2.19/5 — ต้องยกเครื่องทั้งหมด

### Finding 4: Thai Localization Failure (58.7% / 234,800 users)

- **Help documentation ภาษาอังกฤษเท่านั้น:** 245,600 users (61.4%) — CROSS-003
- **ป้ายกำกับ Thai/English ปะปน:** 219,300 users (54.8%) — CROSS-004
- **ไม่มี พ.ศ. date toggle:** 189,100 users (47.3%) — CROSS-006
- **Error messages ภาษาอังกฤษเท่านั้น:** 167,800 users (42.0%) — CROSS-009
- **Thai font kerning/rendering issues:** 145,600 users (36.4%) — CROSS-014
- **Thai sorting order ผิด:** 87,600 users (21.9%) — CROSS-022

**Impact:** ผู้ใช้ที่อ่านภาษาอังกฤษไม่คล่อง (ประมาณ 45%) ใช้งานระบบได้ไม่เต็มประสิทธิภาพ

### Finding 5: Change Resistance (78.0% / 312,000 users)

- **ไม่มี data migration tool จากระบบเดิม:** 267,800 users (67.0%) — CROSS-034
- **ไม่มี training mode / sandbox:** 234,000 users (58.5%) — CROSS-033
- **ไม่มี contextual help / guided tours:** 198,400 users (49.6%) — CROSS-042
- **ไม่มี role-based dashboard:** 184,700 users (46.2%) — CROSS-039

**Impact:** 78% ของ users ที่ต้อง migrate จากระบบเก่า (Express, SAP, Excel) ต่อต้านการเปลี่ยนแปลง เพราะไม่มีเครื่องมือช่วย transition

### Finding 6: Mobile Unusable (44.6% / 178,400 users)

- **Charts อ่านไม่ได้บนหน้าจอ < 768px:** 156,700 users (39.2%) — CROSS-010
- **Tables overflow บนมือถือ:** 163,400 users (40.9%) — CROSS-012
- **กราฟ Dashboard อ่านยากบนมือถือ:** 74,300 users (18.6%) — HD-003
- **Dropdown menus ถูกตัดบนมือถือ:** 87,600 users (21.9%) — CROSS-021
- **Pinch-to-zoom ถูกปิดในบางโมดูล:** 67,800 users (17.0%) — CROSS-024
- **ไม่รองรับ barcode/QR scanning บนมือถือ:** 134,200 users (33.6%) — CROSS-047

**Impact:** Field staff, sales reps, และ managers ที่ต้องอนุมัติงานนอกสถานที่ทำงานผ่านมือถือไม่ได้

### Finding 7: Data Security & Trust (33.6% / 167,800 users)

- **ไม่รองรับ 2FA / SSO:** 167,800 users (42.0%) — CROSS-037
- **ไม่มี audit trail ที่ export ได้:** 145,200 users (36.3%) — CROSS-038
- **ไม่มี audit log สำหรับ admin:** 87,600 users (21.9%) — SY-005
- **ไม่มี data backup/restore self-service:** 134,200 users (33.6%) — SY-008
- **ไม่มี automated user deprovisioning:** 87,400 users (21.9%) — AD-003

**Impact:** องค์กรขนาดกลาง-ใหญ่ปฏิเสธการใช้งานเพราะไม่ผ่าน security audit ภายใน ส่งผลให้สูญเสีย enterprise deals

---

## 2. Top 10 Critical Issues (ปัญหาวิกฤตกระทบมากที่สุด)

### Issue #1: CROSS-001 — Navigation ลึกเกิน 4+ คลิก

| Field | Detail |
|-------|--------|
| **Affected Users** | 284,700 (71.2%) |
| **Severity** | Critical |
| **Module** | Cross-Module |
| **Status** | Open |

**Root Cause Analysis:**
- Information architecture ออกแบบเป็น hierarchical tree ลึก 4-5 ชั้น
- ไม่มี shortcut paths หรือ quick actions สำหรับ frequent tasks
- Sidebar navigation ไม่มี favorites/pinned items
- ไม่มี breadcrumbs ทำให้ user หลงทาง

**Proposed Solution:**
1. Flatten navigation architecture เหลือ max 2 clicks สำหรับ 80% ของ tasks
2. เพิ่ม command palette (Ctrl+K) สำหรับ quick jump ไปทุกหน้า
3. เพิ่ม breadcrumb navigation ทุกหน้า
4. เพิ่ม "Recently Visited" section ใน sidebar
5. เพิ่ม Quick Actions bar บน Home Dashboard

**Effort Estimate:** Large (3-4 sprints)
**Expected Score Improvement:** +0.8 across all modules

---

### Issue #2: CN-001 — Connector setup ซับซ้อนเกินไป

| Field | Detail |
|-------|--------|
| **Affected Users** | 256,700 (64.2%) |
| **Severity** | Critical |
| **Module** | Connectors |
| **Status** | Open |

**Root Cause Analysis:**
- Setup wizard ไม่มี step-by-step guidance
- ต้องกรอก technical parameters (API keys, endpoints) แบบ manual
- ไม่มี pre-configured templates สำหรับระบบที่นิยม
- Error messages เป็น technical jargon ที่ non-technical users ไม่เข้าใจ

**Proposed Solution:**
1. สร้าง guided setup wizard แบบ 3-step (เลือก provider > authorize > test)
2. เพิ่ม pre-built connector templates สำหรับ 15+ Thai systems
3. เปลี่ยน error messages เป็น human-readable Thai
4. เพิ่ม connection health dashboard แบบ real-time
5. เพิ่ม video tutorial สำหรับแต่ละ connector

**Effort Estimate:** Extra Large (4-5 sprints)
**Expected Score Improvement:** Connectors 2.19 -> 3.5 (+1.31)

---

### Issue #3: EX-001 — OCR อ่านใบเสร็จภาษาไทยผิดพลาดสูง (~67% accuracy)

| Field | Detail |
|-------|--------|
| **Affected Users** | 245,600 (61.4%) |
| **Severity** | Critical |
| **Module** | Expense & Receipt |
| **Status** | In Progress |

**Root Cause Analysis:**
- OCR engine ไม่ได้ train กับ Thai receipt formats (ใบกำกับภาษี, ใบเสร็จรับเงิน)
- ไม่รองรับ font หลากหลายที่พบในใบเสร็จไทย (รวมถึง handwritten Thai)
- Template matching ไม่ครอบคลุม format ใบเสร็จไทย (7-Eleven, Lotus, Big C)
- Thai number/currency parsing ผิดพลาดบ่อย (฿ symbol, comma vs dot)

**Proposed Solution:**
1. Retrain OCR model ด้วย 50,000+ Thai receipt samples
2. เพิ่ม Thai receipt template library (ร้านค้า, ห้าง, ออนไลน์)
3. Implement post-OCR validation rules สำหรับ เลขประจำตัวผู้เสียภาษี, VAT calculation
4. เพิ่ม manual correction UI ที่ highlight ส่วนที่ OCR ไม่มั่นใจ
5. Target: accuracy >92%

**Effort Estimate:** Extra Large (5-6 sprints)
**Expected Score Improvement:** Expense & Receipt 2.70 -> 3.8 (+1.10)

---

### Issue #4: CROSS-002 — ไม่มี global search ข้ามโมดูล

| Field | Detail |
|-------|--------|
| **Affected Users** | 245,600 (61.4%) |
| **Severity** | Critical |
| **Module** | Cross-Module |
| **Status** | Open |

**Root Cause Analysis:**
- ไม่มี search index ที่รวมข้อมูลจากทุกโมดูล
- แต่ละโมดูล search เฉพาะภายในตัวเอง
- ไม่รองรับ Thai word segmentation สำหรับ full-text search
- ไม่มี search suggestions หรือ autocomplete

**Proposed Solution:**
1. Build unified search index ด้วย Elasticsearch + Thai tokenizer (ICU)
2. เพิ่ม Ctrl+K command palette สำหรับ global search
3. Implement search suggestions + autocomplete ภาษาไทย
4. เพิ่ม search filters (module, date range, type)
5. เพิ่ม recent searches + saved searches

**Effort Estimate:** Large (3-4 sprints)
**Expected Score Improvement:** +0.5 across all modules

---

### Issue #5: PR-001 — สร้าง PR ต้องกรอกข้อมูลหลายหน้า ไม่มี draft save

| Field | Detail |
|-------|--------|
| **Affected Users** | 213,400 (53.4%) |
| **Severity** | Critical |
| **Module** | Procurement |
| **Status** | In Progress |

**Root Cause Analysis:**
- Form แบ่งเป็น 5+ หน้า ไม่มี single-page view option
- ไม่มี auto-save / draft functionality — data หายเมื่อ browser crash
- ไม่มี template สำหรับ PR ที่สร้างบ่อย
- Validation errors แสดงทีละหน้า ไม่ summary

**Proposed Solution:**
1. Implement auto-save ทุก 30 วินาที + draft status
2. สร้าง PR templates สำหรับ common purchases (office supplies, IT equipment, etc.)
3. เพิ่ม single-page mode option สำหรับ experienced users
4. แสดง validation summary ก่อน submit
5. เพิ่ม "duplicate from previous PR" function

**Effort Estimate:** Medium (2 sprints)
**Expected Score Improvement:** Procurement 2.69 -> 3.3 (+0.61)

---

### Issue #6: SY-004 — ไม่รองรับ LINE Official Account integration

| Field | Detail |
|-------|--------|
| **Affected Users** | 213,400 (53.4%) |
| **Severity** | Critical |
| **Module** | System |
| **Status** | Open |

**Root Cause Analysis:**
- LINE เป็นช่องทาง communication หลักของธุรกิจไทย (95% penetration)
- ระบบส่ง notification ผ่าน email เท่านั้น ซึ่ง open rate ต่ำมาก (<15%)
- ไม่มี LINE Messaging API integration
- Approval workflows ต้องเข้าระบบเท่านั้น ทำไม่ได้ผ่าน LINE

**Proposed Solution:**
1. Integrate LINE Messaging API สำหรับ notifications
2. Build LINE LIFF app สำหรับ quick approvals
3. เพิ่ม LINE login as authentication option
4. สร้าง LINE bot สำหรับ status queries
5. เพิ่ม LINE notification preferences ใน user settings

**Effort Estimate:** Large (3 sprints)
**Expected Score Improvement:** System 2.54 -> 3.2 (+0.66)

---

### Issue #7: CROSS-034 — ไม่มี data migration tool จากระบบเดิม

| Field | Detail |
|-------|--------|
| **Affected Users** | 267,800 (67.0%) |
| **Severity** | Critical |
| **Module** | Cross-Module |
| **Status** | Open |

**Root Cause Analysis:**
- ผู้ใช้ส่วนใหญ่ migrate จาก Express Accounting, SAP B1, หรือ Excel
- ไม่มี import wizard สำหรับ mapping fields
- ไม่มี data validation ก่อน import
- ไม่มี rollback mechanism หาก import ผิดพลาด

**Proposed Solution:**
1. สร้าง Migration Toolkit รองรับ Express (.dbf), SAP (.csv), Excel (.xlsx)
2. Guided field mapping wizard + auto-detect columns
3. Data validation + preview ก่อน import
4. Batch import with progress tracking
5. Rollback capability สำหรับ 30 วัน

**Effort Estimate:** Extra Large (5 sprints)
**Expected Score Improvement:** +0.7 adoption rate improvement

---

### Issue #8: CN-002 — ไม่มี pre-built connectors สำหรับระบบไทย

| Field | Detail |
|-------|--------|
| **Affected Users** | 189,100 (47.3%) |
| **Severity** | Critical |
| **Module** | Connectors |
| **Status** | Open |

**Root Cause Analysis:**
- Connector marketplace มีเฉพาะ international services
- ไม่มี Express Accounting, PEAK, Prosoft, FlowAccount connectors
- ไม่มี Thai banking API connectors (SCB, KBANK, BBL, KTB)
- ไม่มี Thai logistics provider connectors

**Proposed Solution:**
1. Build 10 pre-built Thai connectors: Express, PEAK, Prosoft, FlowAccount, SCB, KBANK, BBL, Kerry, Flash, Thailand Post
2. สร้าง connector SDK สำหรับ partner development
3. เพิ่ม connector marketplace with ratings
4. One-click install + auto-configuration
5. Community-contributed connector support

**Effort Estimate:** Extra Large (5-6 sprints)
**Expected Score Improvement:** Connectors 2.19 -> 3.8 (+1.61)

---

### Issue #9: VM-001 — เปรียบเทียบ Vendor ใช้เวลาโหลดนาน 8-12 วินาที

| Field | Detail |
|-------|--------|
| **Affected Users** | 189,100 (47.3%) |
| **Severity** | Critical |
| **Module** | Vendor Management |
| **Status** | In Progress |

**Root Cause Analysis:**
- Query ดึงข้อมูล vendor ทั้งหมดแบบ unoptimized (no pagination, no indexing)
- Frontend render ข้อมูลทั้งหมดพร้อมกันโดยไม่มี virtual scrolling
- ไม่มี caching layer สำหรับ vendor comparison data
- Image/document attachments load synchronously

**Proposed Solution:**
1. Implement server-side pagination + database indexing
2. เพิ่ม virtual scrolling สำหรับ large lists
3. Implement Redis caching สำหรับ vendor comparison
4. Lazy load images + documents
5. Target: response time < 1.5 วินาที

**Effort Estimate:** Medium (2 sprints)
**Expected Score Improvement:** Vendor Management 2.65 -> 3.2 (+0.55)

---

### Issue #10: SY-001 — Permission system ซับซ้อนเกินไป ไม่มี role template

| Field | Detail |
|-------|--------|
| **Affected Users** | 189,100 (47.3%) |
| **Severity** | Critical |
| **Module** | System |
| **Status** | Open |

**Root Cause Analysis:**
- Permission ต้อง config ทีละ user ทีละ module
- ไม่มี role-based templates (Admin, Manager, Staff, Viewer)
- ไม่มี organization hierarchy support
- ไม่สามารถ bulk assign permissions

**Proposed Solution:**
1. สร้าง 8 pre-built role templates ตามธุรกิจไทย
2. เพิ่ม role hierarchy + inheritance
3. Bulk user-role assignment via CSV
4. Permission audit view (who can access what)
5. Department-based auto-permission assignment

**Effort Estimate:** Medium (2-3 sprints)
**Expected Score Improvement:** System 2.54 -> 3.4 (+0.86)

---

## 3. Module Satisfaction Heatmap & Target Scores

### Overview Table

| # | Module | Current Score | Target Score | Gap | Priority | Sprint Focus |
|---|--------|:------------:|:------------:|:---:|:--------:|:------------|
| 1 | **Connectors** | 2.19 | 4.5 | **2.31** | P0 - HIGHEST | Sprint 1-4 |
| 2 | **System** | 2.54 | 4.5 | **1.96** | P0 | Sprint 1-3 |
| 3 | **Vendor Management** | 2.65 | 4.5 | **1.85** | P1 | Sprint 2-4 |
| 4 | **Finance Doc Hub** | 2.68 | 4.5 | **1.82** | P1 | Sprint 2-5 |
| 5 | **Logistics FX** | 2.68 | 4.5 | **1.82** | P1 | Sprint 3-5 |
| 6 | **Procurement** | 2.69 | 4.5 | **1.81** | P1 | Sprint 1-3 |
| 7 | **Expense & Receipt** | 2.70 | 4.5 | **1.80** | P1 | Sprint 1-4 |
| 8 | **Customer Feedback** | 2.78 | 4.5 | **1.72** | P2 | Sprint 4-6 |
| 9 | **Home Dashboard** | 2.86 | 4.5 | **1.64** | P2 | Sprint 1-2 |
| 10 | **Sales Doc Gen** | 2.93 | 4.5 | **1.57** | P2 | Sprint 3-5 |

---

### Module 1: Connectors (2.19 -> 4.5)

| # | Feature | Description | Impact | Sprint |
|---|---------|-------------|:------:|:------:|
| 1 | Guided Setup Wizard | step-by-step wizard แทน form ยาว | +0.45 | S2 |
| 2 | Pre-built Thai Connectors | Express, PEAK, Prosoft, FlowAccount connectors สำเร็จรูป | +0.50 | S4 |
| 3 | Human-readable Errors | เปลี่ยน API error เป็นข้อความภาษาไทยเข้าใจง่าย | +0.25 | S1 |
| 4 | Connection Health Dashboard | real-time monitoring สถานะ connectors ทั้งหมด | +0.30 | S3 |
| 5 | Thai Banking API Pack | SCB, KBANK, BBL, KTB API connectors | +0.35 | S4 |
| 6 | One-click Connector Install | ติดตั้ง connector ด้วย 1 คลิก + auto-config | +0.20 | S3 |
| 7 | Connector Testing Sandbox | ทดสอบ connector ก่อน deploy จริง | +0.15 | S3 |
| 8 | WeChat Integration | สำหรับลูกค้าจีน | +0.05 | S6 |
| 9 | API Rate Limiting Dashboard | แสดง usage + limits สำหรับ admin | +0.05 | S5 |
| 10 | Connector SDK | ให้ partners สร้าง custom connectors | +0.01 | S6 |

### Module 2: System (2.54 -> 4.5)

| # | Feature | Description | Impact | Sprint |
|---|---------|-------------|:------:|:------:|
| 1 | Role-based Permission Templates | 8 role templates สำเร็จรูป (Admin, Manager, Staff, Viewer, etc.) | +0.40 | S2 |
| 2 | LINE Official Account Integration | แจ้งเตือน + approve ผ่าน LINE | +0.35 | S3 |
| 3 | 2FA / SSO (Azure AD, Google) | เพิ่มความปลอดภัย login | +0.30 | S3 |
| 4 | Settings Page Search | search function ในหน้า Settings | +0.15 | S1 |
| 5 | Bulk User Onboarding (CSV) | import users จาก CSV พร้อม role assignment | +0.20 | S2 |
| 6 | Audit Log for Admin Actions | บันทึก admin actions ทั้งหมดพร้อม export | +0.20 | S3 |
| 7 | Billing Page Improvements | แสดงรายละเอียดค่าใช้จ่ายเข้าใจง่าย | +0.15 | S1 |
| 8 | User Activity Monitoring | dashboard แสดง user login/usage patterns | +0.10 | S4 |
| 9 | Auto User Deprovisioning | ปิด account อัตโนมัติเมื่อพนักงานลาออก | +0.05 | S5 |
| 10 | System Health Page | สถานะระบบ + uptime สำหรับ users | +0.06 | S4 |

### Module 3: Vendor Management (2.65 -> 4.5)

| # | Feature | Description | Impact | Sprint |
|---|---------|-------------|:------:|:------:|
| 1 | Performance Optimization | ลดเวลาโหลดจาก 8-12s เหลือ <1.5s | +0.50 | S2 |
| 2 | Auto Vendor Scoring | ให้คะแนน vendor อัตโนมัติจากประวัติการสั่งซื้อ | +0.30 | S3 |
| 3 | TIS-620 File Support | รองรับ Quotation Analysis ไฟล์ภาษาไทย | +0.25 | S2 |
| 4 | Contract Expiry Notifications | แจ้งเตือนอัตโนมัติก่อนสัญญาหมด | +0.20 | S3 |
| 5 | Task-Timeline Integration | เชื่อมโยง tasks กับ timeline โปรเจค | +0.15 | S4 |
| 6 | Vendor Risk Assessment | module ประเมินความเสี่ยง vendor | +0.15 | S5 |
| 7 | Audit Report Date Filter | filter ช่วงเวลาได้เอง | +0.10 | S1 |
| 8 | Performance Trend Charts | กราฟแสดง vendor performance ย้อนหลัง | +0.10 | S4 |
| 9 | Vendor Portal (Self-service) | portal สำหรับ supplier อัพเดทข้อมูลเอง | +0.05 | S5 |
| 10 | AI Vendor Recommendation | แนะนำ vendor จาก AI ตามประวัติ | +0.05 | S6 |

### Module 4: Finance Doc Hub (2.68 -> 4.5)

| # | Feature | Description | Impact | Sprint |
|---|---------|-------------|:------:|:------:|
| 1 | Document Grouping | จัดกลุ่มเอกสารตามประเภท (invoice, receipt, tax) | +0.35 | S2 |
| 2 | Express/PEAK/Prosoft Integration | เชื่อมต่อระบบบัญชีไทยโดยตรง | +0.40 | S4 |
| 3 | Verification Checklist Templates | template สำหรับ verification workflow | +0.25 | S2 |
| 4 | PDF Annotation & Markup | annotate + comment บน PDF ได้ | +0.20 | S3 |
| 5 | Thai Keyword Search Improvement | ปรับปรุง search ภาษาไทยให้แม่นยำ | +0.15 | S2 |
| 6 | Real-time Dashboard Update | อัพเดท dashboard real-time (ไม่ใช่ batch 1 ชม.) | +0.12 | S3 |
| 7 | Monthly Closing Workflow | workflow ปิดบัญชีรายเดือนอัตโนมัติ | +0.15 | S4 |
| 8 | Document Version Control | revision history สำหรับทุกเอกสาร | +0.10 | S4 |
| 9 | Digital Stamp/Seal | ตราประทับดิจิทัลสำหรับเอกสารราชการ | +0.05 | S5 |
| 10 | e-Tax Invoice Compliance | รองรับ e-Tax Invoice ตามกรมสรรพากร | +0.05 | S4 |

### Module 5: Logistics FX (2.68 -> 4.5)

| # | Feature | Description | Impact | Sprint |
|---|---------|-------------|:------:|:------:|
| 1 | Thai Document OCR | Freight OCR รองรับเอกสารขนส่งไทย | +0.40 | S3 |
| 2 | Thai Provider API Integration | เชื่อมต่อ Kerry/Flash/J&T/Thailand Post | +0.35 | S4 |
| 3 | Thai Rate Cards | อัตราค่าขนส่งแบบไทย (ตาม zone, น้ำหนัก) | +0.25 | S3 |
| 4 | Real-time Shipment Tracking | ติดตามพัสดุ real-time | +0.25 | S4 |
| 5 | Thai Province Names (ภาษาไทย) | แสดงชื่อจังหวัดเป็นภาษาไทย ไม่ใช่ romanized | +0.10 | S1 |
| 6 | Cost-per-unit Analysis | วิเคราะห์ต้นทุนต่อหน่วย | +0.15 | S4 |
| 7 | Warehouse Management Module | จัดการคลังสินค้าเบื้องต้น | +0.15 | S5 |
| 8 | Customs Declaration Form | รองรับใบขนสินค้า | +0.10 | S5 |
| 9 | Cost Calculator Thai Rates | คำนวณค่าขนส่งตามอัตราไทย | +0.05 | S3 |
| 10 | Multi-modal Shipping | รองรับขนส่งหลายรูปแบบ (รถ, เรือ, เครื่องบิน) | +0.02 | S6 |

### Module 6: Procurement (2.69 -> 4.5)

| # | Feature | Description | Impact | Sprint |
|---|---------|-------------|:------:|:------:|
| 1 | PR Draft Auto-save | auto-save ทุก 30 วินาที + draft status | +0.35 | S1 |
| 2 | PR-to-PO Conversion | สร้าง PO จาก PR ได้โดยตรง 1 คลิก | +0.30 | S2 |
| 3 | PR Templates | templates สำหรับ PR ที่สร้างบ่อย | +0.25 | S1 |
| 4 | Bulk PO Creation | สร้าง PO หลายรายการพร้อมกัน | +0.20 | S3 |
| 5 | 3-Way Match Simplification | ลดความซับซ้อนการแสดงผลเปรียบเทียบ | +0.20 | S2 |
| 6 | Analytics Excel/CSV Export | export analytics เป็น Excel/CSV | +0.15 | S1 |
| 7 | Approval Matrix (วงเงิน) | อนุมัติอัตโนมัติตามวงเงิน | +0.15 | S3 |
| 8 | Goods Receipt Module | GR เชื่อมกับ PO | +0.10 | S4 |
| 9 | Blanket PO / Contract PO | รองรับ PO แบบสัญญาต่อเนื่อง | +0.05 | S4 |
| 10 | Vendor Portal Integration | supplier self-service portal | +0.06 | S5 |

### Module 7: Expense & Receipt (2.70 -> 4.5)

| # | Feature | Description | Impact | Sprint |
|---|---------|-------------|:------:|:------:|
| 1 | Thai OCR Improvement | เพิ่ม accuracy จาก 67% เป็น 92%+ | +0.45 | S3 |
| 2 | Multi-file Upload | upload ใบเสร็จหลายใบพร้อมกัน | +0.25 | S1 |
| 3 | Advance Payment Form | ระบบสำรองจ่ายล่วงหน้า | +0.25 | S3 |
| 4 | PromptPay QR Integration | เบิกจ่ายผ่าน PromptPay | +0.20 | S3 |
| 5 | Flexible Approval Workflow | delegation + multi-level approval | +0.20 | S2 |
| 6 | Policy Engine | ตรวจสอบค่าใช้จ่ายอัตโนมัติตาม policy | +0.15 | S3 |
| 7 | Per Diem Calculator | อัตราเบี้ยเลี้ยงตามราชการไทย | +0.10 | S3 |
| 8 | e-Slip Integration (Banks) | รองรับ e-Slip จาก SCB, KBANK, BBL | +0.10 | S4 |
| 9 | Category Drill-down Analytics | breakdown ตามประเภทค่าใช้จ่าย | +0.05 | S2 |
| 10 | Corporate Card Reconciliation | จับคู่ค่าใช้จ่ายกับ corporate card | +0.05 | S5 |

### Module 8: Customer Feedback (2.78 -> 4.5)

| # | Feature | Description | Impact | Sprint |
|---|---------|-------------|:------:|:------:|
| 1 | Thai Sentiment Analysis | วิเคราะห์ sentiment ภาษาไทย | +0.40 | S4 |
| 2 | Conditional Survey Logic | branching logic ใน survey builder | +0.30 | S4 |
| 3 | CRM/Ticket Integration | เชื่อมต่อ CRM + ticketing system | +0.25 | S5 |
| 4 | NPS Real-time Tracking | ติดตาม NPS แบบ real-time | +0.20 | S5 |
| 5 | Feedback Routing | ส่ง feedback ไปยังทีมที่เกี่ยวข้องอัตโนมัติ | +0.20 | S4 |
| 6 | Trend Analysis | วิเคราะห์แนวโน้มข้าม period | +0.15 | S5 |
| 7 | Multi-channel Collection | เก็บ feedback จาก LINE, email, in-app | +0.10 | S5 |
| 8 | Response Templates | template สำหรับตอบ feedback | +0.05 | S4 |
| 9 | AI Categorization | จัดหมวดหมู่ feedback อัตโนมัติ | +0.05 | S6 |
| 10 | Feedback Analytics Export | export report ได้หลาย format | +0.02 | S4 |

### Module 9: Home Dashboard (2.86 -> 4.5)

| # | Feature | Description | Impact | Sprint |
|---|---------|-------------|:------:|:------:|
| 1 | Customizable Dashboard | drag-and-drop widgets ตามความต้องการ | +0.40 | S2 |
| 2 | Quick Action Buttons | ปุ่มลัดสำหรับงานที่ทำบ่อย (สร้าง PR, upload receipt) | +0.30 | S1 |
| 3 | Widget Trend Context | แสดง trend arrows + comparison กับ period ก่อน | +0.20 | S1 |
| 4 | KPI Alert Thresholds | แจ้งเตือนเมื่อ KPI ถึง threshold | +0.20 | S3 |
| 5 | Notification Categorization | แยก urgent/info/system notifications | +0.15 | S1 |
| 6 | Mobile-friendly Charts | กราฟอ่านง่ายบนมือถือ | +0.10 | S5 |
| 7 | Role-based Dashboard | แสดงเฉพาะข้อมูลที่เกี่ยวข้องกับ role | +0.10 | S3 |
| 8 | Export to PPT | export dashboard เป็น PPT สำหรับ management report | +0.08 | S5 |
| 9 | Recently Visited Items | แสดง items ที่เข้าถึงล่าสุด | +0.05 | S1 |
| 10 | Scheduled Report Distribution | สร้าง + ส่ง report อัตโนมัติ | +0.06 | S6 |

### Module 10: Sales Doc Gen (2.93 -> 4.5)

| # | Feature | Description | Impact | Sprint |
|---|---------|-------------|:------:|:------:|
| 1 | Thai Document Templates | templates ใบเสนอราคา, ใบแจ้งหนี้ ภาษาไทย | +0.35 | S3 |
| 2 | Pipeline Drag-and-Drop | เปลี่ยนสถานะ deal ด้วย drag-and-drop | +0.25 | S3 |
| 3 | Auto-generate from Pipeline | สร้างเอกสารอัตโนมัติจาก pipeline data | +0.20 | S4 |
| 4 | e-Signature Support | ลายเซ็นอิเล็กทรอนิกส์ | +0.20 | S4 |
| 5 | CRM Integration (Salesforce, HubSpot) | เชื่อมต่อ CRM | +0.15 | S5 |
| 6 | Withholding Tax Auto-calc | คำนวณภาษีหัก ณ ที่จ่ายอัตโนมัติ | +0.15 | S4 |
| 7 | Conversion Rate Analysis | analytics แสดง conversion rate | +0.10 | S4 |
| 8 | Automated Follow-up Reminders | แจ้งเตือน follow-up อัตโนมัติ | +0.08 | S5 |
| 9 | Multi-currency Quotations | ใบเสนอราคาหลายสกุลเงิน | +0.05 | S5 |
| 10 | Campaign Expense Tracking | ติดตามค่าใช้จ่าย sales campaign | +0.04 | S6 |

---

## 4. Issue Resolution Plan — Sprint Allocation

### Sprint 1 (Week 1-2): Quick Wins — 8 Items

**Theme:** ปรับปรุงทันทีที่เห็นผลเร็ว

| # | Issue ID(s) | Feature/Fix | Acceptance Criteria | Files to Modify | Dependencies |
|---|-------------|-------------|--------------------|--------------------|-------------|
| 1 | CROSS-011 | Add breadcrumb navigation to all modules | - Breadcrumb แสดงทุกหน้า<br>- Clickable ทุก level<br>- แสดง icon + label<br>- Responsive บนมือถือ | `poc-v2.html`, all `modules/*.html` | None |
| 2 | CROSS-006 | Add พ.ศ. (Buddhist Era) date toggle | - Toggle button BE/CE<br>- Persist preference<br>- ทุก date field แสดงถูกต้อง<br>- Format: dd/mm/yyyy พ.ศ. | `poc-v2.html`, all `modules/*.html` | None |
| 3 | SY-003 | Add search bar to System Settings | - Search bar ด้านบนหน้า Settings<br>- Filter settings แบบ real-time<br>- Highlight matching terms<br>- รองรับ Thai input | `poc-v2.html` | None |
| 4 | HD-005 | Notification categorization | - 3 categories: urgent/info/system<br>- Color-coded badges<br>- Filter by category<br>- Count per category | `modules/home.html`, `poc-v2.html` | None |
| 5 | PR-001, PR-005 | PR auto-save + analytics export | - Auto-save ทุก 30 วินาที<br>- Draft indicator icon<br>- Restore from draft<br>- Export to Excel/CSV | `modules/procurement-prpo.html`, `modules/procurement-analytics.html` | None |
| 6 | EX-002 | Multi-file receipt upload | - Drag-and-drop multiple files<br>- Progress bar per file<br>- Batch OCR processing<br>- Error handling per file | `modules/expense-receipt-ocr.html` | None |
| 7 | HD-004, HD-002 | Quick Actions + trend context on widgets | - 5 configurable quick action buttons<br>- Trend arrows on KPI widgets<br>- % change vs previous period<br>- Tooltip with details | `modules/home.html` | None |
| 8 | CN-003 | Human-readable API error messages | - Thai error messages<br>- Suggested actions per error type<br>- Error code reference<br>- Copy error details button | `connectors/api-dashboard.html`, `connectors/connector-hub.html` | None |

---

### Sprint 2 (Week 3-4): Critical Fixes — 15 Items

**Theme:** แก้ปัญหา Critical ที่กระทบมากที่สุด

| # | Issue ID(s) | Feature/Fix | Acceptance Criteria | Files to Modify | Dependencies |
|---|-------------|-------------|--------------------|--------------------|-------------|
| 1 | CROSS-001 | Flatten navigation (4.7 -> 2.5 clicks) | - Restructure sidebar<br>- Add favorites/pinned<br>- Max 2 clicks for top 20 tasks<br>- Measure avg click depth | `poc-v2.html` | None |
| 2 | CROSS-002 | Global search with Thai support | - Ctrl+K command palette<br>- Search across all modules<br>- Thai word segmentation<br>- Autocomplete + suggestions<br>- Recent searches | `poc-v2.html` | Thai tokenizer |
| 3 | CROSS-007 | Undo/Redo across all modules | - Ctrl+Z / Ctrl+Y<br>- 50-step undo history<br>- Visual indicator<br>- Works on all forms | `poc-v2.html`, all `modules/*.html` | None |
| 4 | CROSS-008 | Recently visited items in sidebar | - Last 10 items<br>- Icon + module label<br>- Timestamp<br>- Click to navigate | `poc-v2.html` | None |
| 5 | VM-001 | Vendor comparison performance fix | - Load time < 1.5s<br>- Virtual scrolling<br>- Pagination (20 items/page)<br>- Loading skeleton | `modules/vendor-management.html` | None |
| 6 | SY-001 | Role-based permission templates | - 8 pre-built roles<br>- Clone + customize<br>- Bulk assign<br>- Audit view | `poc-v2.html` | None |
| 7 | PR-002 | PR-to-PO direct conversion | - 1-click convert button<br>- Auto-fill PO from PR data<br>- Edit before confirm<br>- Link PR <-> PO | `modules/procurement-prpo.html` | Sprint 1 #5 |
| 8 | HD-001 | Customizable Dashboard | - Drag-and-drop widgets<br>- Add/remove widgets<br>- Save layout<br>- Reset to default | `modules/home.html` | None |
| 9 | CROSS-004 | Fix Thai/English label consistency | - Audit all labels<br>- Consistent Thai for all UI<br>- English as tooltip/secondary<br>- Style guide document | All `modules/*.html`, `poc-v2.html` | None |
| 10 | FD-001 | Document grouping by type | - Auto-categorize uploads<br>- Group view toggle<br>- Filter by type<br>- Count per category | `modules/finance-cases.html`, `modules/finance-verification.html` | None |
| 11 | FD-002 | Verification checklist templates | - 5 pre-built checklists<br>- Custom checklist builder<br>- Progress tracking<br>- Completion status | `modules/finance-verification.html` | None |
| 12 | VM-002 | TIS-620 file support for quotation | - Detect + convert encoding<br>- Display Thai correctly<br>- Parse Thai values<br>- Error handling | `modules/vendor-management.html` | None |
| 13 | EX-003 | Flexible approval workflow | - Delegation support<br>- Multi-level approval<br>- Auto-escalation rules<br>- Delegation log | `modules/expense-approval.html` | None |
| 14 | EX-005, PR-003 | Expense analytics + 3-way match fix | - Category drill-down<br>- Simplified comparison view<br>- Side-by-side layout<br>- Highlight discrepancies | `modules/expense-dashboard.html`, `modules/procurement-matching.html` | None |
| 15 | CROSS-016 | Fix dark mode inconsistency | - Audit all 4 broken modules<br>- Consistent dark theme<br>- Test all components<br>- No white flash | `modules/expense-receipt-ocr.html`, `modules/finance-verification.html`, `modules/logistics-tracking.html`, `modules/sales-pipeline.html` | None |

---

### Sprint 3 (Week 5-6): Thai Business Workflows — 12 Items

**Theme:** เพิ่ม workflows สำหรับธุรกิจไทย

| # | Issue ID(s) | Feature/Fix | Acceptance Criteria | Files to Modify | Dependencies |
|---|-------------|-------------|--------------------|--------------------|-------------|
| 1 | EX-001 | Thai OCR accuracy improvement | - Accuracy >92%<br>- Thai receipt templates<br>- Post-OCR validation<br>- Manual correction UI<br>- Confidence scores | `modules/expense-receipt-ocr.html` | OCR model retrain |
| 2 | CROSS-030 | Advance payment (สำรองจ่าย) workflow | - Request form<br>- Approval flow<br>- Settlement tracking<br>- Balance report<br>- Overdue alerts | `modules/expense-receipt-ocr.html`, `modules/expense-tasks.html` | Sprint 2 #13 |
| 3 | CROSS-031 | e-Tax Invoice compliance | - กรมสรรพากร format<br>- XML generation<br>- Digital signature<br>- Submission tracking<br>- Validation rules | `modules/finance-verification.html`, `modules/sales-dashboard.html` | None |
| 4 | EX-010 | PromptPay QR Code integration | - Generate PromptPay QR<br>- Scan to pay<br>- Payment confirmation<br>- Receipt auto-attach<br>- Transaction log | `modules/expense-receipt-ocr.html` | Banking API |
| 5 | EX-011 | Per diem calculator (อัตราราชการ) | - Thai government rates<br>- Domestic/international<br>- Auto-calculate by days<br>- Custom rate override | `modules/expense-tasks.html` | None |
| 6 | SD-001 | Thai document templates | - ใบเสนอราคา, ใบแจ้งหนี้, ใบวางบิล<br>- Thai font + layout<br>- Logo + company stamp<br>- VAT calculation built-in | `modules/sales-dashboard.html`, `modules/sales-quotation-builder.html` | None |
| 7 | LG-001 | Thai freight document OCR | - รองรับ Bill of Lading ไทย<br>- Delivery note parsing<br>- Thai logistics terms<br>- Accuracy >85% | `modules/logistics-freight-ocr.html` | OCR model |
| 8 | SD-002 | Pipeline drag-and-drop | - Drag deal between stages<br>- Status update on drop<br>- Undo support<br>- Touch support (mobile) | `modules/sales-pipeline.html` | None |
| 9 | PR-004 | Bulk PO creation | - Select multiple PRs<br>- Batch generate POs<br>- Review before confirm<br>- Progress tracking | `modules/procurement-prpo.html` | Sprint 2 #7 |
| 10 | LG-002 | Thai logistics rate cards | - Rate lookup by zone<br>- Weight-based pricing<br>- Provider comparison<br>- Rate update automation | `modules/logistics-fx-dashboard.html`, `modules/logistics-cost-calculator.html` | None |
| 11 | CROSS-009 | Thai error messages | - All error messages in Thai<br>- Context-specific guidance<br>- Error code reference<br>- Report error button | All `modules/*.html` | None |
| 12 | CROSS-022 | Fix Thai sorting order | - Correct Thai Unicode sort<br>- ก-ฮ ordering<br>- วรรณยุกต์ handling<br>- Consistent across all tables | All `modules/*.html` with data tables | None |

---

### Sprint 4 (Week 7-8): Integration & Connectors — 10 Items

**Theme:** เชื่อมต่อระบบภายนอกที่ธุรกิจไทยใช้ประจำ

| # | Issue ID(s) | Feature/Fix | Acceptance Criteria | Files to Modify | Dependencies |
|---|-------------|-------------|--------------------|--------------------|-------------|
| 1 | CN-001 | Guided connector setup wizard | - 3-step wizard UI<br>- Provider selection gallery<br>- Auto-discovery<br>- Connection test<br>- Success confirmation | `connectors/connector-hub.html` | None |
| 2 | CN-002 | Pre-built Thai system connectors | - Express connector<br>- PEAK connector<br>- Prosoft connector<br>- FlowAccount connector<br>- One-click install | `connectors/connector-hub.html` | API partnerships |
| 3 | SY-004 | LINE Official Account integration | - LINE Messaging API<br>- Notification delivery<br>- Quick reply buttons<br>- LINE login option | `poc-v2.html` | LINE API key |
| 4 | FD-011 | Express/PEAK/Prosoft accounting sync | - Bi-directional sync<br>- Field mapping<br>- Conflict resolution<br>- Sync log | `modules/finance-cases.html`, `modules/finance-verification.html` | Sprint 4 #2 |
| 5 | LG-010 | Thai logistics provider APIs | - Kerry Express API<br>- Flash Express API<br>- J&T Express API<br>- Thailand Post API<br>- Tracking integration | `modules/logistics-tracking.html` | API keys |
| 6 | CN-004 | Connection health monitoring | - Real-time status dashboard<br>- Uptime percentage<br>- Alert on disconnect<br>- Auto-reconnect | `connectors/api-dashboard.html` | None |
| 7 | CROSS-037 | 2FA / SSO implementation | - TOTP 2FA<br>- Azure AD SSO<br>- Google Workspace SSO<br>- Recovery codes<br>- Admin enforcement | `poc-v2.html` | None |
| 8 | EX-012 | e-Slip bank integration | - SCB e-Slip parser<br>- KBANK e-Slip parser<br>- BBL e-Slip parser<br>- Auto-match to expenses | `modules/expense-receipt-ocr.html` | Banking API |
| 9 | SD-012 | CRM integration (Salesforce, HubSpot) | - Contact sync<br>- Deal sync<br>- Activity log<br>- Bi-directional | `modules/sales-dashboard.html`, `modules/sales-pipeline.html` | API keys |
| 10 | CF-003 | CRM/Ticket system integration | - Create tickets from feedback<br>- Status sync<br>- Resolution tracking<br>- SLA monitoring | `modules/customer-feedback.html` | CRM connector |

---

### Sprint 5 (Week 9-10): Mobile & Accessibility — 10 Items

**Theme:** ทำให้ใช้งานบนมือถือได้จริง + accessibility

| # | Issue ID(s) | Feature/Fix | Acceptance Criteria | Files to Modify | Dependencies |
|---|-------------|-------------|--------------------|--------------------|-------------|
| 1 | CROSS-010 | Responsive charts for < 768px | - Charts scale properly<br>- Legend repositioned<br>- Touch-friendly tooltips<br>- Horizontal scroll for wide charts | All `modules/*-analytics.html`, `modules/*-dashboard.html` | None |
| 2 | CROSS-012 | Fix table overflow on mobile | - Horizontal scroll indicator<br>- Frozen first column<br>- Swipe gesture<br>- Column priority (hide less important) | All `modules/*.html` with tables | None |
| 3 | CROSS-017 | Fix keyboard accessibility (34 elements) | - Tab order correct<br>- Focus visible<br>- ARIA labels<br>- Screen reader support<br>- Skip navigation | All `modules/*.html`, `poc-v2.html` | None |
| 4 | CROSS-021 | Fix dropdown menus on mobile | - Full-width dropdowns on mobile<br>- Native select on touch<br>- No overflow cutting<br>- Scroll within dropdown | All `modules/*.html` | None |
| 5 | CROSS-024 | Enable pinch-to-zoom | - Pinch-to-zoom on all modules<br>- Remove meta viewport restrictions<br>- Maintain layout<br>- Double-tap zoom | All `modules/*.html` | None |
| 6 | CROSS-047 | Barcode/QR code scanning | - Camera access for scanning<br>- Barcode + QR code<br>- Auto-fill form fields<br>- Scan history | `modules/expense-receipt-ocr.html`, `modules/logistics-tracking.html` | Mobile camera API |
| 7 | CROSS-033 | Training mode / sandbox | - Sandbox environment toggle<br>- Sample data pre-loaded<br>- Guided tutorials (5 workflows)<br>- No real data affected | `poc-v2.html`, `modules/home.html` | None |
| 8 | CROSS-034 | Data migration toolkit | - Import wizard UI<br>- Excel/CSV upload<br>- Field mapping<br>- Validation preview<br>- Rollback button | `poc-v2.html` | None |
| 9 | CROSS-042 | Contextual help / guided tours | - Tooltip walkthrough per module<br>- Step-by-step overlays<br>- Skip option<br>- Re-trigger from help menu | All `modules/*.html` | None |
| 10 | HD-003 | Mobile dashboard improvements | - Stack widgets vertically<br>- Swipe between widgets<br>- Simplified charts<br>- Touch-friendly controls | `modules/home.html` | Sprint 5 #1 |

---

### Sprint 6 (Week 11-12): Performance & Polish — 10 Items

**Theme:** Performance optimization + remaining features

| # | Issue ID(s) | Feature/Fix | Acceptance Criteria | Files to Modify | Dependencies |
|---|-------------|-------------|--------------------|--------------------|-------------|
| 1 | CROSS-005 | Initial page load optimization | - Load time < 2.0s<br>- Code splitting<br>- Asset compression<br>- Lazy loading<br>- Service worker cache | All HTML files | None |
| 2 | CROSS-014 | Thai font kerning/rendering fix | - Consistent font rendering<br>- Proper line height for Thai<br>- No character overlap<br>- Print-friendly | CSS across all files | None |
| 3 | CROSS-003 | Thai help documentation | - All help content in Thai<br>- Searchable<br>- Screenshots<br>- Video tutorials links | `poc-v2.html` | None |
| 4 | CROSS-013 | Offline capability (PWA) | - Service worker install<br>- Cache critical pages<br>- Offline form entry<br>- Sync on reconnect | `poc-v2.html`, service worker | None |
| 5 | CROSS-032 | Multi-currency full lifecycle | - Currency selection per transaction<br>- Real-time exchange rates<br>- Conversion history<br>- Reporting in base currency | All financial `modules/*.html` | Exchange rate API |
| 6 | CF-001 | Thai sentiment analysis | - Positive/negative/neutral<br>- Thai NLP model<br>- Keyword extraction<br>- Sentiment trend chart | `modules/customer-feedback.html` | NLP model |
| 7 | CF-002 | Survey conditional logic | - If/then branching<br>- Skip logic<br>- Visual flow builder<br>- Preview mode | `modules/customer-feedback.html` | None |
| 8 | CROSS-036 | Approval delegation system | - Delegate to specific user<br>- Date range<br>- Auto-revert<br>- Delegation log<br>- Notify delegator | `poc-v2.html`, all approval `modules/*.html` | None |
| 9 | CROSS-035 | LINE/SMS notification channel | - LINE push notifications<br>- SMS fallback<br>- User preference per channel<br>- Delivery status | `poc-v2.html` | Sprint 4 #3 |
| 10 | CROSS-041 | Batch export/import across modules | - Select multiple items<br>- Export to Excel/CSV/JSON<br>- Import with validation<br>- Mapping wizard | All `modules/*.html` | None |

---

## 5. Top 20 Recommendations Ranked by Impact

### Recommendation 1: Global Search with Thai Language Support

| Field | Detail |
|-------|--------|
| **Rank** | 1 |
| **Impact Score** | 9.5/10 |
| **Related Issues** | CROSS-002, FD-005, CROSS-018 |
| **Affected Users** | 245,600+ |
| **Effort** | L |

**User Story:** "ในฐานะพนักงานบัญชี ฉันต้องการค้นหาเอกสารข้ามทุกโมดูลด้วยภาษาไทย เพื่อลดเวลาค้นหาจาก 3 นาทีเหลือ 10 วินาที"

**Technical Approach:** Build unified search index using Elasticsearch with ICU Thai tokenizer plugin. Implement Ctrl+K command palette overlay component. Index all entities (PO, PR, invoices, vendors, expenses) with Thai-aware tokenization and fuzzy matching.

**ROI Estimate:** ลดเวลาค้นหา 85% = ประหยัด 1.2 ชม./user/วัน x 245,600 users = 294,720 man-hours/day

---

### Recommendation 2: Thai OCR Accuracy to >90%

| Field | Detail |
|-------|--------|
| **Rank** | 2 |
| **Impact Score** | 9.3/10 |
| **Related Issues** | EX-001, LG-001, VM-002 |
| **Affected Users** | 245,600+ |
| **Effort** | XL |

**User Story:** "ในฐานะพนักงานเบิกค่าใช้จ่าย ฉันต้องการให้ OCR อ่านใบเสร็จภาษาไทยได้ถูกต้อง เพื่อไม่ต้องกรอกข้อมูลซ้ำด้วยมือ"

**Technical Approach:** Fine-tune existing OCR model with 50,000+ Thai receipt images. Implement receipt template matching for common Thai vendors (7-Eleven, Makro, Lotus). Add post-processing validation for TIN numbers, VAT amounts, and Thai date formats.

**ROI Estimate:** ลดเวลากรอกข้อมูลจาก 5 นาที/ใบ เหลือ 30 วินาที = ประหยัด 4.5 นาที x ~50 ใบ/เดือน/user

---

### Recommendation 3: Flatten Navigation Architecture (4.7 -> 2.5 clicks)

| Field | Detail |
|-------|--------|
| **Rank** | 3 |
| **Impact Score** | 9.2/10 |
| **Related Issues** | CROSS-001, HD-004, CROSS-008, CROSS-011 |
| **Affected Users** | 284,700 |
| **Effort** | L |

**User Story:** "ในฐานะผู้ใช้ทุกแผนก ฉันต้องการเข้าถึงงานที่ใช้บ่อยภายใน 2 คลิก เพื่อลดเวลาที่เสียไปกับ navigation"

**Technical Approach:** Restructure sidebar with top-level module grouping (max 2 levels). Add pinned/favorite items at top of sidebar. Implement breadcrumbs on all pages. Add recently visited section with last 10 items.

**ROI Estimate:** ลดจำนวนคลิกต่อ task 49% (4.7 -> 2.5) = เพิ่ม productivity 12%

---

### Recommendation 4: LINE Official Account Integration

| Field | Detail |
|-------|--------|
| **Rank** | 4 |
| **Impact Score** | 9.0/10 |
| **Related Issues** | SY-004 |
| **Affected Users** | 213,400 |
| **Effort** | L |

**User Story:** "ในฐานะผู้จัดการ ฉันต้องการรับแจ้งเตือนและอนุมัติงานผ่าน LINE เพื่อไม่ต้องเข้าระบบทุกครั้ง"

**Technical Approach:** Integrate LINE Messaging API v3 for push notifications. Build LINE LIFF mini-app for approval actions (approve/reject/comment). Implement LINE Login as alternative authentication method. Use LINE Flex Messages for rich notification cards.

**ROI Estimate:** Approval response time ลดจาก 4.2 ชม. เหลือ 15 นาที เพราะ LINE open rate 89% vs email 15%

---

### Recommendation 5: Auto-save and Undo/Redo

| Field | Detail |
|-------|--------|
| **Rank** | 5 |
| **Impact Score** | 8.8/10 |
| **Related Issues** | CROSS-007, PR-001 |
| **Affected Users** | 172,300+ |
| **Effort** | M |

**User Story:** "ในฐานะพนักงานจัดซื้อ ฉันต้องการให้ระบบ save งานอัตโนมัติ เพื่อไม่ให้ข้อมูลหายเมื่อ browser crash"

**Technical Approach:** Implement localStorage-based auto-save every 30 seconds for all form states. Build undo/redo stack (50 steps) using command pattern. Visual draft indicator with restore dialog on page load if unsaved changes detected.

**ROI Estimate:** ลด data loss incidents 95%, ลดเวลากรอกซ้ำ 100%

---

### Recommendation 6: Thai Localization Package

| Field | Detail |
|-------|--------|
| **Rank** | 6 |
| **Impact Score** | 8.7/10 |
| **Related Issues** | CROSS-004, CROSS-006, CROSS-009, CROSS-003 |
| **Affected Users** | 219,300+ |
| **Effort** | XL |

**User Story:** "ในฐานะผู้ใช้ที่ถนัดภาษาไทย ฉันต้องการใช้ระบบเป็นภาษาไทยทั้งหมด เพื่อทำงานได้เร็วขึ้นโดยไม่ต้องแปลภาษา"

**Technical Approach:** Create i18n framework with Thai as primary locale. Translate all 2,400+ UI strings. Add Buddhist Era (พ.ศ.) date toggle stored in user preferences. Localize all error messages, help text, and tooltips. Implement Thai number formatting (comma separator).

**ROI Estimate:** เพิ่ม task completion rate 28% สำหรับ users ที่ถนัดภาษาไทย (ประมาณ 180,000 users)

---

### Recommendation 7: Pre-built Thai System Connectors

| Field | Detail |
|-------|--------|
| **Rank** | 7 |
| **Impact Score** | 8.5/10 |
| **Related Issues** | CN-001, CN-002 |
| **Affected Users** | 256,700 |
| **Effort** | XL |

**User Story:** "ในฐานะ IT admin ฉันต้องการเชื่อมต่อระบบบัญชีที่ใช้อยู่ (Express/PEAK) ได้ง่าย เพื่อไม่ต้อง key ข้อมูลซ้ำ"

**Technical Approach:** Build pre-built connector packages for Express Accounting (ODBC), PEAK (REST API), Prosoft (SOAP), FlowAccount (REST). Include guided wizard with auto-detection, field mapping templates, and connection health monitoring.

**ROI Estimate:** ลดเวลา setup จาก 2-3 วัน เหลือ 30 นาที, ลด data entry ซ้ำ 70%

---

### Recommendation 8: Role-based Permission Templates

| Field | Detail |
|-------|--------|
| **Rank** | 8 |
| **Impact Score** | 8.3/10 |
| **Related Issues** | SY-001 |
| **Affected Users** | 189,100 |
| **Effort** | M |

**User Story:** "ในฐานะ IT admin ฉันต้องการ assign permissions ด้วย role template เพื่อลดเวลาจาก 30 นาที/user เหลือ 2 นาที"

**Technical Approach:** Create 8 role templates: Super Admin, Department Manager, Finance Staff, Procurement Staff, Sales Staff, Logistics Staff, Viewer, Auditor. Implement role hierarchy with inheritance. Add bulk assignment via CSV upload.

**ROI Estimate:** ลดเวลา onboarding user ใหม่ 93% (30 min -> 2 min per user)

---

### Recommendation 9: Batch/Bulk Operations

| Field | Detail |
|-------|--------|
| **Rank** | 9 |
| **Impact Score** | 8.2/10 |
| **Related Issues** | PR-004, EX-002 |
| **Affected Users** | 178,900+ |
| **Effort** | L |

**User Story:** "ในฐานะพนักงานจัดซื้อ ฉันต้องการสร้าง PO หลายรายการพร้อมกัน เพื่อประหยัดเวลาในการทำซ้ำ"

**Technical Approach:** Build batch action framework with select-all, multi-select checkboxes, and bulk action toolbar. Support batch create (PO, PR), batch upload (receipts, documents), and batch export. Add progress tracking with error handling per item.

**ROI Estimate:** ลดเวลาทำงานซ้ำ 75% สำหรับ batch operations

---

### Recommendation 10: Performance Optimization

| Field | Detail |
|-------|--------|
| **Rank** | 10 |
| **Impact Score** | 8.0/10 |
| **Related Issues** | VM-001, CROSS-005 |
| **Affected Users** | 213,400 |
| **Effort** | L |

**User Story:** "ในฐานะผู้ใช้ทุกคน ฉันต้องการให้ระบบโหลดเร็วขึ้น เพื่อไม่ต้องรอนานจนหงุดหงิด"

**Technical Approach:** Implement code splitting, lazy loading for non-critical modules, and asset compression (Brotli). Add Redis caching for frequently accessed data. Optimize database queries with proper indexing. Add loading skeletons for perceived performance.

**ROI Estimate:** ลดเวลารอ 70% (4.8s -> 1.5s), ลด bounce rate 40%

---

### Recommendation 11: PR-to-PO Direct Conversion

| Field | Detail |
|-------|--------|
| **Rank** | 11 |
| **Impact Score** | 7.8/10 |
| **Related Issues** | PR-002 |
| **Affected Users** | 145,600 |
| **Effort** | M |

**User Story:** "ในฐานะพนักงานจัดซื้อ ฉันต้องการสร้าง PO จาก PR ที่อนุมัติแล้วด้วย 1 คลิก เพื่อไม่ต้องกรอกข้อมูลซ้ำ"

**Technical Approach:** Add "Convert to PO" button on approved PR detail page. Auto-populate PO form with PR data (items, quantities, vendor, delivery date). Allow editing before final PO creation. Maintain PR-PO linkage for tracking.

**ROI Estimate:** ลดเวลาสร้าง PO จาก 15 นาที เหลือ 2 นาที

---

### Recommendation 12: Mobile-responsive All Modules

| Field | Detail |
|-------|--------|
| **Rank** | 12 |
| **Impact Score** | 7.7/10 |
| **Related Issues** | CROSS-010, CROSS-012, HD-003 |
| **Affected Users** | 163,400+ |
| **Effort** | XL |

**User Story:** "ในฐานะ sales rep ฉันต้องการดูข้อมูลและอนุมัติงานผ่านมือถือ เพื่อทำงานนอกสำนักงานได้"

**Technical Approach:** Implement responsive breakpoints (mobile-first) for all modules. Use CSS Grid + Flexbox for adaptive layouts. Convert wide tables to card view on mobile. Add touch-friendly controls (larger tap targets, swipe gestures).

**ROI Estimate:** เปิด mobile usage สำหรับ 163,400 users ที่ปัจจุบันทำงานบนมือถือไม่ได้

---

### Recommendation 13: Customizable Dashboard

| Field | Detail |
|-------|--------|
| **Rank** | 13 |
| **Impact Score** | 7.5/10 |
| **Related Issues** | HD-001, HD-002 |
| **Affected Users** | 184,700 |
| **Effort** | L |

**User Story:** "ในฐานะผู้จัดการ ฉันต้องการ customize dashboard แสดงเฉพาะ KPI ที่สำคัญ เพื่อดูภาพรวมได้ทันที"

**Technical Approach:** Build widget-based dashboard with drag-and-drop layout using React DnD or SortableJS. Widget catalog with 20+ pre-built widgets. Save layout per user in localStorage + sync to server. Add trend arrows and comparison data to all KPI widgets.

**ROI Estimate:** เพิ่ม dashboard usage จาก 34% เป็น 78% (จาก user research)

---

### Recommendation 14: Thai Sentiment Analysis

| Field | Detail |
|-------|--------|
| **Rank** | 14 |
| **Impact Score** | 7.3/10 |
| **Related Issues** | CF-001 |
| **Affected Users** | 156,700 |
| **Effort** | L |

**User Story:** "ในฐานะ Customer Success Manager ฉันต้องการวิเคราะห์ความรู้สึกลูกค้าจาก feedback ภาษาไทย เพื่อแก้ปัญหาเชิงรุก"

**Technical Approach:** Integrate Thai NLP model (PyThaiNLP or WangchanBERTa) for sentiment classification. Build sentiment dashboard with trend charts, keyword cloud, and topic clustering. Auto-tag feedback with sentiment scores and route to relevant teams.

**ROI Estimate:** ลดเวลาวิเคราะห์ feedback จาก 2 ชม./วัน เหลือ 10 นาที

---

### Recommendation 15: Flexible Approval Workflows

| Field | Detail |
|-------|--------|
| **Rank** | 15 |
| **Impact Score** | 7.2/10 |
| **Related Issues** | EX-003 |
| **Affected Users** | 123,400 |
| **Effort** | L |

**User Story:** "ในฐานะผู้จัดการ ฉันต้องการ delegate การอนุมัติให้รองเมื่อลาหยุด เพื่อไม่ให้งานค้าง"

**Technical Approach:** Build configurable approval workflow engine with delegation, auto-escalation, and multi-level approval. Support time-based delegation (leave period). Add approval history and delegation audit log.

**ROI Estimate:** ลดเวลา approval pending จาก 2.5 วัน เหลือ 4 ชม.

---

### Recommendation 16: Thai Document Templates

| Field | Detail |
|-------|--------|
| **Rank** | 16 |
| **Impact Score** | 7.0/10 |
| **Related Issues** | SD-001 |
| **Affected Users** | 156,700 |
| **Effort** | M |

**User Story:** "ในฐานะพนักงานขาย ฉันต้องการ template ใบเสนอราคาภาษาไทยที่มี VAT + WHT เพื่อส่งให้ลูกค้าได้ทันที"

**Technical Approach:** Create 10 Thai business document templates: ใบเสนอราคา, ใบแจ้งหนี้, ใบวางบิล, ใบเสร็จรับเงิน, ใบกำกับภาษี, ใบสั่งซื้อ, ใบรับสินค้า, ใบส่งของ, สัญญาจ้าง, หนังสือรับรอง. Include Thai fonts, VAT/WHT calculation, and company branding.

**ROI Estimate:** ลดเวลาสร้างเอกสารจาก 20 นาที เหลือ 3 นาที

---

### Recommendation 17: WCAG Accessibility Fixes

| Field | Detail |
|-------|--------|
| **Rank** | 17 |
| **Impact Score** | 6.8/10 |
| **Related Issues** | CROSS-017 |
| **Affected Users** | 123,400+ |
| **Effort** | L |

**User Story:** "ในฐานะผู้ใช้ที่ใช้ keyboard เป็นหลัก ฉันต้องการเข้าถึงทุก element ด้วย Tab key เพื่อทำงานได้โดยไม่ต้องใช้เมาส์"

**Technical Approach:** Audit all 34 inaccessible elements. Add proper tabindex, ARIA labels, and focus indicators. Implement skip navigation links. Test with screen readers (NVDA, VoiceOver). Ensure color contrast ratios meet WCAG 2.1 AA.

**ROI Estimate:** Compliance กับ WCAG 2.1 AA, เข้าถึงผู้ใช้ที่มีความพิการ + power keyboard users

---

### Recommendation 18: PDF Annotation & Document Markup

| Field | Detail |
|-------|--------|
| **Rank** | 18 |
| **Impact Score** | 6.7/10 |
| **Related Issues** | FD-003 |
| **Affected Users** | 134,500 |
| **Effort** | M |

**User Story:** "ในฐานะพนักงานบัญชี ฉันต้องการ annotate บน PDF ใน Finance Doc Hub เพื่อ mark จุดที่ต้องแก้ไขโดยไม่ต้อง download"

**Technical Approach:** Integrate PDF.js viewer with annotation layer. Support highlight, freehand draw, text notes, and stamps. Save annotations server-side linked to document version. Implement @mention in comments for collaboration.

**ROI Estimate:** ลดรอบ review จาก 3 รอบ เหลือ 1.5 รอบ

---

### Recommendation 19: Expense Policy Engine

| Field | Detail |
|-------|--------|
| **Rank** | 19 |
| **Impact Score** | 6.5/10 |
| **Related Issues** | EX-004 |
| **Affected Users** | 106,700 |
| **Effort** | L |

**User Story:** "ในฐานะ CFO ฉันต้องการให้ระบบตรวจสอบค่าใช้จ่ายอัตโนมัติตาม policy เพื่อลด fraud และ errors"

**Technical Approach:** Build rule engine with configurable policies: spending limits per category, per diem rates, approval thresholds, receipt requirements. Visual policy builder with if/then rules. Real-time validation on expense submission with warning/block indicators.

**ROI Estimate:** ลดค่าใช้จ่ายที่ผิด policy 60%, ลดเวลา manual review 50%

---

### Recommendation 20: Connection Health Monitoring & Alerts

| Field | Detail |
|-------|--------|
| **Rank** | 20 |
| **Impact Score** | 6.3/10 |
| **Related Issues** | CN-004 |
| **Affected Users** | 98,700 |
| **Effort** | M |

**User Story:** "ในฐานะ IT admin ฉันต้องการเห็นสถานะ connectors ทั้งหมดแบบ real-time เพื่อแก้ปัญหาก่อนที่ users จะ report"

**Technical Approach:** Build health check service that pings all active connectors every 60 seconds. Dashboard showing uptime %, latency, error rates, and last sync time. Alert via email/LINE when connector goes down. Auto-reconnect with exponential backoff.

**ROI Estimate:** ลด downtime 80%, ลด IT support tickets เรื่อง connector 65%

---

## 6. Quick Wins — Implement in < 2 Days Each

### Quick Win 1: Add Breadcrumb Navigation

| Field | Detail |
|-------|--------|
| **Issue** | CROSS-011 |
| **Files to Modify** | `poc-v2.html`, all `modules/*.html` (27 files) |
| **Estimated Time** | 8 hours |
| **Lines of Code** | ~150 (shared component) + ~5 per module file |
| **User Impact** | 189,100 users (47.3%) |

**Implementation:** Create reusable breadcrumb component. Add `<nav class="breadcrumb">` below header in every module. Auto-generate from URL path.

---

### Quick Win 2: Add พ.ศ. (Buddhist Era) Date Toggle

| Field | Detail |
|-------|--------|
| **Issue** | CROSS-006 |
| **Files to Modify** | `poc-v2.html` (global toggle), all date rendering functions |
| **Estimated Time** | 6 hours |
| **Lines of Code** | ~80 (date utility) + ~3 per date field |
| **User Impact** | 189,100 users (47.3%) |

**Implementation:** Add `convertToBE(date)` utility that adds 543 to year. Toggle in user settings stored in localStorage. Apply to all date displays via CSS class or data attribute.

---

### Quick Win 3: Add Progress Indicators for Long Operations

| Field | Detail |
|-------|--------|
| **Issue** | CROSS-005 (partial), VM-001 (partial) |
| **Files to Modify** | All `modules/*.html` with data loading |
| **Estimated Time** | 6 hours |
| **Lines of Code** | ~100 (loading skeleton component) |
| **User Impact** | 213,400 users (53.4%) |

**Implementation:** Create loading skeleton CSS animations. Replace empty states during load with skeleton placeholders. Add progress bar for operations >2 seconds.

---

### Quick Win 4: Add Search to System Settings

| Field | Detail |
|-------|--------|
| **Issue** | SY-003 |
| **Files to Modify** | `poc-v2.html` |
| **Estimated Time** | 4 hours |
| **Lines of Code** | ~60 |
| **User Impact** | 156,700 users (39.2%) |

**Implementation:** Add `<input type="search">` at top of settings page. Filter settings sections via `element.style.display = 'none'` for non-matching items. Highlight matching text.

---

### Quick Win 5: Notification Categorization

| Field | Detail |
|-------|--------|
| **Issue** | HD-005 |
| **Files to Modify** | `poc-v2.html`, `modules/home.html` |
| **Estimated Time** | 6 hours |
| **Lines of Code** | ~120 |
| **User Impact** | 108,900 users (27.2%) |

**Implementation:** Add `category` field to notification objects (urgent/info/system). Color-coded badges: red=urgent, blue=info, gray=system. Filter tabs in notification dropdown. Show count per category.

---

### Quick Win 6: Multi-file Upload for Receipts

| Field | Detail |
|-------|--------|
| **Issue** | EX-002 |
| **Files to Modify** | `modules/expense-receipt-ocr.html` |
| **Estimated Time** | 8 hours |
| **Lines of Code** | ~200 |
| **User Impact** | 178,900 users (44.7%) |

**Implementation:** Change `<input type="file">` to `multiple`. Add drag-and-drop zone. Show upload progress per file. Batch OCR processing with individual status indicators.

---

### Quick Win 7: Fix Thai Baht Symbol Consistency

| Field | Detail |
|-------|--------|
| **Issue** | CROSS-004 (partial) |
| **Files to Modify** | All `modules/*.html` with currency display |
| **Estimated Time** | 3 hours |
| **Lines of Code** | ~30 (utility function) |
| **User Impact** | 219,300 users (54.8%) |

**Implementation:** Create `formatCurrency(amount)` utility that always uses ฿ prefix with proper spacing. Replace all inline currency formatting. Use `Intl.NumberFormat('th-TH', {style:'currency', currency:'THB'})`.

---

### Quick Win 8: Fix Dark Mode for Remaining Modules

| Field | Detail |
|-------|--------|
| **Issue** | CROSS-016 |
| **Files to Modify** | `modules/expense-receipt-ocr.html`, `modules/finance-verification.html`, `modules/logistics-tracking.html`, `modules/sales-pipeline.html` |
| **Estimated Time** | 8 hours |
| **Lines of Code** | ~100 per file |
| **User Impact** | 123,400 users (30.9%) |

**Implementation:** Audit CSS variables in 4 broken modules. Add missing `body.dark` selectors. Test all components (tables, forms, modals, charts) in dark mode. Ensure no white flash on transition.

---

### Quick Win 9: Add Keyboard Shortcuts

| Field | Detail |
|-------|--------|
| **Issue** | CROSS-040 |
| **Files to Modify** | `poc-v2.html` (global handler) |
| **Estimated Time** | 6 hours |
| **Lines of Code** | ~150 |
| **User Impact** | 98,400 users (24.6%) |

**Implementation:** Add global `keydown` event listener. Shortcuts: Ctrl+K (search), Escape (close modal/sidebar), Ctrl+S (save), Ctrl+Z (undo), Ctrl+Shift+Z (redo), ? (show shortcut help). Add shortcut hints in tooltips.

---

### Quick Win 10: Add "Recently Visited" to Sidebar

| Field | Detail |
|-------|--------|
| **Issue** | CROSS-008 |
| **Files to Modify** | `poc-v2.html` |
| **Estimated Time** | 4 hours |
| **Lines of Code** | ~80 |
| **User Impact** | 167,800 users (42.0%) |

**Implementation:** Track page visits in localStorage (last 10 items). Display in sidebar section below navigation. Show icon + title + timestamp. Click to navigate. Clear all button.

---

### Quick Win 11: Add Loading Skeletons for Data Tables

| Field | Detail |
|-------|--------|
| **Issue** | CROSS-005 (partial) |
| **Files to Modify** | All `modules/*.html` with data tables |
| **Estimated Time** | 6 hours |
| **Lines of Code** | ~80 (shared CSS) + ~10 per table |
| **User Impact** | 213,400 users (53.4%) |

**Implementation:** Create `.skeleton` CSS class with pulse animation. Generate skeleton rows matching table structure during data fetch. Replace with real data on load complete.

---

### Quick Win 12: Fix Thai Text Sorting Order

| Field | Detail |
|-------|--------|
| **Issue** | CROSS-022 |
| **Files to Modify** | All `modules/*.html` with sortable tables |
| **Estimated Time** | 4 hours |
| **Lines of Code** | ~30 (sort utility) |
| **User Impact** | 87,600 users (21.9%) |

**Implementation:** Replace default `Array.sort()` with `Intl.Collator('th')` for all Thai text columns. Update sort functions in all data tables. Test with ก-ฮ, วรรณยุกต์, and mixed Thai-English.

---

### Quick Win 13: Add Export to Excel/CSV Across Analytics

| Field | Detail |
|-------|--------|
| **Issue** | PR-005 |
| **Files to Modify** | `modules/procurement-analytics.html`, `modules/expense-analytics.html`, `modules/sales-analytics.html`, `modules/finance-analytics.html` |
| **Estimated Time** | 8 hours |
| **Lines of Code** | ~150 (shared export utility) |
| **User Impact** | 131,200 users (32.8%) |

**Implementation:** Create `exportToCSV(data, filename)` and `exportToExcel(data, filename)` utilities using SheetJS. Add export buttons (CSV, Excel) to all analytics pages. Include Thai headers and proper encoding (UTF-8 BOM for Excel).

---

### Quick Win 14: Add Form Auto-save / Draft Functionality

| Field | Detail |
|-------|--------|
| **Issue** | PR-001 (partial) |
| **Files to Modify** | `modules/procurement-prpo.html`, `modules/expense-receipt-ocr.html`, `modules/sales-quotation-builder.html` |
| **Estimated Time** | 8 hours |
| **Lines of Code** | ~120 (shared auto-save utility) |
| **User Impact** | 213,400 users (53.4%) |

**Implementation:** Create `AutoSave` class that serializes form state to localStorage every 30 seconds. Show "Draft saved" indicator. On page load, check for saved draft and offer to restore. Clear draft on successful submit.

---

### Quick Win 15: Add Tooltips to All Chart Data Points

| Field | Detail |
|-------|--------|
| **Issue** | CROSS-019 |
| **Files to Modify** | All `modules/*-analytics.html`, `modules/*-dashboard.html` |
| **Estimated Time** | 6 hours |
| **Lines of Code** | ~100 |
| **User Impact** | 112,300 users (28.1%) |

**Implementation:** Enable Chart.js tooltip plugin with custom formatter. Show value, label, percentage, and comparison to previous period. Support Thai number formatting. Touch-friendly (tap to show on mobile).

---

## 7. Engineering Task Assignment

### File: `poc-v2.html` (Main Shell)

| Priority | Task | Related Issues | Sprint |
|:--------:|------|---------------|:------:|
| P0 | Add breadcrumb navigation component | CROSS-011 | S1 |
| P0 | Add global search (Ctrl+K command palette) | CROSS-002 | S2 |
| P0 | Flatten sidebar navigation architecture | CROSS-001 | S2 |
| P0 | Add recently visited items section | CROSS-008 | S1 |
| P1 | Add notification categorization (urgent/info/system) | HD-005 | S1 |
| P1 | Add พ.ศ. date toggle (global setting) | CROSS-006 | S1 |
| P1 | Implement role-based permission templates | SY-001 | S2 |
| P1 | Add keyboard shortcuts (Ctrl+K, Escape, Ctrl+S) | CROSS-040 | S1 |
| P1 | Fix Thai/English label consistency | CROSS-004 | S2 |
| P2 | Add 2FA / SSO implementation | CROSS-037 | S4 |
| P2 | Build LINE integration settings | SY-004 | S4 |
| P2 | Add training mode / sandbox toggle | CROSS-033 | S5 |
| P2 | Data migration toolkit wizard | CROSS-034 | S5 |
| P2 | Contextual help / guided tours framework | CROSS-042 | S5 |
| P2 | Approval delegation system (global) | CROSS-036 | S6 |
| P3 | Add settings page search | SY-003 | S1 |
| P3 | Billing page improvements | SY-002 | S1 |
| P3 | Add Thai help documentation | CROSS-003 | S6 |

### File: `modules/home.html` (Home Dashboard)

| Priority | Task | Related Issues | Sprint |
|:--------:|------|---------------|:------:|
| P0 | Add customizable widget dashboard (drag-and-drop) | HD-001 | S2 |
| P0 | Add quick action buttons | HD-004 | S1 |
| P1 | Add trend context to KPI widgets | HD-002 | S1 |
| P1 | Add KPI alert/threshold notifications | HD-006 | S3 |
| P1 | Add role-based dashboard views | CROSS-039 | S3 |
| P2 | Mobile-friendly chart redesign | HD-003 | S5 |
| P2 | Export dashboard to PPT | HD-007 | S5 |
| P2 | Add recently visited items widget | CROSS-008 | S1 |
| P3 | Scheduled report generation | CROSS-050 | S6 |

### File: `modules/procurement-prpo.html` (Purchase Requisition / Purchase Order)

| Priority | Task | Related Issues | Sprint |
|:--------:|------|---------------|:------:|
| P0 | Implement auto-save / draft for PR forms | PR-001 | S1 |
| P0 | Add PR templates for common purchases | PR-001 | S1 |
| P0 | Build PR-to-PO conversion flow | PR-002 | S2 |
| P1 | Add bulk PO creation | PR-004 | S3 |
| P1 | Add approval matrix by spending amount | PR-013 | S3 |
| P2 | Add Blanket PO / Contract PO support | PR-011 | S4 |
| P2 | Add Goods Receipt (GR) module | PR-010 | S4 |
| P3 | Add vendor portal for supplier self-service | PR-014 | S5 |

### File: `modules/procurement-analytics.html` (Procurement Analytics)

| Priority | Task | Related Issues | Sprint |
|:--------:|------|---------------|:------:|
| P0 | Add export to Excel/CSV | PR-005 | S1 |
| P1 | Add interactive chart tooltips | CROSS-019 | S1 |
| P2 | Add AI vendor recommendation | PR-012 | S6 |

### File: `modules/procurement-matching.html` (3-Way Match)

| Priority | Task | Related Issues | Sprint |
|:--------:|------|---------------|:------:|
| P1 | Simplify 3-way match comparison view | PR-003 | S2 |
| P1 | Side-by-side layout with highlight discrepancies | PR-003 | S2 |

### File: `modules/expense-receipt-ocr.html` (Expense Receipt OCR)

| Priority | Task | Related Issues | Sprint |
|:--------:|------|---------------|:------:|
| P0 | Enable multi-file upload (drag-and-drop) | EX-002 | S1 |
| P0 | Improve Thai OCR accuracy to >92% | EX-001 | S3 |
| P1 | Add advance payment (สำรองจ่าย) form | CROSS-030 | S3 |
| P1 | Add PromptPay QR Code generation | EX-010 | S3 |
| P1 | Add e-Slip bank integration (SCB, KBANK, BBL) | EX-012 | S4 |
| P2 | Add barcode/QR code scanning (mobile) | CROSS-047 | S5 |
| P2 | Add e-commerce receipt support (Shopee, Lazada) | EX-017 | S4 |
| P2 | Add corporate card reconciliation | EX-013 | S5 |
| P3 | Add split billing across departments/projects | EX-014 | S4 |

### File: `modules/expense-tasks.html` (Expense Tasks)

| Priority | Task | Related Issues | Sprint |
|:--------:|------|---------------|:------:|
| P1 | Add policy engine indicators (warning/block) | EX-004 | S3 |
| P1 | Add per diem calculator (Thai government rates) | EX-011 | S3 |
| P2 | Add mileage calculator | EX-015 | S4 |
| P2 | Add event budget tracking | EV-001 | S5 |

### File: `modules/expense-dashboard.html` (Expense Dashboard)

| Priority | Task | Related Issues | Sprint |
|:--------:|------|---------------|:------:|
| P1 | Add category drill-down analytics | EX-005 | S2 |
| P2 | Add automatic exchange rate updates | EX-016 | S4 |

### File: `modules/expense-approval.html` (Expense Approval)

| Priority | Task | Related Issues | Sprint |
|:--------:|------|---------------|:------:|
| P1 | Implement flexible approval workflow + delegation | EX-003 | S2 |
| P2 | Add approval delegation for leave periods | CROSS-036 | S6 |

### File: `modules/finance-verification.html` (Finance Verification)

| Priority | Task | Related Issues | Sprint |
|:--------:|------|---------------|:------:|
| P1 | Add verification checklist templates | FD-002 | S2 |
| P1 | Add e-Tax Invoice compliance | CROSS-031 | S3 |
| P2 | Add PDF annotation and markup | FD-003 | S3 |

### File: `modules/finance-cases.html` (Finance Cases)

| Priority | Task | Related Issues | Sprint |
|:--------:|------|---------------|:------:|
| P1 | Add document grouping by type | FD-001 | S2 |
| P2 | Add Express/PEAK/Prosoft sync | FD-011 | S4 |
| P2 | Add document version control | FD-012 | S4 |
| P2 | Add monthly closing workflow | FD-010 | S4 |
| P3 | Add digital stamp/seal | FD-013 | S5 |

### File: `modules/finance-analytics.html` (Finance Analytics)

| Priority | Task | Related Issues | Sprint |
|:--------:|------|---------------|:------:|
| P1 | Add real-time dashboard update | FD-004 | S3 |
| P1 | Improve Thai keyword search accuracy | FD-005 | S2 |
| P2 | Add export to Excel/CSV | PR-005 | S1 |

### File: `modules/logistics-tracking.html` (Logistics Tracking)

| Priority | Task | Related Issues | Sprint |
|:--------:|------|---------------|:------:|
| P0 | Add Thai provider integration UI (Kerry/Flash/J&T/Post) | LG-010 | S4 |
| P1 | Add real-time shipment tracking | LG-003 | S4 |
| P1 | Fix dark mode | CROSS-016 | S2 |
| P2 | Add barcode scanning for shipment verification | CROSS-047 | S5 |

### File: `modules/logistics-fx-dashboard.html` (Logistics FX Dashboard)

| Priority | Task | Related Issues | Sprint |
|:--------:|------|---------------|:------:|
| P1 | Add Thai rate cards (zone-based, weight-based) | LG-002 | S3 |
| P1 | Fix province names to Thai | LG-003b | S1 |
| P2 | Add cost-per-unit analysis | LG-004 | S4 |

### File: `modules/logistics-freight-ocr.html` (Logistics Freight OCR)

| Priority | Task | Related Issues | Sprint |
|:--------:|------|---------------|:------:|
| P0 | Add Thai freight document OCR support | LG-001 | S3 |
| P2 | Add customs declaration form support | LG-012 | S5 |

### File: `modules/logistics-cost-calculator.html` (Logistics Cost Calculator)

| Priority | Task | Related Issues | Sprint |
|:--------:|------|---------------|:------:|
| P1 | Support Thai logistics rate structures | LG-002 | S3 |
| P2 | Add warehouse management module | LG-011 | S5 |

### File: `modules/sales-dashboard.html` (Sales Dashboard)

| Priority | Task | Related Issues | Sprint |
|:--------:|------|---------------|:------:|
| P1 | Add Thai document templates (ใบเสนอราคา, ใบแจ้งหนี้) | SD-001 | S3 |
| P1 | Add withholding tax auto-calculation | SD-011 | S4 |
| P2 | Add e-Signature support | SD-010 | S4 |
| P2 | Add automated follow-up reminders | SD-013 | S5 |

### File: `modules/sales-pipeline.html` (Sales Pipeline)

| Priority | Task | Related Issues | Sprint |
|:--------:|------|---------------|:------:|
| P1 | Add drag-and-drop stage changes | SD-002 | S3 |
| P1 | Add auto-generate documents from pipeline | SD-003 | S4 |
| P1 | Fix dark mode | CROSS-016 | S2 |
| P2 | Add CRM integration (Salesforce, HubSpot) | SD-012 | S5 |

### File: `modules/sales-analytics.html` (Sales Analytics)

| Priority | Task | Related Issues | Sprint |
|:--------:|------|---------------|:------:|
| P1 | Add conversion rate analysis | SD-004 | S4 |
| P2 | Add export to Excel/CSV | PR-005 (pattern) | S1 |

### File: `modules/vendor-management.html` (Vendor Management)

| Priority | Task | Related Issues | Sprint |
|:--------:|------|---------------|:------:|
| P0 | Optimize performance (8-12s -> <1.5s) | VM-001 | S2 |
| P0 | Add TIS-620 encoding support | VM-002 | S2 |
| P1 | Add auto vendor scoring system | VM-003 | S3 |
| P1 | Add contract expiry notifications | VM-007 | S3 |
| P1 | Add performance trend charts | VM-004 | S4 |
| P2 | Add vendor risk assessment | VM-006 | S5 |
| P2 | Add audit report date filtering | VM-005 | S1 |

### File: `connectors/connector-hub.html` (Connector Hub)

| Priority | Task | Related Issues | Sprint |
|:--------:|------|---------------|:------:|
| P0 | Build guided setup wizard (3-step) | CN-001 | S4 |
| P0 | Add pre-built Thai system connectors | CN-002 | S4 |
| P1 | Add one-click connector install | CN-001 | S4 |
| P1 | Add connector testing sandbox | CN-001 | S4 |
| P2 | Add WeChat integration | INT-003 | S6 |

### File: `connectors/api-dashboard.html` (API Dashboard)

| Priority | Task | Related Issues | Sprint |
|:--------:|------|---------------|:------:|
| P0 | Add human-readable error messages (Thai) | CN-003 | S1 |
| P1 | Add connection health monitoring dashboard | CN-004 | S4 |
| P2 | Add API rate limiting dashboard | SY-006 | S5 |

### File: `modules/customer-feedback.html` (Customer Feedback)

| Priority | Task | Related Issues | Sprint |
|:--------:|------|---------------|:------:|
| P1 | Add Thai sentiment analysis | CF-001 | S6 |
| P1 | Add conditional logic to survey builder | CF-002 | S6 |
| P1 | Add feedback routing to relevant teams | CF-006 | S4 |
| P2 | Add CRM/ticket system integration | CF-003 | S5 |
| P2 | Add NPS real-time tracking | CF-005 | S5 |
| P2 | Add trend analysis across periods | CF-004 | S5 |

---

## Appendix A: Complete Issue Registry (120 Issues)

### Summary by Severity

| Severity | Count | Total Users Affected |
|----------|:-----:|---------------------:|
| Critical | 28 | 5,287,600 (cumulative) |
| High | 56 | 7,432,100 (cumulative) |
| Medium | 32 | 2,987,400 (cumulative) |
| Low | 4 | 226,700 (cumulative) |
| **Total** | **120** | — |

### Summary by Module

| Module | Issues | Avg Users/Issue |
|--------|:------:|:---------------:|
| Cross-Module | 50 | 153,200 |
| Expense & Receipt | 14 | 134,800 |
| Procurement | 8 | 140,700 |
| System | 10 | 118,400 |
| Connectors | 6 | 132,000 |
| Finance Doc Hub | 8 | 112,600 |
| Logistics FX | 8 | 107,200 |
| Sales Doc Gen | 7 | 116,900 |
| Vendor Management | 7 | 104,200 |
| Home Dashboard | 7 | 125,600 |
| Customer Feedback | 6 | 97,900 |

### Summary by Status

| Status | Count |
|--------|:-----:|
| Open | 116 |
| In Progress | 4 |
| Resolved | 0 |

---

## Appendix B: Success Metrics & KPIs

### Target Module Scores After 12 Weeks

| Module | Before | After Sprint 3 | After Sprint 6 | Target |
|--------|:------:|:--------------:|:--------------:|:------:|
| Connectors | 2.19 | 2.80 | 4.00 | 4.50 |
| System | 2.54 | 3.30 | 4.10 | 4.50 |
| Vendor Management | 2.65 | 3.40 | 4.20 | 4.50 |
| Finance Doc Hub | 2.68 | 3.20 | 4.00 | 4.50 |
| Logistics FX | 2.68 | 3.30 | 4.10 | 4.50 |
| Procurement | 2.69 | 3.60 | 4.30 | 4.50 |
| Expense & Receipt | 2.70 | 3.50 | 4.20 | 4.50 |
| Customer Feedback | 2.78 | 2.90 | 3.80 | 4.50 |
| Home Dashboard | 2.86 | 3.70 | 4.30 | 4.50 |
| Sales Doc Gen | 2.93 | 3.40 | 4.10 | 4.50 |

### Key Performance Indicators

| KPI | Current | Target (12 weeks) | Target (24 weeks) |
|-----|:-------:|:------------------:|:------------------:|
| Avg clicks per task | 4.7 | 2.5 | 2.0 |
| Page load time | 4.8s | 2.0s | 1.2s |
| Thai OCR accuracy | 67% | 85% | 95% |
| Mobile task completion | 22% | 65% | 85% |
| User satisfaction (NPS) | -12 | +15 | +40 |
| Feature adoption rate | 34% | 60% | 80% |
| Support tickets/week | 2,400 | 1,200 | 600 |
| Connector setup time | 2-3 days | 30 min | 10 min |
| Approval cycle time | 2.5 days | 4 hours | 1 hour |
| Data entry time/receipt | 5 min | 1 min | 30 sec |

---

## Appendix C: Risk Matrix

| Risk | Probability | Impact | Mitigation |
|------|:-----------:|:------:|------------|
| Thai OCR model training delays | High | Critical | Start data collection immediately; use hybrid approach (OCR + manual) as interim |
| LINE API rate limits | Medium | High | Implement message queuing; negotiate enterprise tier |
| Banking API partnership delays | High | High | Prioritize PromptPay (open API); negotiate bank partnerships in parallel |
| User resistance to UI changes | Medium | High | A/B testing; gradual rollout; training mode first |
| Performance regression with new features | Low | Critical | Performance budget per PR; automated lighthouse CI checks |
| Thai localization quality | Medium | Medium | Native Thai speaker review; community feedback loop |

---

## Appendix D: Team Allocation Recommendation

| Team | Size | Sprint Focus | Key Files |
|------|:----:|-------------|-----------|
| Team A: Core UX | 4 engineers | Navigation, search, breadcrumbs, dashboard | `poc-v2.html`, `modules/home.html` |
| Team B: Thai Business | 4 engineers | OCR, e-Tax, PromptPay, per diem, templates | `modules/expense-*.html`, `modules/sales-*.html` |
| Team C: Integration | 3 engineers | Connectors, LINE, banking, logistics APIs | `connectors/*.html`, `modules/logistics-*.html` |
| Team D: Mobile & A11y | 2 engineers | Responsive design, keyboard access, PWA | All `modules/*.html` CSS |
| Team E: Performance | 2 engineers | Load time, caching, database optimization | All files (infrastructure) |
| Team F: Localization | 2 engineers | Thai translation, พ.ศ., Thai sort, i18n framework | All files (strings) |

**Total: 17 engineers for 12-week execution**

---

*Document generated from analysis of 120 customer feedback issues affecting 400,000 users across 11 modules. All recommendations are prioritized by user impact count and aligned with Thai business requirements.*

*Next review: After Sprint 2 completion (Week 4)*
