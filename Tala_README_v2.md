
# Tala: Teacher and cLassroom Allocation Assistant

**Tala** is a smart, data-driven tool designed to help Philippine schools and divisions efficiently plan and generate class schedules. From optimizing teacher assignments to identifying planning gaps and projecting learning outcomes, Tala empowers education managers with powerful insights and automation.

---

## 🌍 Project Description
Tala simplifies the complex task of teacher and classroom scheduling and elevates it into a full-scale planning and decision-support system. It aligns with DepEd policies, supports ESF-7 reporting, and forecasts the impact of resource mismatches on learning outcomes.

---

## 🔹 Key Features by Phase

### ● Phase 1: Basic Scheduler (Standalone)
- Assign teachers to sections based on specialization
- Prevent conflicts in teacher schedules and room assignments
- Max daily/weekly hours per teacher
- Manual and CSV upload options
- GUI via PyQt5 or Streamlit
- Subject data capture including:
  - Subject name
  - Number of times taught per week
  - Duration per session

### ● Phase 2: School-Level Planning, Gap Analysis, and Impact Simulation
- Input learner demand and compute required sections
- Detect constraint violations:
  - Teachers handling non-specialized subjects
  - Overloaded classrooms
  - Overscheduled teachers
- Determine if a school is overcapacity (too many enrollees, not enough rooms or teachers) or undercapacity
- Estimate impact on learning outcomes:
  - e.g., "23% of assignments handled by non-specialists may reduce NAT scores by ~10%"
  - e.g., "Overcapacity may reduce classroom engagement and increase dropout risk"
- Recommend interventions: merge/split sections, reassign teachers, implement shifts
- Generate ESF-7-aligned reports
- Provide school-level diagnostic dashboard

### ● Phase 3: Division-Level Consolidation, Strategic Deployment, and School Readiness Index
- Consolidate data from multiple schools
- Aggregate and map:
  - Schools with overcapacity (excess enrolment, insufficient teachers/rooms)
  - Schools with undercapacity (few learners, underused teachers or facilities)
- Division-wide learning impact simulation (e.g., "Your division may see a 4.2% decline in NAT Math scores")
- Suggest managing enrolment through:
  - Redistribution
  - Resource allocation
  - Inter-school teacher redeployment
- Compute and report the School Readiness Index (SRI) based on:
  - Teacher gap
  - Classroom adequacy
  - Specialization match
  - Projected learning risks
- Visual dashboard, printable memos, and exportable ESF7 summaries

### ● Phase 4: Mobile Interface, Feedback & Attendance
- Mobile access to teacher schedules
- QR-code based feedback on workload satisfaction (midyear and year-end)
- Upload photos of DTRs to summarize monthly attendance
- No storage of daily logs for privacy and scale

### ● Phase 5: AI-Powered Optimization
- Switchable scheduling engine: PuLP, Genetic Algorithm, OptaPy, OR-Tools
- Auto-learn optimal load distribution patterns
- Predict gaps and recommend plantilla adjustments
- Adaptive engine for real-time reallocation

---

## 📝 Installation and Setup

1. Clone the repo:
```bash
git clone https://github.com/your-repo/tala-scheduler.git
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Run the app:
```bash
# For Streamlit version
streamlit run schedulerv3.py

# For PyQt5 version
python schedulerplus.py
```

---

## ✨ Example Use Cases
- A School Head simulates teacher load and classroom demand before class opening
- A Division Planning Officer reallocates teachers using dashboard insights and SRI scores
- A Teacher provides feedback via QR code at the end of the semester
- A Clerk uploads monthly DTR photo summaries for teacher monitoring

---

## 📊 Future Roadmap
- Integration with LIS and HRIS
- Real-time data sync across schools and division dashboard
- Learning outcome prediction engine
- Printable supervision and TA reports
- Web and mobile dashboards for DepEd RO and CO planners

---

## 💼 Contributors
- Dexter Pante (Project Lead, DepEd School Effectiveness Division)
- [Your Name Here] (Lead Developer)
- [OpenAI GPT-4o] (AI Assistant)

---

## 🌟 Icon and Identity
TALA stands for **Teacher and cLassroom Allocation Assistant**. The icon features a modern design combining a teacher, a classroom board, and interconnected schedule blocks to symbolize intelligent planning.

---

## 📄 License
[MIT License or specify here]
