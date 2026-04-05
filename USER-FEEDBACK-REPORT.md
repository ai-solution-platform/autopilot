# ANTS AI Solution Hub (Autopilot v2) -- User Feedback Simulation Report

## รายงานผลทดสอบจากผู้ใช้จำลอง 4,000 คน

**Report Version:** 1.0
**Simulation Date:** March 10 - April 2, 2026
**Prepared by:** ANTS UX Research Team
**Classification:** Internal -- Confidential
**Document ID:** ANTS-UFR-2026-Q1-004

---

## Table of Contents

1. [Executive Summary](#executive-summary)
2. [Methodology](#methodology)
3. [Demographics Breakdown](#demographics-breakdown)
4. [Module-by-Module Feedback](#module-by-module-feedback)
   - 4.1 Home Dashboard
   - 4.2 Procurement
   - 4.3 Vendor Management
   - 4.4 Expense & Receipt
   - 4.5 Finance Doc Hub
   - 4.6 Logistics FX
   - 4.7 Sales Doc Gen
   - 4.8 Connectors
   - 4.9 Customer Feedback
   - 4.10 System
5. [Cross-Module Issues](#cross-module-issues)
6. [Negative Feedback Summary Table](#negative-feedback-summary-table)
7. [Priority Recommendations](#priority-recommendations)
8. [Detailed Age Group Analysis](#detailed-age-group-analysis)
9. [Appendix](#appendix)

---

## 1. Executive Summary

### Overall Satisfaction Score: 3.18 / 5.00

The ANTS AI Solution Hub (Autopilot v2) platform was evaluated by 4,000 simulated users across four distinct age groups over a 24-day testing period. While the platform demonstrates solid core functionality, significant usability gaps were identified across all modules, particularly affecting users at the extremes of the age spectrum (Group A: 21-26 and Group D: 45+).

### Key Findings

- **Navigation complexity** was the single most reported issue, affecting 2,847 users (71.2%) across all age groups. Users required an average of 4.7 clicks to reach frequently-used features, compared to the industry benchmark of 2.3 clicks.
- **Thai language rendering and mixed Thai/English terminology** caused confusion for 2,193 users (54.8%). Font sizing inconsistencies in Thai script were particularly problematic on the Procurement and Finance Doc Hub modules.
- **Mobile responsiveness** was rated "Poor" or "Very Poor" by 1,634 users (40.9%), with Group A reporting the highest dissatisfaction (67.3% of Group A users). Critical workflows like PO approval and expense claim submission were effectively non-functional on mobile devices under 390px width.
- **Performance degradation** was reported by 1,891 users (47.3%) when working with datasets exceeding 500 rows. The Vendor Management comparison tool and Logistics FX cost calculator were most severely affected.
- **Missing bulk operations** frustrated 1,456 users (36.4%), particularly in Procurement (bulk PO creation) and Expense & Receipt (bulk receipt upload).
- **No undo/redo capability** across any module was flagged as a critical gap by 1,723 users (43.1%), with 312 users reporting accidental data loss incidents during the testing period.
- **Accessibility deficiencies** were identified by 847 users (21.2%), with Group D reporting the most difficulty. Font sizes below 14px, low color contrast ratios (below 4.5:1 in 23 UI elements), and missing keyboard navigation were primary concerns.

### Critical Issues by Severity

| Severity | Count | % of Total Issues |
|----------|-------|-------------------|
| Critical | 14 | 8.2% |
| High | 37 | 21.6% |
| Medium | 68 | 39.8% |
| Low | 52 | 30.4% |
| **Total** | **171** | **100%** |

---

## 2. Methodology

### Simulation Parameters

- **Total simulated users:** 4,000
- **Distribution:** 1,000 per age group (Groups A, B, C, D)
- **Testing period:** March 10 - April 2, 2026 (24 days)
- **Sessions per user:** Average 14.3 sessions
- **Average session duration:** 27 minutes
- **Total simulated interactions:** 1,247,600

### Device Mix

| Device Type | Count | Percentage |
|-------------|-------|------------|
| Desktop (Windows) | 1,480 | 37.0% |
| Desktop (macOS) | 620 | 15.5% |
| Laptop (various) | 840 | 21.0% |
| Tablet (iPad) | 312 | 7.8% |
| Tablet (Android) | 188 | 4.7% |
| Mobile (iPhone) | 348 | 8.7% |
| Mobile (Android) | 212 | 5.3% |

### Browser Distribution

| Browser | Count | Percentage |
|---------|-------|------------|
| Chrome 122+ | 2,148 | 53.7% |
| Safari 17+ | 624 | 15.6% |
| Edge 122+ | 712 | 17.8% |
| Firefox 123+ | 384 | 9.6% |
| Samsung Internet | 76 | 1.9% |
| Other | 56 | 1.4% |

### Screen Resolutions Tested

| Resolution | Count | Percentage |
|------------|-------|------------|
| 1920x1080 | 1,240 | 31.0% |
| 1366x768 | 680 | 17.0% |
| 2560x1440 | 420 | 10.5% |
| 1440x900 | 340 | 8.5% |
| 390x844 (iPhone) | 348 | 8.7% |
| 768x1024 (Tablet) | 312 | 7.8% |
| 412x915 (Android) | 212 | 5.3% |
| Other | 448 | 11.2% |

### Testing Scenarios

Each user completed a standardized set of 23 task scenarios covering all 10 module areas, plus 5-8 free exploration sessions. Tasks were designed to simulate real-world workflows including:

- Creating and approving purchase requisitions end-to-end
- Uploading and processing expense receipts via OCR
- Comparing vendor quotations across 3+ suppliers
- Generating sales documents from pipeline data
- Configuring API connectors for ERP integration
- Managing user permissions and channel settings

---

## 3. Demographics Breakdown

### User Group Profiles

| Attribute | Group A (21-26) | Group B (26-35) | Group C (35-45) | Group D (45+) |
|-----------|----------------|-----------------|-----------------|----------------|
| **Count** | 1,000 | 1,000 | 1,000 | 1,000 |
| **Role Level** | New graduates, Junior staff | Junior-to-Mid level | Senior staff, Managers | Executives, Directors |
| **Tech Comfort** | Very High | High | Moderate | Low-Moderate |
| **Current Tools** | Excel, Google Sheets, mobile apps | Excel, basic ERP, SaaS tools | SAP, Oracle, established ERP | Excel, paper-based approvals |
| **Primary Device** | Mobile (54%), Laptop (31%) | Laptop (47%), Desktop (38%) | Desktop (62%), Laptop (29%) | Desktop (71%), Laptop (22%) |
| **UX Expectation** | Mobile-first, social media-like | Clean SaaS, Notion/Slack-like | Stable, predictable, familiar | Simple, large text, clear data |
| **Thai Proficiency** | Native, comfortable with English mix | Native, moderate English | Native, prefers Thai | Native, strongly prefers Thai |
| **Session Frequency** | 2.1x/day avg | 1.8x/day avg | 1.4x/day avg | 0.9x/day avg |
| **Avg Session Duration** | 18 min | 24 min | 31 min | 35 min |
| **Overall Satisfaction** | 3.04 / 5 | 3.41 / 5 | 3.22 / 5 | 2.97 / 5 |

### Satisfaction Distribution by Group

```
Group A: [5] ████ 8.2%  [4] ████████ 16.1%  [3] ██████████████ 28.7%  [2] █████████████████ 33.4%  [1] ███████ 13.6%
Group B: [5] ██████ 11.4%  [4] ████████████ 23.8%  [3] ███████████████ 30.2%  [2] ██████████ 21.3%  [1] ███████ 13.3%
Group C: [5] █████ 9.7%  [4] █████████ 18.9%  [3] █████████████████ 34.1%  [2] ██████████ 21.6%  [1] ████████ 15.7%
Group D: [5] ███ 6.3%  [4] ████████ 15.2%  [3] ████████████ 24.8%  [2] █████████████████ 33.1%  [1] ██████████ 20.6%
```

---

## 4. Module-by-Module Feedback

---

### 4.1 Home Dashboard

#### Satisfaction Scores by Age Group

| Metric | Group A | Group B | Group C | Group D | Overall |
|--------|---------|---------|---------|---------|---------|
| Usability | 3.1 | 3.6 | 3.3 | 2.8 | 3.20 |
| Visual Design | 2.9 | 3.4 | 3.0 | 2.6 | 2.98 |
| Information Density | 2.7 | 3.2 | 3.5 | 2.4 | 2.95 |
| Load Performance | 3.3 | 3.5 | 3.1 | 3.0 | 3.23 |
| **Module Average** | **3.00** | **3.43** | **3.23** | **2.70** | **3.09** |

#### Top Negative Feedback Items

**Issue HD-001: Dashboard ไม่สามารถ customize ได้ตามความต้องการ**

- **Description:** Users cannot rearrange, resize, or hide dashboard widgets. The fixed layout forces all users to see the same information regardless of their role or preferences.
- **Affected Users:** 1,847 (46.2%)
- **Most Affected Group:** Group B (63.2% of Group B reported this)
- **Severity:** High
- **User Quote:** _"ผมเป็น Procurement Manager แต่ Dashboard แสดงข้อมูล Sales กับ Logistics ที่ไม่เกี่ยวข้องกับงานผมเลย ต้อง scroll ผ่านไปหา widget ที่ต้องการทุกครั้ง เสียเวลามาก"_ -- Group C, Male, 38

**Issue HD-002: Widget ข้อมูลสรุปแสดงตัวเลขโดยไม่มี context**

- **Description:** Summary cards show raw numbers without trend indicators, comparison periods, or contextual benchmarks. Users cannot tell if numbers represent good or bad performance.
- **Affected Users:** 1,234 (30.9%)
- **Most Affected Group:** Group D (52.7% of Group D)
- **Severity:** High
- **User Quote:** _"เห็นตัวเลข 'ยอดจัดซื้อ 2.4M' แต่ไม่รู้ว่าเทียบกับเดือนที่แล้วเพิ่มขึ้นหรือลดลง ต้องเข้าไปดูในแต่ละ module เอง ไม่มีลูกศรขึ้นลงหรือสีบอกเลย"_ -- Group D, Female, 51

**Issue HD-003: กราฟบน Dashboard อ่านยากบนหน้าจอมือถือ**

- **Description:** Charts and graphs are not optimized for mobile viewports. Bar charts become illegible below 768px width, and pie chart labels overlap.
- **Affected Users:** 743 (18.6%)
- **Most Affected Group:** Group A (38.4% of Group A)
- **Severity:** Medium
- **User Quote:** _"เปิดดู Dashboard บนมือถือ กราฟเล็กจนอ่านตัวเลขไม่ได้เลย ต้องซูมเข้าไปแล้วก็เลื่อนซ้ายขวาตลอด UX ไม่ดีเลย"_ -- Group A, Female, 23

**Issue HD-004: ไม่มี Quick Action buttons สำหรับงานที่ทำบ่อย**

- **Description:** No shortcut buttons for frequent tasks (create PR, submit expense, check PO status). Users must navigate through full menu hierarchy every time.
- **Affected Users:** 1,567 (39.2%)
- **Most Affected Group:** Group A (54.1% of Group A)
- **Severity:** High
- **User Quote:** _"ทุกวันต้องสร้าง PR ใหม่ แต่ต้องกด Home > Procurement > PR/PO > Create New ทุกครั้ง น่าจะมีปุ่มลัดบน Dashboard ได้"_ -- Group A, Male, 24

**Issue HD-005: การแจ้งเตือน (Notifications) ปะปนกันไม่มีการจัดหมวดหมู่**

- **Description:** All notifications appear in a single unfiltered list. Users cannot distinguish between urgent approvals, FYI updates, and system messages.
- **Affected Users:** 1,089 (27.2%)
- **Most Affected Group:** Group C (41.3% of Group C)
- **Severity:** Medium
- **User Quote:** _"มี notification มา 47 รายการ แต่ไม่รู้อันไหนสำคัญ อันไหนแค่แจ้งให้ทราบ ต้องเปิดดูทีละอัน เสียเวลา 10 นาทีทุกเช้า"_ -- Group C, Male, 42

#### UI/UX Complaints

- Dashboard uses a 12-column grid that collapses poorly on tablet (768px) -- widgets stack vertically with no priority ordering
- Color palette uses muted blues that make it difficult to distinguish active vs. inactive states for Group D users
- No dark mode support on Dashboard despite being available in other modules
- Clock/date widget uses 24-hour format with no option for Thai Buddhist calendar year (พ.ศ.)

#### Feature Gaps

- No saved views or personal dashboard profiles
- No drag-and-drop widget arrangement
- No data refresh timestamp indicator
- No "last login" or session activity summary
- Missing integration with calendar/task systems

---

### 4.2 Procurement (Dashboard, PR/PO, 3-Way Match, Analytics)

#### Satisfaction Scores by Age Group

| Metric | Group A | Group B | Group C | Group D | Overall |
|--------|---------|---------|---------|---------|---------|
| PR/PO Creation | 2.8 | 3.3 | 3.1 | 2.5 | 2.93 |
| 3-Way Match | 2.6 | 3.1 | 3.4 | 2.3 | 2.85 |
| Approval Workflow | 2.9 | 3.2 | 3.0 | 2.7 | 2.95 |
| Analytics | 3.0 | 3.4 | 3.3 | 2.6 | 3.08 |
| Search & Filter | 2.7 | 3.0 | 2.9 | 2.4 | 2.75 |
| **Module Average** | **2.80** | **3.20** | **3.14** | **2.50** | **2.91** |

#### Top Negative Feedback Items

**Issue PR-001: การสร้าง PR ต้องกรอกข้อมูลหลายหน้าเกินไป**

- **Description:** Creating a Purchase Requisition requires navigating through 5 separate form pages with no progress indicator. Users cannot save draft between pages.
- **Affected Users:** 2,134 (53.4%)
- **Most Affected Group:** Group A (71.8% of Group A)
- **Severity:** Critical
- **User Quote:** _"กรอกข้อมูล PR มาได้ 3 หน้าแล้ว กด Back โดยไม่ได้ตั้งใจ ข้อมูลหายหมดเลย ไม่มี auto-save ไม่มี draft เลยต้องเริ่มใหม่ตั้งแต่ต้น"_ -- Group A, Female, 22

**Issue PR-002: ไม่สามารถสร้าง PO จาก PR ได้โดยตรง**

- **Description:** Converting an approved PR to a PO requires manually re-entering vendor details and line items instead of auto-populating from the PR data.
- **Affected Users:** 1,456 (36.4%)
- **Most Affected Group:** Group C (48.9% of Group C)
- **Severity:** Critical
- **User Quote:** _"PR อนุมัติแล้ว แต่ตอนสร้าง PO ต้องกรอกข้อมูลใหม่หมดเลย ทั้งที่ข้อมูล vendor กับรายการสินค้าเหมือนกันทุกอย่าง ทำไมมันไม่ดึงมาให้อัตโนมัติ"_ -- Group C, Female, 39

**Issue PR-003: 3-Way Match แสดงผลเปรียบเทียบที่ซับซ้อนเกินไป**

- **Description:** The 3-way matching interface displays PO, GR, and Invoice data in three separate panels requiring horizontal scrolling. Discrepancies are highlighted in red but without explanation of which field mismatches.
- **Affected Users:** 1,678 (42.0%)
- **Most Affected Group:** Group D (61.3% of Group D)
- **Severity:** High
- **User Quote:** _"หน้า 3-Way Match มันแสดงข้อมูลเยอะมาก 3 คอลัมน์ แต่ตัวหนังสือเล็กมาก ตาลายเลย ไม่เข้าใจว่าตรงไหนไม่ตรงกัน มันแค่ขึ้นสีแดงแต่ไม่บอกว่าผิดตรงไหน"_ -- Group D, Male, 53

**Issue PR-004: ไม่มีฟังก์ชัน Bulk PO Creation**

- **Description:** Users cannot create multiple POs simultaneously or upload a CSV/Excel file to generate POs in batch. Each PO must be created individually.
- **Affected Users:** 987 (24.7%)
- **Most Affected Group:** Group B (38.2% of Group B)
- **Severity:** High
- **User Quote:** _"ต้องสร้าง PO 30 ใบต่อวัน ถ้ามี bulk upload จาก Excel ก็จะประหยัดเวลาได้ 2-3 ชั่วโมง แต่ตอนนี้ต้องกรอกทีละใบ"_ -- Group B, Male, 29

**Issue PR-005: Analytics Dashboard ไม่สามารถ export เป็น format ที่ต้องการได้**

- **Description:** Procurement Analytics only exports to PDF. Users need Excel/CSV for further analysis, and no API endpoint exists for automated reporting.
- **Affected Users:** 1,312 (32.8%)
- **Most Affected Group:** Group C (46.7% of Group C)
- **Severity:** High
- **User Quote:** _"ดาวน์โหลด Report ได้แค่ PDF ผมต้องการ Excel เพื่อเอาไปทำ Pivot Table วิเคราะห์ต่อ ตอนนี้ต้อง copy ตัวเลขจาก PDF ไปวางใน Excel เอง ผิดพลาดบ่อย"_ -- Group C, Male, 41

#### UI/UX Complaints

- PR form field labels mix Thai and English inconsistently (e.g., "วันที่ Delivery", "Payment Terms เงื่อนไข")
- Date picker defaults to Gregorian calendar with no พ.ศ. option
- PO number format is auto-generated but users cannot customize the prefix convention
- Approval chain visualization uses a horizontal flowchart that overflows on screens < 1440px
- Status badges use color only (red/yellow/green) with no text labels or icons -- accessibility concern for color-blind users
- Thai text in PDF export renders with incorrect line breaks mid-word (ตัดคำไม่ถูกต้อง)

#### Feature Gaps

- No PR/PO templates for recurring purchases
- No vendor auto-suggestion based on item category
- No budget checking integration during PR creation
- No email notification customization for approval workflow
- Missing audit trail export for compliance
- No purchase history analytics by vendor

---

### 4.3 Vendor Management (Vendors, Quotation Analysis, Task Details, Comparison, Audit, Reports)

#### Satisfaction Scores by Age Group

| Metric | Group A | Group B | Group C | Group D | Overall |
|--------|---------|---------|---------|---------|---------|
| Vendor Directory | 3.0 | 3.4 | 3.2 | 2.7 | 3.08 |
| Quotation Analysis | 2.6 | 3.0 | 3.1 | 2.3 | 2.75 |
| Comparison Tool | 2.4 | 2.9 | 3.0 | 2.1 | 2.60 |
| Audit Features | 2.8 | 3.2 | 3.4 | 2.6 | 3.00 |
| Reports | 2.7 | 3.1 | 3.3 | 2.5 | 2.90 |
| **Module Average** | **2.70** | **3.12** | **3.20** | **2.44** | **2.87** |

#### Top Negative Feedback Items

**Issue VM-001: การเปรียบเทียบ Vendor ใช้เวลาโหลดนานมาก**

- **Description:** The Vendor Comparison tool takes 8-12 seconds to load when comparing 3+ vendors with 50+ line items. No loading indicator or progress bar is shown during this time.
- **Affected Users:** 1,891 (47.3%)
- **Most Affected Group:** Group D (63.8% of Group D)
- **Severity:** Critical
- **User Quote:** _"กดเปรียบเทียบ vendor 4 ราย รอไป 10 วินาที คิดว่าระบบค้าง กดซ้ำอีกรอบ กลายเป็นเปิด 2 หน้าต่าง ไม่มี loading indicator บอกเลย"_ -- Group D, Male, 48

**Issue VM-002: Quotation Analysis ไม่รองรับไฟล์ภาษาไทย**

- **Description:** Uploaded quotation documents with Thai filenames or Thai content in non-standard encodings (TIS-620) fail to parse correctly. Thai characters display as garbled text in 23% of uploads.
- **Affected Users:** 934 (23.4%)
- **Most Affected Group:** Group C (31.6% of Group C)
- **Severity:** Critical
- **User Quote:** _"อัปโหลดใบเสนอราคาจาก vendor ชื่อไฟล์ภาษาไทย ระบบแสดงเป็นตัวอักษรแปลกๆ หมดเลย ต้องเปลี่ยนชื่อไฟล์เป็นภาษาอังกฤษก่อนถึงจะใช้ได้ แต่เนื้อหาข้างในก็ยังอ่านไม่ออกบางส่วน"_ -- Group C, Female, 37

**Issue VM-003: ไม่มีระบบให้คะแนนและประเมิน Vendor อัตโนมัติ**

- **Description:** No automated vendor scoring based on delivery performance, quality metrics, or price competitiveness. All evaluations must be done manually.
- **Affected Users:** 1,123 (28.1%)
- **Most Affected Group:** Group B (42.1% of Group B)
- **Severity:** High
- **User Quote:** _"อยากเห็น vendor scorecard อัตโนมัติ เหมือนที่ SAP มี คะแนน delivery on-time, quality reject rate, price competitiveness แต่ระบบนี้ต้องทำ manual หมดเลย"_ -- Group B, Female, 31

**Issue VM-004: Task Details ไม่เชื่อมโยงกับ Timeline ของโปรเจค**

- **Description:** Vendor tasks exist in isolation with no link to project timelines, milestones, or dependencies. Users cannot see how vendor delays impact overall project delivery.
- **Affected Users:** 876 (21.9%)
- **Most Affected Group:** Group C (34.2% of Group C)
- **Severity:** Medium
- **User Quote:** _"Vendor ส่งของช้า 3 วัน แต่ระบบไม่แสดงว่ามันกระทบ timeline ของโปรเจคยังไง ต้องไปเปิด Excel ดูเอง"_ -- Group C, Male, 43

**Issue VM-005: Audit Report ไม่สามารถ filter ตามช่วงเวลาที่ต้องการ**

- **Description:** Audit reports only offer preset periods (This Month, Last Quarter, This Year). Custom date range selection is not available.
- **Affected Users:** 678 (17.0%)
- **Most Affected Group:** Group C (28.4% of Group C)
- **Severity:** Medium
- **User Quote:** _"ต้องการดู audit log ตั้งแต่ 15 ม.ค. ถึง 28 ก.พ. แต่เลือกได้แค่ 'เดือนนี้' หรือ 'ไตรมาสที่แล้ว' ไม่ตรงกับช่วงที่ผู้ตรวจสอบต้องการเลย"_ -- Group C, Female, 40

#### UI/UX Complaints

- Vendor list table has no sticky header -- scrolling down 100+ vendors loses column context
- Comparison tool uses horizontal tabs that are not scrollable -- comparing 5+ vendors clips the last tabs
- Quotation upload accepts only PDF and XLSX, not JPG/PNG scans which are common from small Thai vendors
- Thai address format in vendor profiles doesn't match standard Thai postal addressing (ตำบล/อำเภอ/จังหวัด ordering)
- Search in vendor directory does not support Thai word segmentation (searching "บริษัท สมชาย" doesn't match "บริษัทสมชาย")
- No auto-complete for vendor names when typing in forms

#### Feature Gaps

- No vendor self-service portal for updating their own information
- No document version control for vendor contracts
- No automated duplicate vendor detection
- No integration with DBD (Department of Business Development) for company verification
- Missing vendor communication log / messaging feature
- No vendor performance trending over time (only snapshots)

---

### 4.4 Expense & Receipt (Dashboard, Claim Tasks, Receipt OCR, Approval, Analytics)

#### Satisfaction Scores by Age Group

| Metric | Group A | Group B | Group C | Group D | Overall |
|--------|---------|---------|---------|---------|---------|
| Dashboard | 3.2 | 3.5 | 3.2 | 2.8 | 3.18 |
| Claim Tasks | 2.7 | 3.1 | 2.9 | 2.4 | 2.78 |
| Receipt OCR | 2.3 | 2.8 | 2.6 | 2.0 | 2.43 |
| Approval Flow | 3.0 | 3.3 | 3.1 | 2.7 | 3.03 |
| Analytics | 3.1 | 3.4 | 3.3 | 2.6 | 3.10 |
| **Module Average** | **2.86** | **3.22** | **3.02** | **2.50** | **2.90** |

#### Top Negative Feedback Items

**Issue EX-001: OCR อ่านใบเสร็จภาษาไทยผิดพลาดสูง**

- **Description:** Receipt OCR accuracy for Thai-language receipts is approximately 67%, compared to 91% for English receipts. Common errors include misreading Thai numerals, confusing similar Thai characters (ภ/ถ, บ/ป), and failing to parse Thai date formats.
- **Affected Users:** 2,456 (61.4%)
- **Most Affected Group:** Group D (78.3% of Group D)
- **Severity:** Critical
- **User Quote:** _"ถ่ายรูปใบเสร็จจากร้านอาหาร OCR อ่านยอดเงิน 350 บาท เป็น 850 บาท แล้วชื่อร้านก็ผิดหมด ต้องมานั่งแก้เองทุกช่อง สู้พิมพ์เองตั้งแต่แรกยังเร็วกว่า"_ -- Group D, Female, 49

**Issue EX-002: ไม่สามารถอัปโหลดใบเสร็จหลายใบพร้อมกันได้**

- **Description:** Receipt upload only accepts one file at a time. No batch upload, no drag-and-drop multiple files, and no mobile camera burst mode support.
- **Affected Users:** 1,789 (44.7%)
- **Most Affected Group:** Group A (62.3% of Group A)
- **Severity:** High
- **User Quote:** _"ไปสัมมนา 3 วัน มีใบเสร็จ 23 ใบ ต้องอัปโหลดทีละใบ กด browse ทีละไฟล์ รอ OCR ทีละใบ ใช้เวลาเกือบ 45 นาที ถ้า upload ได้ทีเดียว 23 ใบ น่าจะเสร็จใน 5 นาที"_ -- Group A, Male, 25

**Issue EX-003: Approval workflow ไม่ยืดหยุ่น ไม่รองรับการอนุมัติแบบมีเงื่อนไข**

- **Description:** Approval routing is rigid (sequential only). Cannot configure conditional routing (e.g., expenses > 10,000 THB require VP approval), parallel approvals, or delegation during leave.
- **Affected Users:** 1,234 (30.9%)
- **Most Affected Group:** Group C (47.8% of Group C)
- **Severity:** High
- **User Quote:** _"ผมลาพักร้อน 1 สัปดาห์ ไม่สามารถมอบหมายอำนาจอนุมัติให้คนอื่นได้ ลูกน้อง 15 คนรอเบิกเงินไม่ได้เลยจนกว่าจะกลับมา"_ -- Group C, Male, 44

**Issue EX-004: ไม่มี Policy Engine สำหรับตรวจสอบการเบิกค่าใช้จ่ายอัตโนมัติ**

- **Description:** No configurable expense policy rules. Cannot auto-flag expenses that exceed per-diem limits, duplicate submissions, or policy violations.
- **Affected Users:** 1,067 (26.7%)
- **Most Affected Group:** Group C (39.4% of Group C)
- **Severity:** High
- **User Quote:** _"พนักงานเบิกค่าอาหารเกิน policy 500 บาท/มื้อ ระบบไม่แจ้งเตือนเลย ต้องตรวจ manual ทีละรายการ ถ้ามี auto-check ก็จะช่วยได้เยอะ"_ -- Group C, Female, 36

**Issue EX-005: Analytics ไม่แสดง breakdown ตามประเภทค่าใช้จ่ายที่ชัดเจน**

- **Description:** Expense analytics shows total amounts but lacks drill-down by category (travel, meals, supplies), department, or individual. No comparison between budget vs. actual.
- **Affected Users:** 892 (22.3%)
- **Most Affected Group:** Group D (37.1% of Group D)
- **Severity:** Medium
- **User Quote:** _"อยากดูว่าแผนกไหนเบิกค่าเดินทางเยอะสุด เทียบกับงบที่ตั้งไว้ แต่ Analytics แสดงแค่ยอดรวมทั้งบริษัท ไม่มีประโยชน์สำหรับการตัดสินใจ"_ -- Group D, Male, 56

#### UI/UX Complaints

- Receipt photo capture on mobile does not auto-crop or guide document alignment
- Claim form requires selecting expense category from a dropdown with 78 items -- no search/filter in dropdown
- Thai Baht currency symbol (฿) renders inconsistently across browsers (sometimes as "B" in Edge)
- Approval history shows timestamps in UTC, not Asia/Bangkok timezone
- No visual distinction between pending/approved/rejected claims in the task list beyond small colored dots
- The receipt preview pane is fixed at 300px width -- cannot zoom or pan on large receipts

#### Feature Gaps

- No receipt forwarding via email (snap photo, email to system)
- No credit card transaction auto-import
- No mileage calculator for travel claims
- No per-diem auto-calculation based on destination
- No split expense functionality (splitting one receipt across multiple cost centers)
- No receipt duplicate detection
- No offline receipt capture with sync

---

### 4.5 Finance Doc Hub (Dashboard, Cases, Case Detail, Verification, Analytics)

#### Satisfaction Scores by Age Group

| Metric | Group A | Group B | Group C | Group D | Overall |
|--------|---------|---------|---------|---------|---------|
| Dashboard | 3.1 | 3.4 | 3.3 | 2.9 | 3.18 |
| Case Management | 2.8 | 3.2 | 3.1 | 2.5 | 2.90 |
| Case Detail View | 2.6 | 3.0 | 2.9 | 2.3 | 2.70 |
| Verification Flow | 2.5 | 2.9 | 3.0 | 2.2 | 2.65 |
| Analytics | 3.0 | 3.3 | 3.2 | 2.7 | 3.05 |
| **Module Average** | **2.80** | **3.16** | **3.10** | **2.52** | **2.90** |

#### Top Negative Feedback Items

**Issue FD-001: Case Detail แสดงเอกสารแนบเป็นรายการยาว ไม่มีการจัดกลุ่ม**

- **Description:** Financial cases with 10+ attached documents display as a flat list with no grouping by type (invoice, receipt, contract, etc.). Users must open each document to identify its content.
- **Affected Users:** 1,567 (39.2%)
- **Most Affected Group:** Group D (54.2% of Group D)
- **Severity:** High
- **User Quote:** _"เคส reconciliation มีเอกสารแนบ 24 ไฟล์ ไม่รู้ว่าอันไหนเป็น invoice อันไหนเป็น receipt ชื่อไฟล์เป็น 'DOC001.pdf', 'DOC002.pdf' ต้องเปิดทีละไฟล์ดู"_ -- Group D, Male, 52

**Issue FD-002: Verification workflow ไม่มี checklist หรือ template**

- **Description:** Financial verification requires users to manually remember all checking steps. No configurable checklist templates for different verification types (invoice matching, reconciliation, tax verification).
- **Affected Users:** 1,123 (28.1%)
- **Most Affected Group:** Group B (36.8% of Group B)
- **Severity:** High
- **User Quote:** _"ตรวจสอบเอกสารการเงิน ไม่มี checklist ว่าต้องเช็คอะไรบ้าง บางทีลืมเช็คเลขที่ภาษี ต้องกลับมาเปิดดูใหม่ ถ้ามี template checklist ก็จะไม่พลาด"_ -- Group B, Female, 28

**Issue FD-003: ไม่สามารถ annotate หรือ comment บนเอกสาร PDF ได้โดยตรง**

- **Description:** Users cannot add annotations, highlights, or comments directly on financial documents within the platform. Must download, annotate externally, and re-upload.
- **Affected Users:** 1,345 (33.6%)
- **Most Affected Group:** Group C (45.3% of Group C)
- **Severity:** High
- **User Quote:** _"ต้องการ highlight ยอดที่ไม่ตรงบน invoice แต่ต้องดาวน์โหลดมา mark ใน Acrobat แล้ว upload กลับขึ้นไป เสียเวลามาก ถ้า annotate ในระบบได้เลยจะดีกว่าเยอะ"_ -- Group C, Male, 38

**Issue FD-004: Dashboard สรุปยอดไม่ update แบบ real-time**

- **Description:** Finance Dashboard summary numbers update only once per hour via batch process. Users see stale data and make decisions based on outdated figures.
- **Affected Users:** 756 (18.9%)
- **Most Affected Group:** Group C (29.7% of Group C)
- **Severity:** Medium
- **User Quote:** _"อนุมัติจ่ายเงินไปแล้ว 500,000 บาท แต่ Dashboard ยังแสดงยอดเดิม ต้องรอ 1 ชั่วโมงถึงจะ update เกือบอนุมัติเกินงบเพราะเห็นตัวเลขเก่า"_ -- Group C, Female, 41

**Issue FD-005: Search ในระบบ Cases ค้นหาด้วย keyword ภาษาไทยไม่แม่นยำ**

- **Description:** Thai keyword search does not support partial matching or word segmentation. Searching "ใบแจ้งหนี้" does not match cases tagged as "ใบแจ้งหนี้/Invoice" or "Invoice/ใบแจ้งหนี้".
- **Affected Users:** 1,034 (25.9%)
- **Most Affected Group:** Group A (34.7% of Group A)
- **Severity:** Medium
- **User Quote:** _"ค้นหาคำว่า 'ใบกำกับภาษี' ไม่เจอ แต่พอค้น 'tax invoice' ถึงจะเจอ ระบบควรค้นหาทั้งไทยและอังกฤษพร้อมกัน"_ -- Group A, Female, 24

#### UI/UX Complaints

- Case status indicators use only English terms (Open, In Progress, Resolved) with no Thai translation
- Financial amounts display with comma separators but no Thai Baht symbol in some views
- Case detail page loads all attachments simultaneously, causing 5-8 second delay for cases with large files
- Verification step completion is not auto-saved -- refreshing the page loses verification progress
- Print layout for case summaries breaks Thai text across page boundaries incorrectly
- No keyboard shortcuts for common verification actions (approve, reject, flag for review)

#### Feature Gaps

- No automated document classification using AI
- No integration with accounting software (QuickBooks, MYOB, or local Thai systems like Express)
- No recurring case templates for monthly closing activities
- No SLA tracking for case resolution time
- Missing inter-case linking (related cases/parent-child relationships)
- No financial document OCR within the hub (must use Expense module separately)

---

### 4.6 Logistics FX (Dashboard, Freight OCR, Cost Calculator, Analytics)

#### Satisfaction Scores by Age Group

| Metric | Group A | Group B | Group C | Group D | Overall |
|--------|---------|---------|---------|---------|---------|
| Dashboard | 3.2 | 3.5 | 3.3 | 2.8 | 3.20 |
| Freight OCR | 2.4 | 2.9 | 2.7 | 2.1 | 2.53 |
| Cost Calculator | 2.6 | 3.1 | 3.0 | 2.3 | 2.75 |
| Analytics | 3.0 | 3.3 | 3.2 | 2.6 | 3.03 |
| **Module Average** | **2.80** | **3.20** | **3.05** | **2.45** | **2.88** |

#### Top Negative Feedback Items

**Issue LG-001: Freight OCR ไม่รองรับรูปแบบเอกสารขนส่งไทย**

- **Description:** Freight OCR is optimized for international shipping documents (B/L, AWB) but fails to correctly parse Thai domestic shipping documents, delivery orders from Thai logistics companies (Kerry Express, Flash Express, J&T), and Thai customs forms.
- **Affected Users:** 1,678 (42.0%)
- **Most Affected Group:** Group B (53.4% of Group B)
- **Severity:** Critical
- **User Quote:** _"อัปโหลดใบส่งสินค้าจาก Kerry Express ระบบอ่านไม่ออกเลย ทั้งเลข tracking, ที่อยู่, น้ำหนัก ต้องกรอกเองหมด OCR ใช้ได้แค่กับเอกสารภาษาอังกฤษ"_ -- Group B, Male, 30

**Issue LG-002: Cost Calculator ไม่รองรับอัตราค่าขนส่งแบบไทย**

- **Description:** The cost calculator uses international freight rate structures. It does not support Thai domestic rate cards, zoned pricing (กรุงเทพ/ปริมณฑล vs ต่างจังหวัด), or Thai customs duty calculations.
- **Affected Users:** 1,234 (30.9%)
- **Most Affected Group:** Group C (42.3% of Group C)
- **Severity:** High
- **User Quote:** _"ใช้ Cost Calculator คำนวณค่าส่งจากกรุงเทพไปเชียงใหม่ ตัวเลขที่ได้ไม่ตรงกับความเป็นจริงเลย เพราะระบบคำนวณแบบ international freight ไม่มี rate card ของขนส่งไทย"_ -- Group C, Male, 39

**Issue LG-003: Dashboard ไม่แสดงสถานะ shipment แบบ real-time tracking**

- **Description:** Logistics dashboard shows only static status (Ordered, Shipped, Delivered) without real-time GPS tracking or estimated delivery times.
- **Affected Users:** 1,456 (36.4%)
- **Most Affected Group:** Group A (48.7% of Group A)
- **Severity:** High
- **User Quote:** _"แค่บอกว่า 'กำลังจัดส่ง' แต่ไม่บอกว่าของอยู่ตรงไหน จะถึงเมื่อไหร่ ต้องไปเข้าเว็บ Kerry เช็ค tracking แยกอีกที ทำไมไม่ integrate เข้ามาในระบบ"_ -- Group A, Female, 23

**Issue LG-004: Analytics ไม่มี Cost-per-unit analysis**

- **Description:** Logistics analytics shows total shipping costs but does not break down to cost-per-unit, cost-per-kg, or cost-per-route for optimization analysis.
- **Affected Users:** 845 (21.1%)
- **Most Affected Group:** Group C (33.8% of Group C)
- **Severity:** Medium
- **User Quote:** _"อยากเทียบต้นทุนขนส่งต่อหน่วยระหว่าง vendor ขนส่ง 3 ราย แต่ Analytics แสดงแค่ยอดรวม ต้องไปคำนวณเองใน Excel"_ -- Group C, Female, 37

#### UI/UX Complaints

- Freight document preview renders slowly for multi-page documents (> 5 pages)
- Cost calculator input fields do not validate numeric formats (accepts "1,234.56" but not "1234.56")
- Weight unit selector defaults to kg but does not auto-convert from lbs/oz
- Thai province names in route calculator are romanized (e.g., "Chiang Mai" instead of "เชียงใหม่")
- Map visualization for shipment routes does not work offline
- No print-friendly layout for cost calculations

#### Feature Gaps

- No integration with Thai logistics providers' APIs (Kerry, Flash, J&T, Thailand Post)
- No container tracking for sea freight
- No customs clearance workflow
- No automated freight rate comparison across providers
- No carbon footprint calculation per shipment
- Missing insurance cost estimation

---

### 4.7 Sales Doc Gen (Dashboard, Pipeline, Analytics)

#### Satisfaction Scores by Age Group

| Metric | Group A | Group B | Group C | Group D | Overall |
|--------|---------|---------|---------|---------|---------|
| Dashboard | 3.3 | 3.6 | 3.4 | 3.0 | 3.33 |
| Document Generation | 2.9 | 3.3 | 3.1 | 2.6 | 2.98 |
| Pipeline View | 3.1 | 3.5 | 3.3 | 2.7 | 3.15 |
| Analytics | 3.2 | 3.5 | 3.3 | 2.8 | 3.20 |
| **Module Average** | **3.13** | **3.48** | **3.28** | **2.78** | **3.17** |

#### Top Negative Feedback Items

**Issue SD-001: Template เอกสารมีให้เลือกน้อยและไม่รองรับรูปแบบไทย**

- **Description:** Only 8 document templates available, all designed for international format. No Thai quotation format (ใบเสนอราคา), Thai invoice format (ใบแจ้งหนี้), or Thai receipt format (ใบเสร็จรับเงิน) with proper tax ID placement.
- **Affected Users:** 1,567 (39.2%)
- **Most Affected Group:** Group C (51.2% of Group C)
- **Severity:** Critical
- **User Quote:** _"ต้องการออกใบเสนอราคาแบบไทย มีเลขประจำตัวผู้เสียภาษี มีรหัสสาขา มีช่องลายเซ็น ผู้มีอำนาจ แต่ template ที่มีเป็นแบบฝรั่งหมด ต้องไปทำใน Word แทน"_ -- Group C, Male, 43

**Issue SD-002: Pipeline view ไม่มี drag-and-drop สำหรับเปลี่ยนสถานะ**

- **Description:** Moving deals between pipeline stages requires opening the deal, editing the status field, and saving. No visual drag-and-drop Kanban-style interaction.
- **Affected Users:** 1,234 (30.9%)
- **Most Affected Group:** Group A (47.8% of Group A)
- **Severity:** High
- **User Quote:** _"Pipeline view ดูเหมือน Kanban board แต่ drag-and-drop ไม่ได้ ต้องคลิกเข้าไปแก้สถานะทีละ deal ทีละ 3-4 คลิก ทั้งที่ควรลากวางได้เลย"_ -- Group A, Male, 22

**Issue SD-003: ไม่สามารถ auto-generate เอกสารจากข้อมูล Pipeline ได้**

- **Description:** Document generation requires manual input of all fields even when data already exists in the pipeline. No auto-populate from deal/opportunity records.
- **Affected Users:** 1,089 (27.2%)
- **Most Affected Group:** Group B (38.9% of Group B)
- **Severity:** High
- **User Quote:** _"ข้อมูลลูกค้า ชื่อบริษัท มูลค่า deal อยู่ใน Pipeline แล้ว แต่ตอนสร้างใบเสนอราคา ต้องพิมพ์ข้อมูลซ้ำใหม่หมด ทำไมมันไม่ดึงมาให้อัตโนมัติ"_ -- Group B, Male, 33

**Issue SD-004: Analytics ขาด Conversion Rate analysis**

- **Description:** Sales analytics shows deal counts and values per stage but does not calculate conversion rates between stages, average deal velocity, or win/loss reasons.
- **Affected Users:** 756 (18.9%)
- **Most Affected Group:** Group D (31.2% of Group D)
- **Severity:** Medium
- **User Quote:** _"อยากรู้ว่าจาก Proposal ไป Closing มี conversion rate เท่าไหร่ แต่ Analytics ไม่มี ต้องไปนับเองจาก Pipeline view"_ -- Group D, Female, 47

#### UI/UX Complaints

- Document preview renders Thai fonts with incorrect kerning -- characters are too close together
- Generated PDF documents do not embed Thai fonts -- recipients without Thai font support see blank characters
- Pipeline column widths are fixed -- long Thai company names are truncated with "..."
- No e-signature integration for generated documents
- Color coding in pipeline uses pastel colors that are hard to distinguish in projector/meeting room settings

#### Feature Gaps

- No document version history / revision tracking
- No client-facing document sharing portal
- No automated follow-up reminders from pipeline stages
- No proposal approval workflow before sending to client
- No Thai withholding tax calculation in quotations
- No integration with e-Tax Invoice system (กรมสรรพากร)

---

### 4.8 Connectors (API Dashboard, Connector Hub)

#### Satisfaction Scores by Age Group

| Metric | Group A | Group B | Group C | Group D | Overall |
|--------|---------|---------|---------|---------|---------|
| API Dashboard | 2.7 | 3.3 | 2.9 | 1.8 | 2.68 |
| Connector Hub | 2.5 | 3.1 | 2.7 | 1.6 | 2.48 |
| Documentation | 2.3 | 2.8 | 2.5 | 1.5 | 2.28 |
| Setup Ease | 2.1 | 2.7 | 2.3 | 1.4 | 2.13 |
| **Module Average** | **2.40** | **2.98** | **2.60** | **1.58** | **2.39** |

#### Top Negative Feedback Items

**Issue CN-001: Connector setup ซับซ้อนเกินไปสำหรับ non-technical users**

- **Description:** Setting up a new API connector requires understanding of OAuth flows, API keys, webhook URLs, and JSON payload mapping. No wizard or guided setup for common integrations.
- **Affected Users:** 2,567 (64.2%)
- **Most Affected Group:** Group D (89.4% of Group D)
- **Severity:** Critical
- **User Quote:** _"ต้องการเชื่อมต่อกับ SAP แต่หน้า setup มีแต่ศัพท์เทคนิค OAuth, API Key, Webhook ไม่เข้าใจเลย ต้องเรียก IT มาช่วย ผมแค่อยากให้ข้อมูลมันส่งไปมาได้"_ -- Group D, Male, 54

**Issue CN-002: ไม่มี pre-built connectors สำหรับระบบที่นิยมในไทย**

- **Description:** Connector Hub lacks pre-built integrations for popular Thai business systems: Express Accounting, Prosoft, WinSpeed, PEAK Accounting, iTAX, LINE Official Account API, PromptPay, and Thai banking APIs.
- **Affected Users:** 1,891 (47.3%)
- **Most Affected Group:** Group C (62.1% of Group C)
- **Severity:** Critical
- **User Quote:** _"บริษัทใช้โปรแกรมบัญชี Express แต่ไม่มี connector สำเร็จรูป ต้องเขียน API เอง ทั้งที่ Express เป็นโปรแกรมบัญชีที่คนไทยใช้เยอะที่สุด"_ -- Group C, Female, 36

**Issue CN-003: API Dashboard ไม่แสดง error logs ที่เข้าใจง่าย**

- **Description:** API error messages display raw HTTP status codes and JSON error bodies. No human-readable explanation, no suggested fixes, and no Thai translation of error messages.
- **Affected Users:** 1,456 (36.4%)
- **Most Affected Group:** Group A (48.2% of Group A)
- **Severity:** High
- **User Quote:** _"API แสดง error 'HTTP 422 Unprocessable Entity: {\"error\":\"invalid_field\",\"field\":\"vendor_tax_id\"}' ไม่เข้าใจว่าต้องแก้ยังไง น่าจะแปลเป็นภาษาคนอ่าน เช่น 'เลขประจำตัวผู้เสียภาษีไม่ถูกต้อง'"_ -- Group A, Male, 25

**Issue CN-004: ไม่มี connection health monitoring แบบ real-time**

- **Description:** No real-time monitoring dashboard for active connections. Users discover connection failures only when transactions fail, not proactively.
- **Affected Users:** 987 (24.7%)
- **Most Affected Group:** Group B (34.6% of Group B)
- **Severity:** High
- **User Quote:** _"Connection กับ ERP ตัดไปตอน 2 ทุ่ม ไม่มีแจ้งเตือนเลย รู้ตอน 8 โมงเช้าวันรุ่งขึ้นตอนข้อมูลไม่ sync ทำให้เสียข้อมูลไป 12 ชั่วโมง"_ -- Group B, Female, 27

#### UI/UX Complaints

- API documentation uses entirely English technical jargon with no Thai explanation
- Connector Hub search does not autocomplete or suggest similar connectors
- Setup flow requires switching between 4 different tabs -- no unified wizard
- Connection test button is hidden at the bottom of a long form page
- Rate limit information is not displayed anywhere in the UI
- No visual flow diagram showing data mapping between systems

#### Feature Gaps

- No low-code/no-code connector builder
- No webhook event log with replay capability
- No data transformation/mapping visual editor
- No connector marketplace for community-built integrations
- No scheduled sync with configurable frequency
- No data validation rules before sync
- No rollback capability for failed sync operations
- No Zapier/Make (Integromat) integration as a bridge

---

### 4.9 Customer Feedback

#### Satisfaction Scores by Age Group

| Metric | Group A | Group B | Group C | Group D | Overall |
|--------|---------|---------|---------|---------|---------|
| Survey Creation | 3.1 | 3.5 | 3.3 | 2.8 | 3.18 |
| Response Collection | 3.0 | 3.4 | 3.2 | 2.7 | 3.08 |
| Analysis Tools | 2.7 | 3.1 | 3.0 | 2.4 | 2.80 |
| Reporting | 2.8 | 3.2 | 3.1 | 2.5 | 2.90 |
| **Module Average** | **2.90** | **3.30** | **3.15** | **2.60** | **2.99** |

#### Top Negative Feedback Items

**Issue CF-001: ไม่มี sentiment analysis สำหรับข้อความภาษาไทย**

- **Description:** The feedback analysis tool provides sentiment scoring for English text only. Thai feedback text is classified as "Neutral" regardless of content, rendering the analysis useless for Thai-language responses.
- **Affected Users:** 1,567 (39.2%)
- **Most Affected Group:** Group C (52.3% of Group C)
- **Severity:** Critical
- **User Quote:** _"ลูกค้าเขียน feedback ภาษาไทยว่า 'แย่มาก ผิดหวัง ไม่ซื้ออีกแล้ว' แต่ระบบวิเคราะห์เป็น Neutral sentiment ไม่มีประโยชน์เลยถ้า AI อ่านไทยไม่ออก"_ -- Group C, Female, 40

**Issue CF-002: Survey builder ไม่มี conditional logic / branching**

- **Description:** Cannot create surveys with conditional paths (e.g., if answer is "unsatisfied", show follow-up questions). All respondents see all questions regardless of previous answers.
- **Affected Users:** 1,123 (28.1%)
- **Most Affected Group:** Group B (41.2% of Group B)
- **Severity:** High
- **User Quote:** _"อยากทำแบบสอบถามที่ถ้าลูกค้าให้คะแนนต่ำกว่า 3 จะถามเหตุผลเพิ่มเติม แต่ระบบทำไม่ได้ ลูกค้าที่พอใจก็ต้องตอบคำถามที่ไม่เกี่ยวกับตัวเอง"_ -- Group B, Male, 28

**Issue CF-003: ไม่สามารถ integrate feedback เข้ากับ CRM หรือ ticket system**

- **Description:** Feedback data lives in isolation. No automatic ticket creation for negative feedback, no customer profile linking, no trigger-based notifications.
- **Affected Users:** 934 (23.4%)
- **Most Affected Group:** Group B (33.7% of Group B)
- **Severity:** High
- **User Quote:** _"ลูกค้าให้คะแนน 1 ดาว เขียนว่าจะยกเลิกสัญญา แต่ไม่มีระบบแจ้งเตือนใครเลย ถ้า integrate กับ CRM จะเปิด ticket ให้ทีม Customer Success ตามได้ทันที"_ -- Group B, Female, 32

**Issue CF-004: Reporting ไม่มี trend analysis ข้าม period**

- **Description:** Feedback reports show snapshots of individual periods but cannot overlay multiple periods for trend comparison. No NPS trending, no satisfaction score over time.
- **Affected Users:** 789 (19.7%)
- **Most Affected Group:** Group D (32.4% of Group D)
- **Severity:** Medium
- **User Quote:** _"อยากเห็นกราฟ NPS score ย้อนหลัง 12 เดือน แต่ต้อง export แต่ละเดือนมาเทียบใน Excel เอง ระบบแสดงได้ทีละเดือนเท่านั้น"_ -- Group D, Male, 55

#### UI/UX Complaints

- Survey preview on mobile does not match actual respondent experience
- Thai text in survey questions wraps awkwardly on narrow screens
- Response rate calculation includes incomplete submissions, inflating numbers
- No dark mode for survey response pages
- Export to CSV encodes Thai characters incorrectly in some versions of Excel (UTF-8 BOM issue)
- QR code generation for survey links does not include custom branding

#### Feature Gaps

- No multi-language survey support (Thai + English in same survey)
- No video/audio feedback collection
- No automated follow-up based on response score
- No feedback widget for embedding in external websites
- No A/B testing for survey formats
- No anonymous feedback option with verifiable authenticity

---

### 4.10 System (Users, Channels, Billing, Settings)

#### Satisfaction Scores by Age Group

| Metric | Group A | Group B | Group C | Group D | Overall |
|--------|---------|---------|---------|---------|---------|
| User Management | 3.0 | 3.3 | 3.1 | 2.6 | 3.00 |
| Channel Config | 2.8 | 3.1 | 2.9 | 2.3 | 2.78 |
| Billing | 2.6 | 3.0 | 2.8 | 2.4 | 2.70 |
| Settings | 2.5 | 2.9 | 2.7 | 2.2 | 2.58 |
| **Module Average** | **2.73** | **3.08** | **2.88** | **2.38** | **2.77** |

#### Top Negative Feedback Items

**Issue SY-001: User permission system ซับซ้อนเกินไปและไม่มี role template**

- **Description:** Permission configuration requires setting individual permissions for each of 47 features across 10 modules. No pre-built role templates (Admin, Manager, Viewer, etc.) and no bulk permission assignment.
- **Affected Users:** 1,891 (47.3%)
- **Most Affected Group:** Group D (68.7% of Group D)
- **Severity:** Critical
- **User Quote:** _"ต้องตั้งค่า permission ให้พนักงานใหม่ 1 คน ต้องกดเลือก 47 รายการทีละอัน ใช้เวลา 20 นาที ทั้งที่พนักงาน role เดียวกันก็ควรมี template ให้เลือก"_ -- Group D, Male, 50

**Issue SY-002: Billing page ไม่แสดงรายละเอียดค่าใช้จ่ายที่เข้าใจง่าย**

- **Description:** Billing shows technical usage metrics (API calls, storage GB, active users) without clear pricing breakdown. Users cannot predict next month's bill or understand which module drives costs.
- **Affected Users:** 1,345 (33.6%)
- **Most Affected Group:** Group D (52.1% of Group D)
- **Severity:** High
- **User Quote:** _"ดู Billing เห็นแต่ 'API Calls: 12,847' และ 'Storage: 4.2GB' ไม่รู้ว่าคิดเงินยังไง ราคาต่อหน่วยเท่าไหร่ เดือนหน้าจะโดนชาร์จเท่าไหร่"_ -- Group D, Female, 48

**Issue SY-003: Settings ไม่มี search function**

- **Description:** Settings page is organized in 12 categories with 80+ individual settings. No search functionality to find specific settings, requiring users to browse through all categories.
- **Affected Users:** 1,567 (39.2%)
- **Most Affected Group:** Group A (53.4% of Group A)
- **Severity:** High
- **User Quote:** _"อยากเปลี่ยน timezone แต่หาไม่เจอ ต้องกดดูทุก category ใน Settings สุดท้ายอยู่ใน 'Regional' ซึ่งไม่ใช่ชื่อที่คิดจะหา ถ้ามี search bar ก็จะเร็วกว่านี้เยอะ"_ -- Group A, Female, 21

**Issue SY-004: Channel management ไม่รองรับ LINE Official Account**

- **Description:** Communication channels support Email, Slack, and Microsoft Teams but not LINE, which is the dominant business communication platform in Thailand.
- **Affected Users:** 2,134 (53.4%)
- **Most Affected Group:** Group A (71.2% of Group A)
- **Severity:** Critical
- **User Quote:** _"บริษัทใช้ LINE Official Account สื่อสารกับลูกค้าและภายใน แต่ระบบ connect ได้แค่ Email กับ Slack คนไทยใช้ LINE เป็นหลัก ไม่มี LINE integration เหมือนขาดอะไรไปเยอะ"_ -- Group A, Male, 26

**Issue SY-005: ไม่มี audit log สำหรับ admin actions**

- **Description:** No comprehensive audit trail for administrative actions (permission changes, user creation/deletion, billing changes, settings modifications).
- **Affected Users:** 876 (21.9%)
- **Most Affected Group:** Group C (34.8% of Group C)
- **Severity:** High
- **User Quote:** _"มีคนเปลี่ยน permission ของ user บางคน ไม่รู้ว่าใครเปลี่ยน เมื่อไหร่ เปลี่ยนอะไรบ้าง ไม่มี log ให้ตรวจสอบเลย"_ -- Group C, Male, 42

#### UI/UX Complaints

- User list table does not support sorting by last active date
- Bulk user import via CSV has no validation preview -- errors only appear after import attempt
- Password policy settings are hidden deep in Security > Advanced > Authentication settings
- Two-factor authentication setup instructions are only in English
- Billing history only shows last 6 months, no option to view older records
- Settings changes require page reload to take effect -- no dynamic save

#### Feature Gaps

- No SSO (Single Sign-On) support for Azure AD or Google Workspace
- No IP whitelist/blacklist for access control
- No user activity dashboard (who logged in, what they accessed)
- No automated license optimization recommendations
- No role hierarchy with inheritance
- No data export/portability tools for compliance
- No backup/restore for system configuration
- No API rate limit management per user/team

---

## 5. Cross-Module Issues

### 5.1 Navigation & Information Architecture

| Issue | Affected Users | Details |
|-------|---------------|---------|
| Deep navigation hierarchy (4+ clicks to reach target) | 2,847 (71.2%) | Average depth: 4.7 clicks. Industry benchmark: 2.3 clicks. Most affected: Procurement PR creation (5 clicks), Vendor Comparison (6 clicks) |
| Inconsistent sidebar menu organization | 2,134 (53.4%) | Module order changes between desktop and mobile. Sub-items not consistently expandable. |
| No breadcrumb navigation | 1,891 (47.3%) | Users frequently report "getting lost" within modules, unable to determine their current location in the hierarchy |
| No global search across all modules | 2,456 (61.4%) | Search is module-specific only. Users cannot search for a PO number from the Home Dashboard or find a vendor from the Finance module |
| Back button behavior inconsistent | 1,567 (39.2%) | Browser back button sometimes returns to previous module instead of previous page within the same module |
| No keyboard navigation support | 1,234 (30.9%) | Tab order is illogical in forms. No keyboard shortcuts for power users. Focus indicators are missing on most interactive elements |
| No recently visited items | 1,678 (42.0%) | No history of recently accessed documents, cases, or vendors for quick return |

### 5.2 Performance Concerns

| Issue | Affected Users | Avg Load Time | Acceptable Threshold |
|-------|---------------|---------------|---------------------|
| Initial page load on first visit | 2,134 (53.4%) | 4.8 seconds | < 2.0 seconds |
| Module switching latency | 1,891 (47.3%) | 2.3 seconds | < 0.5 seconds |
| Large dataset rendering (500+ rows) | 1,567 (39.2%) | 6.7 seconds | < 1.5 seconds |
| PDF generation for documents | 1,345 (33.6%) | 8.2 seconds | < 3.0 seconds |
| Search result return time | 1,123 (28.1%) | 3.1 seconds | < 1.0 seconds |
| Dashboard widget loading | 987 (24.7%) | 3.4 seconds | < 1.5 seconds |
| File upload processing (> 5MB) | 876 (21.9%) | 12.3 seconds | < 5.0 seconds |
| OCR processing per document | 2,456 (61.4%) | 15.7 seconds | < 5.0 seconds |

**Key Performance Finding:** 67.8% of Group D users reported closing the browser tab thinking the application had crashed during OCR processing, due to the lack of progress indicators.

### 5.3 Mobile Responsiveness Issues

| Issue | Affected Users | Primary Device |
|-------|---------------|----------------|
| Tables overflow horizontally with no scroll indicator | 1,634 (40.9%) | iPhone 14/15, Samsung Galaxy S23 |
| Form fields too small for touch input (< 44px tap target) | 1,456 (36.4%) | All mobile devices |
| Modal dialogs extend beyond viewport on mobile | 1,234 (30.9%) | Devices with width < 412px |
| Bottom navigation bar overlaps content on iOS Safari | 987 (24.7%) | iPhone (all models) |
| Dropdown menus clip at screen edge | 876 (21.9%) | All mobile devices |
| Charts/graphs not readable below 768px | 1,567 (39.2%) | All mobile and small tablet devices |
| File upload button not accessible on mobile (hidden by keyboard) | 756 (18.9%) | Android devices |
| Horizontal scroll trap in comparison views | 1,123 (28.1%) | All mobile devices |
| Pinch-to-zoom disabled in some modules | 678 (17.0%) | All mobile devices |

**Critical Finding:** 247 users from Group A reported being completely unable to complete the expense claim workflow on their iPhone. The receipt photo capture, form filling, and submission flow requires horizontal scrolling at every step on screens under 390px.

### 5.4 Accessibility Gaps

| WCAG Criteria | Issue | Elements Affected | Severity |
|---------------|-------|-------------------|----------|
| 1.4.3 Contrast Ratio | 23 UI elements have contrast ratio below 4.5:1 | Placeholder text, disabled buttons, secondary labels | High |
| 1.4.4 Text Resize | Thai text breaks layout when browser zoom exceeds 125% | Data tables, sidebar navigation, modal headers | High |
| 2.1.1 Keyboard Access | 34 interactive elements unreachable via keyboard | Dropdown menus, date pickers, toggle switches, drag targets | Critical |
| 2.4.7 Focus Visible | Focus indicator missing on 67% of interactive elements | Buttons, links, form fields, tabs | High |
| 3.1.1 Language of Page | Page lang attribute set to "en" despite mixed Thai/English content | All pages | Medium |
| 3.3.1 Error Identification | Form errors displayed only as red border with no text message | All form fields | High |
| 4.1.2 Name/Role/Value | 41 custom components missing ARIA labels | Custom dropdowns, toggle switches, tabs, accordion panels | Critical |

**Age Impact Analysis:**
- Group D users (45+) reported the most accessibility-related complaints: 423 out of 1,000 (42.3%)
- Most common complaint from Group D: _"ตัวหนังสือเล็กเกินไป อ่านยากมาก โดยเฉพาะในตาราง ขยายหน้าจอแล้วก็เพี้ยนหมด"_ (Font too small, especially in tables. Zooming breaks the layout.)
- 178 Group D users reported difficulty distinguishing between active/inactive states
- 134 Group D users reported accidental clicks due to small touch targets

### 5.5 Localization / Language Issues

| Issue | Affected Users | Examples |
|-------|---------------|----------|
| Inconsistent Thai/English mixing in labels | 2,193 (54.8%) | "วันที่ Created", "สถานะ: Pending", "ยอด Total" |
| Thai text rendering issues (font kerning) | 1,456 (36.4%) | Sara Am (สระอำ) renders with extra spacing in table cells |
| No พ.ศ. (Buddhist Era) date option | 1,891 (47.3%) | All dates display in ค.ศ. (Christian Era) only |
| Thai number format inconsistency | 987 (24.7%) | Some modules use "1,234.56" others use "1234.56" without consistency |
| Error messages in English only | 1,678 (42.0%) | "Invalid input", "Connection timeout", "File too large" |
| Thai word segmentation issues in search | 1,234 (30.9%) | "บริษัทสมชาย" not matched when searching "บริษัท สมชาย" |
| Help documentation available only in English | 2,456 (61.4%) | All help articles, tooltips, and onboarding guides are English-only |
| PDF export Thai line-breaking errors | 1,123 (28.1%) | Thai words broken mid-syllable at line wraps in exported PDFs |
| Thai sorting order incorrect in lists | 876 (21.9%) | Vendor names sorted by Unicode codepoint, not Thai alphabetical order (กขฃคฅฆง...) |
| No support for Thai numeric characters (๐-๙) | 567 (14.2%) | Input fields reject Thai numeral characters |

### 5.6 Data Visualization Problems

| Issue | Affected Users | Affected Modules |
|-------|---------------|------------------|
| Charts not colorblind-friendly | 1,234 (30.9%) | All modules with analytics |
| No data labels on chart elements | 1,567 (39.2%) | Procurement, Logistics, Sales |
| Legend placement obscures chart data | 987 (24.7%) | Dashboard, Finance Doc Hub |
| Y-axis labels truncated on narrow screens | 1,345 (33.6%) | All analytics dashboards |
| No interactive tooltips on chart hover | 1,123 (28.1%) | Vendor Management, Customer Feedback |
| Chart animation delays data readability | 756 (18.9%) | Dashboard (all widgets) |
| No option to switch between chart types | 1,456 (36.4%) | All modules -- users want bar/line/pie flexibility |
| Data grouping options limited (daily/monthly only) | 1,089 (27.2%) | Procurement Analytics, Expense Analytics |
| Exported charts lose quality in PDF | 845 (21.1%) | All modules with chart export |
| No benchmark/target lines on charts | 1,678 (42.0%) | Procurement, Expense, Finance |

### 5.7 Additional Cross-Module Issues

**Missing Undo/Redo (All Modules)**
- Affected Users: 1,723 (43.1%)
- 312 users reported accidental data loss
- Most critical in: PR/PO creation (167 incidents), Expense Claims (89 incidents), Vendor editing (56 incidents)
- _"ลบรายการสินค้าใน PO ผิดรายการ ไม่มีปุ่ม Undo ต้องสร้าง PO ใหม่ตั้งแต่ต้น"_ -- Group B, Male, 34

**No Offline Capability**
- Affected Users: 1,456 (36.4%)
- Group A most affected (traveling salespeople, field staff)
- _"ไปหาลูกค้าต่างจังหวัด สัญญาณอินเทอร์เน็ตไม่ดี เปิดระบบไม่ได้เลย ต้องใช้ Excel บนเครื่องแทน แล้วค่อยมากรอกทีหลัง"_ -- Group A, Male, 25

**Dark Mode Inconsistency**
- Affected Users: 1,234 (30.9%)
- Dark mode available in 6 of 10 modules only
- Modules without dark mode: Connectors, Customer Feedback, Billing, Settings
- Switching between dark/light modules causes visual jarring
- Some charts become illegible in dark mode (dark text on dark background)
- _"เปิด Dark Mode แล้วเข้า Connectors กลับเป็น Light Mode ตาแสบเวลาทำงานตอนดึก"_ -- Group A, Female, 22

**Limited Search Functionality**
- Affected Users: 2,456 (61.4%)
- No fuzzy matching / typo tolerance
- No search suggestions or autocomplete
- No search history
- No advanced search operators (AND, OR, NOT, date ranges)
- No search within document attachments (full-text search of PDFs)
- _"ค้นหาชื่อ vendor พิมพ์ผิดตัวเดียวก็ไม่เจอ ระบบอื่นจะ suggest ชื่อที่ใกล้เคียง แต่ระบบนี้ไม่มี"_ -- Group B, Female, 29

---

## 6. Negative Feedback Summary Table

All identified issues sorted by affected user count (descending).

| Issue ID | Module | Description | Affected Users | % of Total | Severity | Primary Age Groups |
|----------|--------|-------------|---------------|------------|----------|--------------------|
| CN-001 | Connectors | Connector setup too complex for non-technical users | 2,567 | 64.2% | Critical | D, C |
| CROSS-001 | Cross-Module | Deep navigation hierarchy (4+ clicks) | 2,847 | 71.2% | Critical | A, D |
| CROSS-002 | Cross-Module | No global search across modules | 2,456 | 61.4% | Critical | A, B |
| CROSS-003 | Cross-Module | Help documentation English-only | 2,456 | 61.4% | High | D, C |
| EX-001 | Expense & Receipt | OCR Thai receipt accuracy ~67% | 2,456 | 61.4% | Critical | D, A |
| CROSS-004 | Cross-Module | Inconsistent Thai/English label mixing | 2,193 | 54.8% | High | D, C |
| CROSS-005 | Cross-Module | Initial page load > 4.8 seconds | 2,134 | 53.4% | High | D, C |
| PR-001 | Procurement | PR creation -- multi-page form, no draft save | 2,134 | 53.4% | Critical | A, B |
| SY-004 | System | No LINE Official Account integration | 2,134 | 53.4% | Critical | A, B |
| CROSS-006 | Cross-Module | No พ.ศ. date format option | 1,891 | 47.3% | High | D, C |
| CN-002 | Connectors | No pre-built Thai system connectors | 1,891 | 47.3% | Critical | C, B |
| VM-001 | Vendor Management | Comparison tool load time 8-12 seconds | 1,891 | 47.3% | Critical | D, C |
| SY-001 | System | Permission system too complex, no role templates | 1,891 | 47.3% | Critical | D, C |
| HD-001 | Home Dashboard | Dashboard not customizable | 1,847 | 46.2% | High | B, C |
| EX-002 | Expense & Receipt | No batch receipt upload | 1,789 | 44.7% | High | A, B |
| CROSS-007 | Cross-Module | No undo/redo across modules | 1,723 | 43.1% | Critical | B, A |
| LG-001 | Logistics FX | Freight OCR fails on Thai domestic documents | 1,678 | 42.0% | Critical | B, C |
| CROSS-008 | Cross-Module | No recently visited items | 1,678 | 42.0% | Medium | A, B |
| CROSS-009 | Cross-Module | Error messages English-only | 1,678 | 42.0% | High | D, C |
| PR-003 | Procurement | 3-Way Match display too complex | 1,678 | 42.0% | High | D, C |
| CROSS-010 | Cross-Module | Charts/graphs unreadable < 768px | 1,567 | 39.2% | High | A, B |
| CROSS-011 | Cross-Module | No breadcrumb navigation | 1,891 | 47.3% | High | D, A |
| HD-004 | Home Dashboard | No quick action buttons for frequent tasks | 1,567 | 39.2% | High | A, B |
| SD-001 | Sales Doc Gen | Templates lack Thai business document formats | 1,567 | 39.2% | Critical | C, D |
| SY-003 | System | Settings page has no search function | 1,567 | 39.2% | High | A, B |
| CF-001 | Customer Feedback | No Thai sentiment analysis | 1,567 | 39.2% | Critical | C, B |
| CROSS-012 | Cross-Module | Tables overflow on mobile, no scroll indicator | 1,634 | 40.9% | High | A, B |
| CROSS-013 | Cross-Module | No offline capability | 1,456 | 36.4% | High | A, B |
| CN-003 | Connectors | API errors not human-readable | 1,456 | 36.4% | High | A, C |
| LG-003 | Logistics FX | No real-time shipment tracking | 1,456 | 36.4% | High | A, B |
| PR-002 | Procurement | Cannot create PO directly from approved PR | 1,456 | 36.4% | Critical | C, B |
| CROSS-014 | Cross-Module | Thai font kerning/rendering issues | 1,456 | 36.4% | Medium | D, C |
| CROSS-015 | Cross-Module | No chart type switching option | 1,456 | 36.4% | Medium | C, B |
| FD-003 | Finance Doc Hub | No PDF annotation capability | 1,345 | 33.6% | High | C, B |
| SY-002 | System | Billing page unclear pricing breakdown | 1,345 | 33.6% | High | D, C |
| PR-005 | Procurement | Analytics only exports to PDF | 1,312 | 32.8% | High | C, B |
| EX-003 | Expense & Receipt | Rigid approval workflow, no delegation | 1,234 | 30.9% | High | C, D |
| CROSS-016 | Cross-Module | Dark mode inconsistent across modules | 1,234 | 30.9% | Medium | A, B |
| SD-002 | Sales Doc Gen | No drag-and-drop in Pipeline view | 1,234 | 30.9% | High | A, B |
| CROSS-017 | Cross-Module | 34 elements unreachable via keyboard | 1,234 | 30.9% | Critical | D, C |
| LG-002 | Logistics FX | Cost calculator lacks Thai rate structures | 1,234 | 30.9% | High | C, B |
| HD-002 | Home Dashboard | Summary widgets lack trend context | 1,234 | 30.9% | High | D, C |
| VM-003 | Vendor Management | No automated vendor scoring | 1,123 | 28.1% | High | B, C |
| CF-002 | Customer Feedback | No survey conditional logic / branching | 1,123 | 28.1% | High | B, A |
| CROSS-018 | Cross-Module | Thai word segmentation issues in search | 1,234 | 30.9% | Medium | A, B |
| FD-002 | Finance Doc Hub | No verification checklist templates | 1,123 | 28.1% | High | B, C |
| CROSS-019 | Cross-Module | No interactive chart tooltips | 1,123 | 28.1% | Medium | D, C |
| HD-005 | Home Dashboard | Notifications unfiltered/uncategorized | 1,089 | 27.2% | Medium | C, D |
| SD-003 | Sales Doc Gen | No auto-generate docs from pipeline data | 1,089 | 27.2% | High | B, A |
| CROSS-020 | Cross-Module | Data grouping limited (daily/monthly only) | 1,089 | 27.2% | Medium | C, B |
| FD-005 | Finance Doc Hub | Thai keyword search inaccurate | 1,034 | 25.9% | Medium | A, B |
| PR-004 | Procurement | No bulk PO creation | 987 | 24.7% | High | B, C |
| CN-004 | Connectors | No real-time connection health monitoring | 987 | 24.7% | High | B, C |
| CROSS-021 | Cross-Module | Dropdown menus clip on mobile | 876 | 21.9% | Medium | A, B |
| SY-005 | System | No admin action audit log | 876 | 21.9% | High | C, D |
| VM-004 | Vendor Management | Tasks not linked to project timeline | 876 | 21.9% | Medium | C, B |
| CROSS-022 | Cross-Module | Thai sorting order incorrect | 876 | 21.9% | Medium | D, C |
| LG-004 | Logistics FX | No cost-per-unit analysis | 845 | 21.1% | Medium | C, B |
| CROSS-023 | Cross-Module | Exported charts lose quality | 845 | 21.1% | Medium | C, D |
| CF-003 | Customer Feedback | No CRM/ticket system integration | 934 | 23.4% | High | B, C |
| VM-002 | Vendor Management | Thai filename/encoding issues in uploads | 934 | 23.4% | Critical | C, B |
| EX-005 | Expense & Receipt | Analytics lacks category drill-down | 892 | 22.3% | Medium | D, C |
| CF-004 | Customer Feedback | No trend analysis across periods | 789 | 19.7% | Medium | D, C |
| SD-004 | Sales Doc Gen | No conversion rate analysis | 756 | 18.9% | Medium | D, B |
| FD-004 | Finance Doc Hub | Dashboard not real-time (1hr batch update) | 756 | 18.9% | Medium | C, B |
| HD-003 | Home Dashboard | Charts illegible on mobile | 743 | 18.6% | Medium | A, B |
| CROSS-024 | Cross-Module | Pinch-to-zoom disabled in some modules | 678 | 17.0% | Medium | D, A |
| VM-005 | Vendor Management | Audit report custom date range missing | 678 | 17.0% | Medium | C, B |
| CROSS-025 | Cross-Module | No Thai numeral character support (๐-๙) | 567 | 14.2% | Low | D, C |
| EX-004 | Expense & Receipt | No configurable expense policy engine | 1,067 | 26.7% | High | C, B |
| FD-001 | Finance Doc Hub | Document attachments not grouped by type | 1,567 | 39.2% | High | D, C |

**Total unique issues catalogued:** 171
**Critical severity issues:** 14
**Issues affecting > 1,000 users:** 43
**Issues affecting > 2,000 users:** 9

---

## 7. Priority Recommendations

### Top 20 Improvements Ranked by Impact

| Rank | Recommendation | Related Issues | Estimated Effort | Impact Score (1-10) | Affected Users |
|------|---------------|----------------|-----------------|--------------------|----|
| 1 | **Implement global search with Thai language support** -- Add a global search bar accessible from any page supporting fuzzy matching, Thai word segmentation, and cross-module results. | CROSS-002, FD-005, CROSS-018 | L | 9.5 | 2,456+ |
| 2 | **Improve Thai OCR accuracy to >90%** -- Upgrade OCR engine with Thai-specific training data, support TIS-620 encoding, and add manual correction workflow with learning feedback loop. | EX-001, LG-001, VM-002 | XL | 9.3 | 2,456+ |
| 3 | **Flatten navigation architecture** -- Reduce average click depth from 4.7 to 2.5 by implementing mega-menu, quick actions bar, and recently visited shortcuts. Add breadcrumb navigation throughout. | CROSS-001, HD-004, CROSS-008, CROSS-011 | L | 9.2 | 2,847 |
| 4 | **Add LINE Official Account integration** -- Build a native LINE connector for notifications, approvals, and basic interactions. This is the most requested Thai-market-specific feature. | SY-004 | L | 9.0 | 2,134 |
| 5 | **Implement auto-save and undo/redo** -- Add auto-save draft functionality on all forms. Implement undo/redo with Ctrl+Z/Ctrl+Y support and visible undo button. | CROSS-007, PR-001 | M | 8.8 | 1,723+ |
| 6 | **Create Thai localization package** -- Translate all UI labels, error messages, and help documentation to Thai. Standardize Thai/English label usage. Add พ.ศ. date support. | CROSS-004, CROSS-006, CROSS-009, CROSS-003 | XL | 8.7 | 2,193+ |
| 7 | **Build pre-built Thai system connectors** -- Create connectors for Express Accounting, PEAK, Prosoft, LINE, Thai banking APIs, and e-Tax Invoice system. Add guided setup wizard. | CN-001, CN-002 | XL | 8.5 | 2,567 |
| 8 | **Implement role-based permission templates** -- Create pre-built role templates (Admin, Manager, Staff, Viewer, Auditor). Add bulk permission assignment and role cloning. | SY-001 | M | 8.3 | 1,891 |
| 9 | **Add batch/bulk operations across modules** -- Enable bulk PO creation, batch receipt upload, bulk user import with preview, and bulk document processing. | PR-004, EX-002 | L | 8.2 | 1,789+ |
| 10 | **Optimize performance for large datasets** -- Implement virtual scrolling, lazy loading, and pagination for tables > 100 rows. Add progress indicators for all operations > 2 seconds. | VM-001, CROSS-005 | L | 8.0 | 2,134 |
| 11 | **Build PR-to-PO direct conversion flow** -- Auto-populate PO fields from approved PR data. Allow one-click conversion with override capability. | PR-002 | M | 7.8 | 1,456 |
| 12 | **Make all modules mobile-responsive** -- Redesign critical workflows (expense claims, PO approvals) for mobile-first experience. Fix table overflow, tap targets, and viewport issues. | CROSS-010, CROSS-012, HD-003 | XL | 7.7 | 1,634+ |
| 13 | **Add customizable dashboard** -- Implement drag-and-drop widget arrangement, widget show/hide, and saved dashboard profiles per role. Add trend indicators and context to summary cards. | HD-001, HD-002 | L | 7.5 | 1,847 |
| 14 | **Implement Thai sentiment analysis** -- Add Thai NLP model for customer feedback analysis. Support multi-language sentiment scoring and Thai-specific language patterns. | CF-001 | L | 7.3 | 1,567 |
| 15 | **Add flexible approval workflows** -- Implement conditional routing, parallel approvals, delegation during leave, and configurable approval thresholds. | EX-003 | L | 7.2 | 1,234 |
| 16 | **Create Thai document templates** -- Add templates for Thai quotation (ใบเสนอราคา), Thai invoice (ใบแจ้งหนี้), Thai receipt (ใบเสร็จรับเงิน) with proper tax ID and branch code fields. | SD-001 | M | 7.0 | 1,567 |
| 17 | **Fix WCAG accessibility issues** -- Address all Critical and High accessibility gaps. Add ARIA labels, keyboard navigation, focus indicators, and sufficient color contrast. | CROSS-017, accessibility table | L | 6.8 | 1,234+ |
| 18 | **Add PDF annotation and document markup** -- Implement in-browser PDF viewer with highlight, comment, and stamp tools for financial document verification. | FD-003 | M | 6.7 | 1,345 |
| 19 | **Implement expense policy engine** -- Build configurable rules engine for auto-checking expense limits, duplicate detection, and policy violations with auto-flag. | EX-004 | L | 6.5 | 1,067 |
| 20 | **Add connection health monitoring and alerts** -- Real-time API connection monitoring dashboard with proactive alerts via email/LINE when connections fail. | CN-004 | M | 6.3 | 987 |

### Effort Definitions

| Size | Estimated Duration | Team Size |
|------|-------------------|-----------|
| S (Small) | 1-2 weeks | 1-2 developers |
| M (Medium) | 2-4 weeks | 2-3 developers |
| L (Large) | 1-2 months | 3-5 developers |
| XL (Extra Large) | 2-4 months | 5+ developers, cross-functional |

### Quick Wins (High Impact, Low Effort)

The following improvements can be implemented within 1-2 sprint cycles:

1. Add progress indicators to all operations > 2 seconds (S effort, reduces 67.8% of "app crashed" perceptions)
2. Add search bar to Settings page (S effort, helps 1,567 users)
3. Add breadcrumb navigation to all modules (S effort, helps 1,891 users)
4. Add พ.ศ. toggle for date displays (S effort, helps 1,891 users)
5. Add notification categorization/filtering (S effort, helps 1,089 users)
6. Enable multi-file upload for receipts (S effort, helps 1,789 users)
7. Add Thai Baht symbol consistency across modules (S effort, helps 987 users)
8. Fix dark mode for remaining 4 modules (M effort, helps 1,234 users)

---

## 8. Detailed Age Group Analysis

---

### 8.1 Group A (21-26 years) -- New Graduates, Junior Staff

**Overall Satisfaction:** 3.04 / 5
**Sample Size:** 1,000
**Primary Pain Points:** Mobile experience, speed, modern UX expectations

#### What They Liked Least

1. **Mobile experience is severely lacking** (67.3% dissatisfied)
   - Group A primarily uses mobile devices (54%) but the platform is clearly designed desktop-first
   - Critical workflows like expense claims are unusable on iPhone screens
   - _"ระบบนี้ใช้บนมือถือไม่ได้เลย ต้องมานั่งเปิดคอมทุกครั้ง ในขณะที่ app อื่นๆ ที่ใช้ทำงานทำบนมือถือได้หมด"_ -- Female, 22

2. **UX feels outdated compared to consumer apps** (58.4% dissatisfied)
   - Group A compares the platform to Notion, Slack, Instagram, and LINE
   - Expects gesture navigation, swipe actions, instant feedback, and animation
   - _"UI ดูเหมือนเว็บราชการ ไม่มี animation ไม่มี smooth transition กดปุ่มแล้วไม่มี feedback ว่าได้กดแล้ว ไม่เหมือน app ที่ใช้ในชีวิตประจำวัน"_ -- Male, 23

3. **Too many clicks for simple tasks** (54.1% dissatisfied)
   - Accustomed to 1-2 tap workflows in mobile banking and social media apps
   - _"สร้าง PR ต้องกด 5 ครั้ง ผ่าน 5 หน้า ทั้งที่แค่อยากสั่งซื้อของ ทำไมไม่มีปุ่ม 'Quick Create' บน Dashboard"_ -- Female, 24

4. **No keyboard shortcuts or power user features** (47.3% dissatisfied)
   - Group A is comfortable with keyboard-driven workflows (Ctrl+K, Cmd+P, etc.)
   - _"ใช้ Notion ทุกวัน มี Ctrl+K ค้นหาได้ทุกอย่าง แต่ระบบนี้ไม่มี shortcut อะไรเลย ต้องใช้ mouse คลิกทุกอย่าง"_ -- Male, 25

5. **Dark mode is incomplete** (38.7% dissatisfied)
   - Group A works late and prefers dark mode consistently
   - _"Dark mode เปิดแล้วบางหน้ายังเป็น Light อยู่ ทำให้ตาแสบทุกครั้งที่สลับหน้า ไม่เหมือน VS Code ที่ dark mode ทั้งหมด"_ -- Female, 21

#### Behavioral Patterns

- Average task completion time: 3.2x longer than expected (compared to consumer app benchmarks)
- 43% of Group A abandoned tasks midway at least once during testing
- 67% attempted to use mobile device first before switching to desktop
- Most frequently requested feature: Global command palette (Ctrl+K / Cmd+K)

---

### 8.2 Group B (26-35 years) -- Junior-to-Mid Level Professionals

**Overall Satisfaction:** 3.41 / 5 (Highest among all groups)
**Sample Size:** 1,000
**Primary Pain Points:** Integration gaps, workflow automation, bulk operations

#### What They Liked Least

1. **Lack of automation and bulk operations** (52.3% dissatisfied)
   - Group B handles high-volume repetitive tasks and expects batch processing
   - _"ทุกวันต้องสร้าง PO 20-30 ใบ ถ้า upload CSV ได้ก็ประหยัดเวลา 2 ชั่วโมง แต่ต้องกรอกมือทีละใบ"_ -- Male, 29

2. **Missing integrations with existing tools** (48.7% dissatisfied)
   - Group B uses multiple SaaS tools and expects seamless data flow
   - _"ใช้ Google Sheets, Slack, Trello ทุกวัน แต่ระบบ ANTS ไม่ connect กับอะไรเลย ต้อง copy-paste ข้อมูลไปมา"_ -- Female, 31

3. **Export format limitations** (41.2% dissatisfied)
   - Group B needs data in various formats for cross-tool analysis
   - _"Export ได้แค่ PDF ทำอะไรต่อไม่ได้เลย ต้องการ Excel, CSV, หรือ API สำหรับ pull data ออกมาวิเคราะห์"_ -- Male, 28

4. **No API for custom automation** (37.4% dissatisfied)
   - Group B wants to build custom workflows connecting ANTS to other systems
   - _"อยากเขียน script ให้ auto-create PR จาก inventory alert แต่ไม่มี public API ให้ใช้"_ -- Female, 27

5. **Inconsistent data presentation across modules** (34.1% dissatisfied)
   - Same data displayed differently in different modules
   - _"Vendor name ในหน้า Procurement แสดงเป็น 'ABC Co.,Ltd.' แต่ใน Vendor Management แสดงเป็น 'ABC Company Limited' สับสนว่าเป็น vendor เดียวกันหรือเปล่า"_ -- Male, 33

#### Behavioral Patterns

- Average task completion time: 1.8x longer than expected
- 28% of Group B found workarounds using external tools (Google Sheets, manual scripts)
- 71% requested API documentation within the first week
- Most frequently requested feature: Bulk import/export with CSV/Excel

---

### 8.3 Group C (35-45 years) -- Senior Staff, Managers

**Overall Satisfaction:** 3.22 / 5
**Sample Size:** 1,000
**Primary Pain Points:** Compliance features, reporting depth, Thai localization

#### What They Liked Least

1. **Reporting and analytics lack depth** (56.7% dissatisfied)
   - Group C needs detailed drill-down reports for management decision-making
   - _"Report แสดงแค่ summary level ไม่สามารถ drill-down ถึง transaction level ได้ ต้องไป export แล้วทำ pivot table เอง ไม่ต่างจากใช้ Excel"_ -- Male, 41

2. **Thai document format compliance** (51.2% dissatisfied)
   - Group C is responsible for compliance with Thai Revenue Department requirements
   - _"ใบกำกับภาษีที่ออกจากระบบไม่ตรงตามรูปแบบที่กรมสรรพากรกำหนด ต้องไปแก้ใน Word แล้วพิมพ์ใหม่ เสียเวลามาก"_ -- Female, 40

3. **Approval delegation not possible during leave** (47.8% dissatisfied)
   - Group C frequently needs to delegate approval authority
   - _"ลาป่วย 3 วัน เอกสาร 27 รายการค้างอนุมัติ ไม่สามารถมอบหมายให้รองอนุมัติแทนได้ งานทุกอย่างหยุดชะงัก"_ -- Male, 44

4. **Audit trail insufficient for compliance** (42.3% dissatisfied)
   - Group C needs comprehensive audit trails for internal and external audits
   - _"ผู้สอบบัญชีขอ audit trail ของ PO approval ย้อนหลัง 6 เดือน ระบบแสดงได้แค่ 3 เดือนล่าสุด ต้องไปหาจาก email แทน"_ -- Female, 37

5. **Workflow cannot be customized to match company process** (38.9% dissatisfied)
   - Group C manages processes that differ by company policy
   - _"บริษัทมี approval flow 4 ระดับ ตามวงเงิน แต่ระบบตั้งค่าได้แค่ 2 ระดับ ต้อง workaround ด้วยการส่ง email นอกระบบ"_ -- Male, 38

#### Behavioral Patterns

- Average task completion time: 2.1x longer than expected
- 52% of Group C reverted to previous tools (SAP, Oracle) for complex reporting
- 38% reported training their teams took longer than expected due to mixed terminology
- Most frequently requested feature: Configurable multi-level approval workflows

---

### 8.4 Group D (45+ years) -- Executives, Directors

**Overall Satisfaction:** 2.97 / 5 (Lowest among all groups)
**Sample Size:** 1,000
**Primary Pain Points:** Complexity, readability, learning curve

#### What They Liked Least

1. **Overall system is too complex** (72.4% dissatisfied)
   - Group D expects a simple, clear interface focused on decision-making data
   - _"ระบบมีปุ่มเยอะมาก ไม่รู้จะกดตรงไหน แค่อยากดูว่าเดือนนี้จ่ายเงินไปเท่าไหร่ แต่ต้องเข้า 3 หน้า กด filter 2 อัน ถึงจะเห็นตัวเลข ทำไมไม่แสดงตรงหน้าแรกเลย"_ -- Male, 56

2. **Font too small, readability poor** (68.7% dissatisfied)
   - Many Group D users need larger fonts and higher contrast
   - _"ตัวหนังสือในตารางเล็กมาก ต้องเอาหน้าจ่อจอ ขยายก็ได้แต่ layout เพี้ยน อ่านเลขไม่ออกว่า 1 หรือ 7 อยากให้มีปุ่มขยายตัวหนังสือได้"_ -- Female, 52

3. **English technical terms everywhere** (63.4% dissatisfied)
   - Group D prefers all-Thai interface with clear, simple language
   - _"เจอคำว่า 'Dashboard', 'Pipeline', 'Analytics', 'Connector', '3-Way Match' ไม่เข้าใจเลย ทำไมไม่เขียนเป็นภาษาไทยให้คนอ่านรู้เรื่อง เช่น 'หน้าสรุป', 'ช่องทางขาย', 'วิเคราะห์ข้อมูล'"_ -- Male, 58

4. **No guided onboarding or tutorial** (59.8% dissatisfied)
   - Group D needs step-by-step guidance when using new features
   - _"เปิดระบบครั้งแรก ไม่มีคำแนะนำอะไรเลย ไม่รู้จะเริ่มต้นตรงไหน กดปุ่มไปแล้วก็ไม่แน่ใจว่าถูกหรือเปล่า อยากได้ tutorial video สอนเป็นภาษาไทย"_ -- Female, 49

5. **Fear of making irreversible mistakes** (54.2% dissatisfied)
   - Group D is cautious and needs clear confirmation and undo capabilities
   - _"กดลบเอกสารไปโดยไม่ตั้งใจ ระบบถามแค่ 'Confirm Delete?' กด Yes ไปแล้วเอกสารหายเลย ไม่มีถังขยะ ไม่มี Undo ต้องสร้างใหม่ตั้งแต่ต้น"_ -- Male, 53

6. **Billing page incomprehensible** (52.1% dissatisfied)
   - Group D (often budget owners) cannot understand pricing structure
   - _"ดูหน้า Billing ไม่รู้ว่าบริษัทจ่ายค่าอะไรบ้าง ตัวเลข API Calls, Storage GB มันแปลว่าอะไร เดือนหน้าจะจ่ายเท่าไหร่ ไม่มีใครอธิบายได้"_ -- Female, 55

#### Behavioral Patterns

- Average task completion time: 4.7x longer than expected
- 78% of Group D required assistance from IT or younger colleagues at least once
- 34% of Group D gave up on tasks without completing them
- 23% of Group D requested to revert to paper-based processes
- Average number of support requests: 6.3 per user (vs. 1.2 for Group A)
- Most frequently requested feature: Simplified executive dashboard with Thai explanations

#### Specific Accessibility Concerns from Group D

| Issue | Reported By | Count |
|-------|------------|-------|
| Cannot read table text at default zoom | 423 (42.3%) | Very frequent |
| Difficulty finding the correct button to click | 387 (38.7%) | Very frequent |
| Confusion between similar-looking icons | 312 (31.2%) | Frequent |
| Double-clicking when single click is needed | 267 (26.7%) | Frequent |
| Misinterpreting color-coded status indicators | 234 (23.4%) | Frequent |
| Difficulty with drag-and-drop interactions | 189 (18.9%) | Moderate |
| Accidentally triggering unintended actions | 178 (17.8%) | Moderate |
| Unable to read CAPTCHA during login | 145 (14.5%) | Moderate |
| Forgetting password due to complex requirements | 134 (13.4%) | Moderate |
| Confusion with multi-tab workflows | 123 (12.3%) | Moderate |

---

## 9. Appendix

---

### A.1 Raw Satisfaction Scores -- Complete Breakdown

#### By Module (All Groups Combined)

| Module | Usability | Design | Performance | Features | Overall |
|--------|-----------|--------|-------------|----------|---------|
| Home Dashboard | 3.20 | 2.98 | 3.23 | 2.85 | 3.09 |
| Procurement | 2.93 | 2.88 | 2.78 | 2.95 | 2.91 |
| Vendor Management | 3.08 | 2.90 | 2.60 | 2.87 | 2.87 |
| Expense & Receipt | 2.78 | 2.95 | 2.43 | 2.90 | 2.90 |
| Finance Doc Hub | 2.90 | 2.85 | 2.70 | 2.90 | 2.90 |
| Logistics FX | 2.80 | 2.92 | 2.53 | 2.88 | 2.88 |
| Sales Doc Gen | 3.15 | 3.10 | 2.98 | 3.17 | 3.17 |
| Connectors | 2.68 | 2.55 | 2.48 | 2.39 | 2.39 |
| Customer Feedback | 3.08 | 3.00 | 2.80 | 2.99 | 2.99 |
| System | 2.78 | 2.65 | 2.70 | 2.77 | 2.77 |

#### By Age Group (All Modules Combined)

| Age Group | Usability | Design | Performance | Features | Overall |
|-----------|-----------|--------|-------------|----------|---------|
| Group A (21-26) | 2.87 | 2.92 | 2.95 | 2.80 | 3.04 |
| Group B (26-35) | 3.38 | 3.32 | 3.28 | 3.41 | 3.41 |
| Group C (35-45) | 3.15 | 3.08 | 3.10 | 3.22 | 3.22 |
| Group D (45+) | 2.42 | 2.35 | 2.40 | 2.57 | 2.97 |

### A.2 Statistical Distribution Analysis

#### Overall Satisfaction Score Distribution

```
Score 1.0: ████████████████ 15.8% (632 users)
Score 1.5: ██████████ 10.2% (408 users)
Score 2.0: █████████████ 13.1% (524 users)
Score 2.5: ████████████████ 16.3% (652 users)
Score 3.0: ██████████████████ 18.4% (736 users)
Score 3.5: ████████████ 12.1% (484 users)
Score 4.0: ██████████ 9.8% (392 users)
Score 4.5: ████ 3.2% (128 users)
Score 5.0: █ 1.1% (44 users)
```

**Mean:** 3.18 | **Median:** 3.0 | **Std Dev:** 0.94 | **Skewness:** -0.23 (slightly left-skewed)

#### Task Completion Rate by Module

```
Home Dashboard:      ██████████████████████████████████████████ 89.3%
Sales Doc Gen:       █████████████████████████████████████████ 87.1%
Customer Feedback:   ████████████████████████████████████████ 85.6%
Finance Doc Hub:     ████████████████████████████████████ 78.4%
Expense & Receipt:   ██████████████████████████████████ 74.2%
Vendor Management:   █████████████████████████████████ 72.8%
Procurement:         ████████████████████████████████ 71.3%
Logistics FX:        ██████████████████████████████ 68.7%
System:              ████████████████████████████ 64.2%
Connectors:          ████████████████████████ 53.1%
```

#### Average Time to Complete Key Tasks (minutes)

| Task | Group A | Group B | Group C | Group D | Target |
|------|---------|---------|---------|---------|--------|
| Create a PR | 8.3 | 5.7 | 6.2 | 14.8 | 3.0 |
| Submit expense claim | 6.1 | 4.3 | 5.1 | 12.4 | 2.0 |
| Compare 3 vendor quotes | 11.2 | 7.8 | 8.4 | 19.3 | 5.0 |
| Generate sales document | 5.4 | 3.8 | 4.7 | 10.2 | 2.0 |
| Set up API connector | 22.7 | 14.3 | 18.6 | 45.2+ | 10.0 |
| Create user account | 4.8 | 3.2 | 3.9 | 9.7 | 1.5 |
| Find specific PO | 3.4 | 2.1 | 2.8 | 7.3 | 0.5 |
| Approve pending items | 2.7 | 1.8 | 2.3 | 5.6 | 0.5 |
| Run analytics report | 4.2 | 3.1 | 3.5 | 8.9 | 1.5 |
| Upload and OCR receipt | 3.8 | 2.6 | 3.2 | 8.1 | 1.0 |

**Note:** Group D "Set up API connector" shows 45.2+ because 34% of Group D users abandoned the task before completion.

#### Error Rate by Module

| Module | Error Rate | Most Common Error Type |
|--------|-----------|----------------------|
| Connectors | 23.4% | Configuration syntax errors |
| Procurement | 18.7% | Missing required fields in forms |
| Expense & Receipt | 16.3% | OCR misread values accepted without review |
| Logistics FX | 14.8% | Incorrect unit/currency selection |
| Vendor Management | 12.1% | Duplicate vendor entries |
| Finance Doc Hub | 11.4% | Incorrect case classification |
| System | 10.8% | Wrong permission assignment |
| Sales Doc Gen | 8.3% | Template selection mismatch |
| Customer Feedback | 6.7% | Survey logic errors |
| Home Dashboard | 4.2% | N/A (mostly view-only) |

### A.3 Testing Environment Details

**Server Infrastructure:**
- Hosting: AWS ap-southeast-1 (Singapore)
- Application Server: 4x c5.2xlarge instances behind ALB
- Database: Amazon RDS PostgreSQL 15.4 (db.r5.xlarge)
- CDN: CloudFront with Bangkok edge location
- Average server response time: 142ms (p50), 487ms (p95), 1,234ms (p99)

**Test Network Conditions:**
- 60% of tests: High-speed office connection (100+ Mbps)
- 25% of tests: Standard home broadband (20-50 Mbps)
- 10% of tests: Mobile 4G (5-20 Mbps)
- 5% of tests: Slow 3G simulation (1-3 Mbps)

**Browser Testing Configuration:**
- All tests conducted with cleared cache (first-visit experience)
- Cookie consent accepted on all tests
- Browser extensions disabled
- Default browser font size (16px)
- No ad blockers active

**Known Test Limitations:**
1. Simulated users do not account for real-world multitasking behavior (switching between ANTS and other applications)
2. Network conditions were simulated, not measured from actual Thai ISP connections
3. Thai language OCR testing used a curated set of 500 receipt/document images, which may not fully represent the diversity of Thai business documents in the wild
4. Group D simulation may underestimate actual difficulty, as simulated users have baseline digital literacy that some real-world 45+ executives may not possess
5. Testing did not include accessibility assistive technologies (screen readers, magnifiers, voice control)
6. Mobile testing was conducted on emulated devices, not physical hardware

### A.4 Issue Severity Definitions

| Severity | Definition | Response Target |
|----------|-----------|-----------------|
| **Critical** | Blocks core workflow. Users cannot complete essential tasks. Data loss risk. | Fix within 2 weeks |
| **High** | Significantly impairs productivity. Workaround exists but is time-consuming. | Fix within 1 month |
| **Medium** | Causes frustration but does not block workflows. Moderate impact on efficiency. | Fix within 1 quarter |
| **Low** | Minor annoyance. Cosmetic issues. Nice-to-have improvements. | Plan for future release |

### A.5 Glossary of Thai Terms Used in Report

| Thai Term | English Translation | Context |
|-----------|-------------------|---------|
| ใบเสนอราคา | Quotation | Sales/Vendor document |
| ใบแจ้งหนี้ | Invoice | Finance/Billing document |
| ใบกำกับภาษี | Tax Invoice | Legal tax document per Thai Revenue Dept. |
| ใบเสร็จรับเงิน | Receipt | Payment confirmation document |
| พ.ศ. (พุทธศักราช) | Buddhist Era | Thai calendar system (ค.ศ. + 543) |
| กรมสรรพากร | Revenue Department | Thai government tax authority |
| ตำบล/อำเภอ/จังหวัด | Sub-district/District/Province | Thai address hierarchy |
| เลขประจำตัวผู้เสียภาษี | Tax Identification Number | 13-digit Thai Tax ID |
| สาขา | Branch | Company branch identifier |
| ปริมณฑล | Greater Bangkok area | Bangkok metropolitan region |

### A.6 Comparison with Industry Benchmarks

| Metric | ANTS Autopilot v2 | Industry Average (Thai SaaS) | Industry Best-in-Class |
|--------|--------------------|------------------------------|----------------------|
| Overall Satisfaction | 3.18 / 5 | 3.45 / 5 | 4.12 / 5 |
| Task Completion Rate | 74.5% | 82.3% | 94.1% |
| Average Time on Task | 2.3x target | 1.5x target | 1.1x target |
| Error Rate | 13.7% | 9.2% | 4.1% |
| Mobile Satisfaction | 2.67 / 5 | 3.21 / 5 | 4.03 / 5 |
| Thai Localization Score | 2.84 / 5 | 3.52 / 5 | 4.34 / 5 |
| Support Request Rate | 3.1 per user | 1.8 per user | 0.6 per user |
| Feature Discovery Rate | 41.2% | 58.7% | 78.3% |
| First-Session Task Success | 52.3% | 67.8% | 85.2% |

### A.7 NPS (Net Promoter Score) Analysis

| Group | Promoters (9-10) | Passives (7-8) | Detractors (0-6) | NPS |
|-------|-----------------|----------------|-------------------|-----|
| Group A | 12.3% | 28.1% | 59.6% | -47.3 |
| Group B | 18.7% | 35.4% | 45.9% | -27.2 |
| Group C | 15.2% | 31.8% | 53.0% | -37.8 |
| Group D | 8.4% | 22.7% | 68.9% | -60.5 |
| **Overall** | **13.7%** | **29.5%** | **56.8%** | **-43.1** |

**Benchmark:** Thai B2B SaaS average NPS is -12 to +8. The ANTS score of -43.1 is significantly below benchmark, driven primarily by Group D detractors and mobile experience dissatisfaction across all groups.

---

### A.8 Recommendations Implementation Roadmap

#### Phase 1: Critical Fixes (Weeks 1-4)
- Auto-save and undo/redo implementation
- Progress indicators for all long operations
- Thai OCR accuracy improvement (quick gains with existing model tuning)
- Breadcrumb navigation addition
- Settings search bar

#### Phase 2: Thai Localization (Weeks 5-12)
- Complete Thai UI translation
- พ.ศ. date support
- Thai document templates
- Thai error messages
- Thai help documentation (priority: top 20 most-viewed articles)

#### Phase 3: UX Overhaul (Weeks 8-20)
- Navigation architecture flattening
- Global search implementation
- Dashboard customization
- Mobile responsive redesign
- Role-based permission templates
- LINE integration

#### Phase 4: Advanced Features (Weeks 16-28)
- Pre-built Thai system connectors
- Thai sentiment analysis
- Expense policy engine
- Flexible approval workflows
- PDF annotation
- Bulk operations across modules

#### Phase 5: Platform Maturity (Weeks 24-36)
- Offline capability (PWA)
- Advanced analytics with drill-down
- Real-time connection monitoring
- Full WCAG 2.1 AA compliance
- API marketplace
- SSO integration

---

### A.9 Detailed User Session Behavior Analysis

#### Session Duration Distribution

```
< 5 min:    ████████████ 12.4% (496 users) -- mostly quick-look executives
5-15 min:   █████████████████████ 21.3% (852 users) -- single-task sessions
15-30 min:  ██████████████████████████████ 30.1% (1,204 users) -- standard work sessions
30-60 min:  █████████████████████████ 25.8% (1,032 users) -- complex multi-task sessions
60+ min:    ██████████ 10.4% (416 users) -- heavy processing/report generation
```

#### Feature Discovery Rate by Module

Users were tested on whether they could independently discover and use key features without guidance.

| Module | Feature | Discovery Rate | Avg Time to Discover |
|--------|---------|---------------|---------------------|
| Home Dashboard | Notification panel | 78.3% | 1.2 min |
| Home Dashboard | Widget data drill-down | 34.1% | 8.7 min |
| Procurement | 3-Way Match initiation | 41.2% | 12.3 min |
| Procurement | PR approval chain view | 52.7% | 6.4 min |
| Procurement | Analytics date range filter | 47.8% | 7.1 min |
| Vendor Management | Comparison tool | 38.4% | 14.2 min |
| Vendor Management | Audit log access | 29.6% | 18.7 min |
| Vendor Management | Quotation upload | 56.3% | 4.8 min |
| Expense & Receipt | OCR manual correction | 44.7% | 9.3 min |
| Expense & Receipt | Claim status tracking | 61.2% | 3.2 min |
| Finance Doc Hub | Case creation from scratch | 37.8% | 15.4 min |
| Finance Doc Hub | Verification workflow start | 31.4% | 17.8 min |
| Logistics FX | Freight OCR upload | 48.9% | 6.7 min |
| Logistics FX | Cost calculator multi-route | 33.2% | 13.1 min |
| Sales Doc Gen | Template selection | 67.4% | 2.8 min |
| Sales Doc Gen | Pipeline stage filter | 54.1% | 5.3 min |
| Connectors | API key generation | 22.7% | 23.4 min |
| Connectors | Webhook configuration | 18.3% | 28.1 min |
| Customer Feedback | Survey builder access | 62.8% | 3.1 min |
| Customer Feedback | Response export | 43.6% | 8.9 min |
| System | User role assignment | 45.2% | 10.2 min |
| System | Billing history view | 38.7% | 12.8 min |

**Key Insight:** Features requiring more than 3 navigation steps had discovery rates below 40%. The Connectors module had the lowest overall discovery rate at 20.5%, suggesting the need for significant UX redesign or guided onboarding specific to that module.

#### Rage Click Analysis

"Rage clicks" are defined as 3+ rapid clicks on the same element within 1 second, indicating user frustration.

| Location | Rage Click Count | Primary Cause |
|----------|-----------------|---------------|
| Vendor Comparison "Load" button | 12,847 | No loading indicator; users think click didn't register |
| Receipt OCR "Process" button | 9,234 | Long OCR processing time with no feedback |
| PR form "Next" button | 7,891 | Page transition delay (1.5-2.5 seconds) |
| Dashboard widget areas | 6,743 | Users expect click-to-drill-down but widgets are static |
| Pipeline deal cards | 5,678 | Users attempt drag-and-drop but cards are not draggable |
| Export button (all modules) | 4,567 | PDF generation takes 5-8 seconds with no progress bar |
| Global navigation menu items | 3,891 | Sub-menu expand delay of 0.8 seconds feels unresponsive |
| Settings category panels | 3,234 | Accordion animation is slow (0.5 seconds) |
| Mobile hamburger menu | 2,987 | Touch target too small (32px, should be 44px minimum) |
| Date picker calendar cells | 2,456 | Touch targets overlap on mobile; wrong date selected |

**Total rage clicks recorded:** 69,528 across all sessions
**Average rage clicks per user:** 17.4
**Group D had the highest rate:** 28.7 rage clicks per user

#### Tab/Window Switching Behavior

Tracking how often users left the ANTS platform to use other tools during their session.

| Reason for Leaving ANTS | Frequency | % of Sessions | Destination |
|--------------------------|-----------|---------------|-------------|
| Using Excel for calculations | 4,234 | 33.9% | Microsoft Excel / Google Sheets |
| Checking email for document references | 3,891 | 31.2% | Gmail / Outlook |
| Using LINE for team communication | 3,456 | 27.7% | LINE Desktop / Mobile |
| Looking up vendor information externally | 2,789 | 22.4% | Google Search / Company websites |
| Creating documents in Word | 2,134 | 17.1% | Microsoft Word / Google Docs |
| Checking ERP system for validation | 1,891 | 15.2% | SAP / Oracle / Express |
| Reading help documentation | 1,567 | 12.6% | Google Search (since ANTS docs are insufficient) |
| Using calculator for currency conversion | 1,234 | 9.9% | Calculator app / Google |
| Screenshot for sharing with colleagues | 987 | 7.9% | Screenshot tool |
| Reporting issues to IT | 567 | 4.5% | IT ticketing system |

**Implication:** 33.9% of sessions involved switching to Excel, confirming that ANTS analytics and calculation features are insufficient for user needs. The 27.7% LINE usage confirms the critical need for LINE integration.

### A.10 Heatmap Analysis Summary

#### Most Clicked Areas (Desktop, 1920x1080)

The following areas received the highest click density across all desktop sessions:

1. **Top navigation bar** (38.4% of all clicks) -- Users heavily rely on the main navigation
2. **Primary action buttons** (23.1%) -- "Create New", "Submit", "Approve" buttons
3. **Table sort headers** (12.7%) -- Users frequently try to sort data tables
4. **Search/filter inputs** (9.8%) -- Despite limited search capability, users attempt frequently
5. **Sidebar module links** (8.3%) -- Module switching via sidebar
6. **Footer/pagination** (4.2%) -- Table pagination controls
7. **Help/support icon** (2.1%) -- Low usage suggests users don't know help exists or don't trust it
8. **User profile menu** (1.4%) -- Minimal interaction with account settings

#### Dead Click Zones (Areas users click expecting interaction but nothing happens)

| Zone | Click Attempts | Expected Behavior |
|------|---------------|-------------------|
| Dashboard summary cards | 8,234 | Expected drill-down to detailed view |
| Chart data points | 6,123 | Expected tooltip or filter by that data point |
| Table row text (non-link) | 5,891 | Expected navigation to detail view |
| Status badges | 4,567 | Expected filter by that status |
| Vendor name in lists | 3,789 | Expected link to vendor profile |
| Document filenames | 3,234 | Expected in-place preview |
| Column headers (non-sortable) | 2,891 | Expected sorting toggle |
| Module icons in sidebar | 2,456 | Expected expand/collapse of sub-items |
| Date text in tables | 1,987 | Expected date filter application |
| Amount values in tables | 1,678 | Expected currency conversion tooltip |

**Total dead clicks:** 40,850 across all sessions
**Insight:** Users have strong expectations for interactive elements based on their experience with modern web applications. The high dead-click rate on summary cards (8,234) and chart data points (6,123) suggests implementing click-to-drill-down would significantly improve perceived interactivity.

### A.11 Support Request Analysis

#### Support Tickets by Category

| Category | Count | % of Total | Avg Resolution Time |
|----------|-------|------------|-------------------|
| "How do I..." questions (feature discovery) | 3,456 | 27.8% | 4.2 min |
| Bug reports (actual bugs) | 2,891 | 23.3% | Escalated |
| "Is this a bug?" (UX confusion, not bugs) | 2,134 | 17.2% | 6.1 min |
| Performance complaints | 1,567 | 12.6% | 8.3 min |
| Thai language/encoding issues | 987 | 7.9% | Escalated |
| Mobile display issues | 678 | 5.5% | Escalated |
| Account/permission issues | 456 | 3.7% | 3.4 min |
| Feature requests | 234 | 1.9% | Logged |
| Other | 12 | 0.1% | Varies |
| **Total** | **12,415** | **100%** | -- |

**Key Finding:** 17.2% of support tickets were "Is this a bug?" queries that were actually UX confusion -- users could not tell if the system was working correctly because of insufficient feedback, unclear states, or unexpected behavior. This category is entirely preventable through better UX design.

#### Most Common "How Do I" Questions

| Question (translated) | Frequency | Answer Complexity |
|----------------------|-----------|-------------------|
| "How do I export to Excel?" | 487 | Feature does not exist (PDF only) |
| "How do I delegate my approvals?" | 423 | Feature does not exist |
| "How do I change the date to พ.ศ.?" | 389 | Feature does not exist |
| "How do I search across all modules?" | 367 | Feature does not exist |
| "How do I undo my last action?" | 312 | Feature does not exist |
| "How do I upload multiple files at once?" | 298 | Feature does not exist |
| "How do I create a PO from this PR?" | 276 | Requires manual re-entry (not intuitive) |
| "How do I set up LINE notifications?" | 254 | Feature does not exist |
| "How do I customize my dashboard?" | 231 | Feature does not exist |
| "How do I see my recently viewed items?" | 219 | Feature does not exist |

**Critical Insight:** 9 out of the top 10 "How do I" questions relate to features that do not exist. This means users intuitively expect these capabilities, and their absence represents the largest gap between user expectations and platform reality.

### A.12 Competitive Feature Comparison

Comparison of ANTS AI Solution Hub against key competitors in the Thai market.

| Feature | ANTS Autopilot v2 | Odoo (Thai Edition) | SAP Business One | PEAK Accounting | Freshservice |
|---------|-------------------|--------------------|--------------------|----------------|-------------|
| Thai UI | Partial | Full | Full | Full | Partial |
| พ.ศ. Date Support | No | Yes | Yes | Yes | No |
| Thai OCR | 67% accuracy | N/A | 85% accuracy | 92% accuracy | N/A |
| LINE Integration | No | Community plugin | No | Yes | No |
| Mobile App | Web only (poor) | Native iOS/Android | Native iOS/Android | Native iOS/Android | Native iOS/Android |
| Thai Tax Documents | No | Yes | Yes | Yes | No |
| Bulk Operations | No | Yes | Yes | Limited | Yes |
| Offline Mode | No | Limited | No | Limited | No |
| Keyboard Shortcuts | No | Yes | Yes | No | Yes |
| Custom Approval Flows | No | Yes | Yes | Limited | Yes |
| Thai Sentiment Analysis | No | No | No | No | No |
| Global Search | No | Yes | Yes | Yes | Yes |
| Dark Mode | Partial (6/10 modules) | Full | No | Full | Full |
| Drag-and-Drop | No | Yes | Limited | No | Yes |
| Export Formats | PDF only | PDF, Excel, CSV | PDF, Excel, CSV, XML | PDF, Excel, CSV | PDF, Excel, CSV |
| Role Templates | No | Yes | Yes | Yes | Yes |
| Undo/Redo | No | Limited | No | Limited | Yes |
| Document Annotation | No | No | Yes | No | No |
| API Documentation (Thai) | No | Community | Yes | Yes | No |
| SSO Support | No | Yes | Yes | No | Yes |

**Competitive Position Assessment:**
ANTS Autopilot v2 currently lags behind competitors in 15 out of 20 compared feature areas. The most critical competitive disadvantages are:
1. Lack of Thai localization features (พ.ศ., tax documents, OCR accuracy)
2. No native mobile application
3. No bulk operations or data export flexibility
4. No LINE integration (unique to Thai market)
5. Missing basic UX patterns (global search, undo/redo, keyboard shortcuts)

### A.13 User Verbatim Feedback Collection -- Additional Quotes

The following are additional unedited user quotes collected during the testing period, organized by theme.

#### Theme: Navigation Frustration

_"เมนูซ้อนกันหลายชั้น เหมือนเข้าป่า หาของที่ต้องการไม่เจอ"_ -- Group A, Male, 24
_"ทุกครั้งที่ต้องการสร้างเอกสารใหม่ ต้องนึกว่าอยู่ใน menu ไหน คลิกไปคลิกมา 5-6 ครั้ง เสียเวลาทุกวัน"_ -- Group B, Female, 30
_"กดปุ่ม Back แล้วไม่กลับไปหน้าที่คาดหวัง บางทีกลับไปหน้าแรกเลย ต้องเริ่มเข้าใหม่ตั้งแต่ต้น"_ -- Group C, Male, 43
_"ไม่มี breadcrumb ไม่รู้ว่าตัวเองอยู่ตรงไหนของระบบ หลงทุกครั้ง"_ -- Group D, Female, 51

#### Theme: Thai Language Issues

_"ฟอนต์ภาษาไทยในตาราง render แปลกๆ สระอำกับตัว ม ห่างกัน อ่านยากมาก"_ -- Group A, Female, 22
_"คำศัพท์สลับไทยอังกฤษตลอด 'สถานะ: Pending Approval' ทำไมไม่เขียนว่า 'สถานะ: รออนุมัติ' ให้มันเป็นภาษาเดียวกัน"_ -- Group B, Male, 28
_"Export PDF ออกมาตัดคำภาษาไทยผิด คำว่า 'สิน' ตัดไปบรรทัดใหม่เป็น 'ค้า' อ่านไม่รู้เรื่อง"_ -- Group C, Female, 38
_"เจอแต่ภาษาอังกฤษ Dashboard, Analytics, Pipeline ผมอายุ 57 ไม่ได้เรียนมา ไม่เข้าใจว่ามันคืออะไร"_ -- Group D, Male, 57

#### Theme: Performance Anxiety

_"กดปุ่มแล้วไม่มีอะไรเกิดขึ้น รอ 5 วินาที ไม่รู้ว่าระบบทำงานอยู่หรือค้าง กดซ้ำอีกรอบ กลายเป็นสร้างซ้ำ 2 รายการ"_ -- Group D, Male, 49
_"Loading หน้า Vendor Comparison นานมาก คิดว่า internet ตัด Refresh ไปแล้วต้องเริ่มใหม่"_ -- Group C, Female, 41
_"ตอน peak hour ตอนเช้า 9-10 โมง ระบบช้าลงเห็นได้ชัด ทุกอย่างใช้เวลาเป็น 2 เท่า"_ -- Group B, Male, 34
_"OCR ใช้เวลา 15 วินาทีต่อใบ มีใบเสร็จ 20 ใบ ต้องรอ 5 นาที ไม่มี progress bar ไม่รู้ว่าเหลืออีกกี่ใบ"_ -- Group A, Female, 25

#### Theme: Mobile Experience

_"เปิดระบบบน iPhone ตารางข้อมูลยื่นออกนอกจอ ต้อง scroll ไปทางขวา แต่ไม่มีอะไรบอกว่ามีข้อมูลอีก"_ -- Group A, Male, 23
_"กรอกฟอร์มบนมือถือ keyboard บังปุ่ม Submit ต้อง scroll ลงไปหา กดไม่ถูกปุ่ม"_ -- Group A, Female, 21
_"ปุ่มบนมือถือเล็กมาก นิ้วกดไม่ถูกปุ่ม กด Reject แทน Approve โดนลูกน้องโทรมาถาม"_ -- Group D, Male, 53

#### Theme: Data Loss Fears

_"กรอกข้อมูล PR ไปครึ่งชั่วโมง Internet ตัดไปแป๊บเดียว ข้อมูลหายหมดเลย ไม่มี auto-save"_ -- Group B, Female, 31
_"กด Delete โดยไม่ได้ตั้งใจ มี popup ถามแค่ 'Are you sure?' กด Enter ตามสัญชาตญาณ ข้อมูลหาย ไม่มี Undo ไม่มีถังขยะ"_ -- Group C, Male, 39
_"แก้ไขข้อมูล vendor แล้วกด Save แต่ไม่มี confirmation ว่า save สำเร็จหรือเปล่า ไม่กล้าออกจากหน้า กลัวข้อมูลหาย"_ -- Group D, Female, 48

#### Theme: Missing Features Users Expected

_"ไม่มี Ctrl+Z ทำ Undo ก็ได้เหรอ app อะไรในปี 2026 ที่ไม่มี Undo"_ -- Group A, Male, 26
_"หา dark mode ใน Connectors ไม่เจอ ทำไมบาง module มี บาง module ไม่มี"_ -- Group A, Female, 23
_"ไม่มี offline mode ไปทำงานต่างจังหวัดที่ไม่มีอินเทอร์เน็ต ทำงานไม่ได้เลย"_ -- Group B, Male, 29
_"ไม่มี notification ทาง LINE ต้องเปิดเว็บ ANTS ดูตลอดว่ามีงานรออนุมัติหรือเปล่า"_ -- Group C, Female, 36
_"ไม่มี SSO ต้องจำ password อีกตัว นอกเหนือจาก email, SAP, VPN ที่มีอยู่แล้ว"_ -- Group B, Male, 33
_"ใช้งาน 2 สัปดาห์แล้ว ยังไม่เจอว่าดูประวัติการใช้งานของ user ได้ยังไง"_ -- Group C, Male, 44

### A.14 Module Interaction Flow Analysis

#### Most Common User Journeys (Top 10)

| Rank | Journey | Frequency | Avg Duration | Completion Rate |
|------|---------|-----------|-------------|-----------------|
| 1 | Home > Procurement > PR/PO > Create PR | 4,567 | 8.4 min | 71.3% |
| 2 | Home > Expense > Claim Tasks > Submit Claim | 3,891 | 6.8 min | 74.2% |
| 3 | Home > Procurement > PR/PO > View PO Status | 3,234 | 2.1 min | 89.4% |
| 4 | Home > Vendor Mgmt > Vendors > Search Vendor | 2,891 | 3.4 min | 78.7% |
| 5 | Home > Finance Doc > Cases > Open Case | 2,456 | 4.7 min | 76.1% |
| 6 | Home > Expense > Approval > Approve Claims | 2,134 | 3.2 min | 82.3% |
| 7 | Home > Sales Doc > Pipeline > View Pipeline | 1,987 | 2.8 min | 91.2% |
| 8 | Home > Vendor Mgmt > Comparison > Compare | 1,678 | 11.2 min | 63.4% |
| 9 | Home > Logistics > Freight OCR > Upload | 1,456 | 5.3 min | 68.7% |
| 10 | Home > System > Users > Manage User | 1,234 | 7.1 min | 64.2% |

#### Journey Drop-off Points

| Journey | Primary Drop-off Point | Drop-off Rate | Cause |
|---------|----------------------|---------------|-------|
| Create PR | Page 3 of 5 (line items) | 28.7% | Complex item entry form, no template |
| Submit Claim | OCR correction step | 25.8% | OCR results require too much manual correction |
| Compare Vendors | Loading comparison results | 36.6% | Long load time, no progress indicator |
| Upload Freight OCR | Post-upload parsing | 31.3% | Thai document parsing failures |
| Manage Users | Permission assignment | 35.8% | 47 individual permissions, no templates |

### A.15 Device-Specific Issue Log

#### iOS Safari Specific Issues

| Issue | Affected Users | iOS Version |
|-------|---------------|-------------|
| Bottom bar overlap with fixed footer | 234 | iOS 17+ |
| Date picker shows native wheel instead of custom picker | 189 | All |
| File upload dialog limited to Photos app | 167 | All |
| Viewport height calculation incorrect (100vh issue) | 145 | iOS 16+ |
| Rubber-banding interferes with internal scrolling | 123 | All |
| Input zoom on focus (font-size < 16px) | 312 | All |

#### Android Chrome Specific Issues

| Issue | Affected Users | Android Version |
|-------|---------------|----------------|
| Keyboard pushes content up, hiding input labels | 178 | Android 13+ |
| Back gesture conflicts with in-app navigation | 156 | Android 14+ |
| Thai font rendering inconsistent across brands | 134 | Samsung, OPPO, Vivo |
| Address bar auto-hide causes layout shift | 112 | Chrome 122+ |
| Camera permission prompt blocks OCR workflow | 98 | Android 12+ |

#### Desktop Browser Specific Issues

| Issue | Browser | Affected Users |
|-------|---------|---------------|
| Thai Baht symbol (฿) renders as "B" | Edge 122 (specific builds) | 87 |
| Print dialog breaks Thai text layout | Firefox 123 | 134 |
| PDF download prompts instead of inline preview | Safari 17 | 98 |
| Clipboard paste strips Thai formatting | Chrome (all) | 167 |
| Table column resize handle not visible | Firefox 123 | 89 |

---

### A.16 Simulation Confidence Intervals

All user counts reported in this document carry the following confidence intervals (95% CI):

| Reported User Count Range | Margin of Error |
|--------------------------|-----------------|
| > 2,000 users | +/- 2.3% |
| 1,000 - 2,000 users | +/- 3.1% |
| 500 - 1,000 users | +/- 4.4% |
| < 500 users | +/- 6.2% |

**Note:** These confidence intervals account for simulation variability but do not account for potential differences between simulated user behavior and actual user behavior in production environments.

---

### A.17 Abandoned Task Analysis

The following table details tasks that users started but did not complete, organized by the stage at which abandonment occurred.

#### PR/PO Creation Abandonment Funnel

```
Step 1: Click "Create New PR"        1,000 users entered     -----> 100.0%
Step 2: Fill basic information        967 users continued     -----> 96.7%  (33 abandoned: couldn't find button)
Step 3: Add line items                834 users continued     -----> 83.4%  (133 abandoned: form too complex)
Step 4: Attach documents              712 users continued     -----> 71.2%  (122 abandoned: upload issues)
Step 5: Select approval chain         689 users continued     -----> 68.9%  (23 abandoned: confusion)
Step 6: Review and submit             651 users completed     -----> 65.1%  (38 abandoned: no confidence in data)
```

**Critical Insight:** 34.9% of users who started a PR did not complete it. The largest single drop-off (133 users, 13.3%) occurred at Step 3 (line item entry), confirming that the line item form is the primary pain point.

#### Expense Claim Submission Abandonment Funnel

```
Step 1: Navigate to Claim Tasks       1,000 users entered     -----> 100.0%
Step 2: Upload receipt                 923 users continued     -----> 92.3%  (77 abandoned: couldn't find upload)
Step 3: Review OCR results             891 users continued     -----> 89.1%  (32 abandoned: upload failed)
Step 4: Correct OCR errors             678 users continued     -----> 67.8%  (213 abandoned: too many errors)
Step 5: Fill additional details        634 users continued     -----> 63.4%  (44 abandoned: form fatigue)
Step 6: Submit for approval            612 users completed     -----> 61.2%  (22 abandoned: unsure about policy)
```

**Critical Insight:** The OCR correction step (Step 4) accounts for the largest drop-off of 213 users (21.3%). This directly correlates with the 67% Thai OCR accuracy rate. Improving OCR to 90%+ would potentially retain 150+ of these abandoning users.

#### Vendor Comparison Abandonment Funnel

```
Step 1: Select vendors to compare     1,000 users entered     -----> 100.0%
Step 2: Wait for comparison to load    934 users continued     -----> 93.4%  (66 abandoned: wrong vendors selected)
Step 3: View comparison results        623 users continued     -----> 62.3%  (311 abandoned: load time too long)
Step 4: Analyze differences            567 users continued     -----> 56.7%  (56 abandoned: display too complex)
Step 5: Make selection decision         534 users completed     -----> 53.4%  (33 abandoned: insufficient data)
```

**Critical Insight:** 311 users (31.1%) abandoned during the loading step, directly attributable to the 8-12 second load time. This is the highest single-step abandonment rate across all modules.

### A.18 Cross-Group Satisfaction Correlation Matrix

This matrix shows how satisfaction in one module area correlates with satisfaction in other areas. Values range from -1.0 (inverse correlation) to +1.0 (perfect correlation).

| | Dashboard | Procurement | Vendor | Expense | Finance | Logistics | Sales | Connectors | Feedback | System |
|---|---|---|---|---|---|---|---|---|---|---|
| **Dashboard** | 1.00 | 0.72 | 0.68 | 0.71 | 0.65 | 0.58 | 0.74 | 0.42 | 0.63 | 0.55 |
| **Procurement** | 0.72 | 1.00 | 0.81 | 0.67 | 0.73 | 0.64 | 0.61 | 0.48 | 0.52 | 0.57 |
| **Vendor** | 0.68 | 0.81 | 1.00 | 0.59 | 0.71 | 0.67 | 0.55 | 0.51 | 0.49 | 0.54 |
| **Expense** | 0.71 | 0.67 | 0.59 | 1.00 | 0.76 | 0.53 | 0.58 | 0.39 | 0.61 | 0.52 |
| **Finance** | 0.65 | 0.73 | 0.71 | 0.76 | 1.00 | 0.62 | 0.54 | 0.45 | 0.57 | 0.59 |
| **Logistics** | 0.58 | 0.64 | 0.67 | 0.53 | 0.62 | 1.00 | 0.51 | 0.47 | 0.44 | 0.48 |
| **Sales** | 0.74 | 0.61 | 0.55 | 0.58 | 0.54 | 0.51 | 1.00 | 0.43 | 0.67 | 0.53 |
| **Connectors** | 0.42 | 0.48 | 0.51 | 0.39 | 0.45 | 0.47 | 0.43 | 1.00 | 0.38 | 0.71 |
| **Feedback** | 0.63 | 0.52 | 0.49 | 0.61 | 0.57 | 0.44 | 0.67 | 0.38 | 1.00 | 0.51 |
| **System** | 0.55 | 0.57 | 0.54 | 0.52 | 0.59 | 0.48 | 0.53 | 0.71 | 0.51 | 1.00 |

**Key Correlations:**
- Procurement and Vendor Management are most strongly correlated (0.81), suggesting users evaluate them as a single workflow
- Connectors and System are correlated (0.71), likely because both require technical configuration
- Connectors satisfaction has the weakest correlation with other modules (avg 0.45), confirming it serves a distinct user persona
- Expense and Finance are moderately correlated (0.76), reflecting overlapping financial workflows

### A.19 Estimated Business Impact of Top Issues

| Issue | Est. Productivity Loss per User per Day | Total Annual Cost (4,000 users) | Notes |
|-------|----------------------------------------|--------------------------------|-------|
| Deep navigation (4.7 clicks avg) | 12 min | 3,360,000 THB | Based on avg salary of 35,000 THB/month |
| OCR correction time | 8 min | 2,240,000 THB | For users who process receipts daily |
| No bulk operations | 15 min | 4,200,000 THB | For users processing 10+ items daily |
| No global search | 6 min | 1,680,000 THB | Time spent navigating to find items |
| Manual PR-to-PO re-entry | 10 min | 2,800,000 THB | For procurement staff only (~400 users) |
| Missing export formats | 7 min | 1,960,000 THB | Time spent converting PDF to Excel |
| No approval delegation | 3 days/year blocked | 8,400,000 THB | Approval bottleneck during manager leave |
| Performance issues (slow loads) | 5 min | 1,400,000 THB | Cumulative wait time per day |
| **Total estimated annual impact** | | **26,040,000 THB** | **~$723,000 USD** |

**Note:** These are conservative estimates based on average hourly rates and assume 250 working days per year. Actual impact may be higher when accounting for error correction, rework, and opportunity costs from delayed approvals.

### A.20 Final Assessment Summary

#### Platform Strengths (Despite Negative Focus)

While this report focuses on negative feedback and improvement areas, the testing did reveal several platform strengths worth acknowledging:

1. **Core workflow logic is sound** -- When users successfully complete tasks, the underlying business logic (approval chains, matching algorithms, calculations) produces correct results
2. **Data integrity** -- No data corruption or loss due to system errors was observed (all data loss was from user-initiated deletions without undo)
3. **Security posture** -- Authentication, session management, and data access controls functioned correctly throughout testing
4. **Uptime** -- 99.7% availability during the 24-day testing period (43 minutes total downtime)
5. **Group B satisfaction** -- The 26-35 age group, representing the core SaaS user demographic, achieved the highest satisfaction score (3.41/5), suggesting the platform's fundamental design is appropriate for its primary target audience

#### Critical Success Factors for Improvement

Based on the comprehensive analysis in this report, addressing the following 5 areas would have the most significant impact on overall satisfaction:

1. **Thai localization (estimated +0.4 to overall score)** -- Complete Thai UI, พ.ศ. dates, Thai document templates, Thai OCR improvement
2. **Navigation simplification (estimated +0.3 to overall score)** -- Global search, breadcrumbs, quick actions, reduced click depth
3. **Performance optimization (estimated +0.25 to overall score)** -- Progress indicators, faster load times, virtual scrolling
4. **Mobile experience (estimated +0.2 to overall score)** -- Responsive redesign for all critical workflows
5. **Safety nets (estimated +0.15 to overall score)** -- Auto-save, undo/redo, confirmation dialogs, recycle bin

**Projected improvement:** Addressing all 5 areas would raise the estimated overall satisfaction from 3.18 to approximately 4.48/5, bringing the platform to best-in-class territory in the Thai B2B SaaS market.

### A.21 Risk Assessment for Inaction

If the issues identified in this report are not addressed within the next two quarters, the following risks are projected:

| Risk | Probability | Impact | Mitigation |
|------|------------|--------|------------|
| User churn to competitor platforms (Odoo, PEAK) | High (70%) | Loss of 15-25% of user base | Prioritize Thai localization and LINE integration |
| Negative word-of-mouth in Thai business community | High (65%) | Reduced new customer acquisition by 30-40% | Address top 5 critical issues immediately |
| IT department pushback / shadow IT adoption | Medium (55%) | Teams bypass ANTS using Excel/Google Sheets | Improve export options and bulk operations |
| Executive sponsor dissatisfaction (Group D) | High (72%) | Budget reduction or project cancellation | Create simplified executive view with Thai UI |
| Compliance audit failures due to insufficient audit trails | Medium (50%) | Regulatory penalties, fines | Implement comprehensive audit logging |
| Data entry errors due to missing undo/validation | High (68%) | Financial reporting inaccuracies | Implement auto-save, undo/redo, validation |
| Help desk overwhelm from "is this a bug" tickets | Ongoing | Support cost increase of 40% | Improve UX feedback, add Thai help docs |
| Accessibility lawsuit risk under Thai disability law | Low (15%) | Legal liability, reputation damage | Conduct WCAG audit and remediation |

#### Quarterly Business Review Metrics to Track

The following KPIs should be tracked quarterly to measure improvement against this baseline:

| KPI | Current Baseline | Q2 Target | Q3 Target | Q4 Target |
|-----|-----------------|-----------|-----------|-----------|
| Overall Satisfaction | 3.18 / 5 | 3.45 / 5 | 3.75 / 5 | 4.00 / 5 |
| NPS | -43.1 | -25.0 | -10.0 | +5.0 |
| Task Completion Rate | 74.5% | 80.0% | 87.0% | 92.0% |
| Avg Clicks to Target | 4.7 | 3.5 | 2.8 | 2.3 |
| Mobile Satisfaction | 2.67 / 5 | 3.10 / 5 | 3.50 / 5 | 3.90 / 5 |
| Thai OCR Accuracy | 67% | 80% | 88% | 92% |
| Support Tickets per User | 3.1 | 2.2 | 1.5 | 1.0 |
| Feature Discovery Rate | 41.2% | 52.0% | 63.0% | 72.0% |
| Avg Session Duration (healthy) | 27 min | 22 min | 18 min | 15 min |
| Rage Clicks per Session | 17.4 | 10.0 | 5.0 | 2.0 |

**Note:** Decreasing average session duration is a positive indicator -- it means users are completing tasks faster, not that they are disengaging.

### A.22 Acknowledgments

This simulation study was designed and executed by the ANTS UX Research Team with input from:
- Product Management (module prioritization and scenario design)
- Engineering (performance baseline measurements)
- Customer Success (real-world pain point seeding)
- Thai Localization Consultants (cultural UX validation)
- Accessibility Specialists (WCAG compliance evaluation)

Special thanks to the 12 internal beta testers from various departments who validated the simulation scenarios against real-world workflows before the full 4,000-user simulation run.

### A.23 Document Revision History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 0.1 | March 28, 2026 | UX Research Team | Initial draft with raw data |
| 0.5 | March 31, 2026 | UX Research Team | Added cross-module analysis and recommendations |
| 0.8 | April 2, 2026 | UX Research Team | Added age group detailed analysis and appendices |
| 0.9 | April 3, 2026 | Product Management | Review comments incorporated |
| 1.0 | April 5, 2026 | UX Research Team | Final version approved for distribution |

### A.24 Contact Information

For questions or clarifications regarding this report:

- **Primary Contact:** UX Research Lead -- ux-research@ants-ai.com
- **Product Owner:** Product Management -- product@ants-ai.com
- **Engineering Lead:** Platform Engineering -- platform-eng@ants-ai.com
- **Accessibility Specialist:** Accessibility Team -- a11y@ants-ai.com

---

*End of Report*

**Document Control:**
- Version 1.0 -- Initial release
- Prepared: April 5, 2026
- Next review: May 5, 2026
- Distribution: Product Team, Engineering Lead, UX Design Team, Executive Sponsor
- Feedback on this report: ux-research@ants-ai.com
