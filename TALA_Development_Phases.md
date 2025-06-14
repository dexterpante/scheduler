
# 📘 TALA Development Phases  
**Teacher and cLassroom Allocation Assistant**

---

## ✅ Phase 1: Core Scheduler MVP

### Scope
Develop a minimum viable product (MVP) for a Senior High School class scheduler that can:
- Assign teachers to subjects based on specialization (major/minor).
- Allocate classrooms based on class size and room capacity.
- Generate conflict-free schedules across 5 weekdays and 8–10 periods/day.
- Enforce DepEd-standard constraints (e.g., ≤6 hours/day, ≤30 hours/week per teacher).
- Identify gaps in assignments and provide system-generated recommendations.

### Features
- 📥 Upload/Manual entry of:
  - **Teachers** (ID, major, minor)
  - **Classrooms** (ID, capacity)
  - **Subjects/Sections** (ID, subject, enrollment, grade)
- 🧠 Schedule generation using PuLP optimizer
- 🔍 Gap analysis and recommendations:
  - e.g., "No qualified teacher for subject X"
  - e.g., "Add room with capacity ≥ 45"

### Outputs
- Schedule table (teacher, section, subject, room, day, period)
- Gap and resource analysis
- Recommendations to school heads

### Tools
- `schedulerv3.py` (Streamlit)
- `schedulerplus.py` (PyQt5 Desktop)
- SHS Consultation Packet Curriculum alignment

---

## 🚧 Phase 2: Learner & Workload Management

### Scope
Enhance TALA by integrating student demand and workload transparency.

### Features
- 🧮 **Learner Tab**: Input enrollment per grade/subject
- ➗ **Automatic Section Calculation**: Based on class size limits
- 📤 **Section to Subject Mapping**: Create required section-subject combinations
- ⚖️ **Teacher Workload Viewer**: Total load per teacher visualized
- 📝 **Editable Schedules**: Allow manual override of generated outputs
- 📎 Linkage to constraints (e.g., only assign if teacher has not exceeded load)

### Additions
- Persistent session state in Streamlit
- Editable tables in all tabs
- User-adjustable limits for sections per grade

---

## 🚀 Phase 3: Evaluation, Mobile, and Integration

### Scope
Create feedback mechanisms, mobile deployment, and DepEd system integrations.

### Features
- 📲 **QR-based Schedule Evaluation**:
  - QR codes per schedule
  - Expiry-based feedback forms (midyear/end-year)
- 🧾 **DTR Template Integration**:
  - Generate monthly DTR summaries
  - Allow capture via mobile photo upload
- 📡 **System Integrations**:
  - Option to link with LIS, HRIS, or school EMIS
- 📊 **Admin Dashboards**:
  - Teacher utilization
  - Classroom bottlenecks
  - Curriculum gaps vs. demand

### Mobile/Offline
- PyInstaller version for school-level desktop use
- Optional mobile-first UI for faculty access

---

## 🔚 Summary
TALA evolves from a simple scheduler into a school planning assistant, bridging human resource deployment, student demand, and infrastructure gaps through automation and AI-driven analysis.

