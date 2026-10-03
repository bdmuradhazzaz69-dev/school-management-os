🏫 SCHOOL MANAGEMENT APP

Master Product Blueprint — V1.0

বিদ্যালয়: ২ নং বালক সরকারি প্রাথমিক বিদ্যালয়
শ্রেণি: প্রথম → পঞ্চম
Platform: Android-first, Mobile-first
Product Type: School Operating System
Core Principle: One Student → One Master Profile → One Permanent Student ID

---

1. PRODUCT VISION

এই অ্যাপটি শুধু Student Information বা Attendance App হবে না।

এটি হবে বিদ্যালয়ের একটি পূর্ণাঙ্গ School Operating System, যেখানে একসঙ্গে থাকবে:

- Student Management
- Academic Management
- Teacher Workflow
- Attendance
- Learning Assessment
- Homework & Diary
- Examination & Result
- Parent Communication
- Special Classes & Groups
- Achievement & Portfolio
- Principal Monitoring
- Reports
- Notifications
- Security
- Privacy
- Audit
- Backup
- Offline-first operation

মূল উদ্দেশ্য

প্রধান শিক্ষক যেন কয়েক মিনিটের মধ্যে জানতে পারেন:

«আজ স্কুলে কী অবস্থা?
কে অনুপস্থিত?
কোন শিক্ষক/ক্লাসে সমস্যা আছে?
কোন lesson পিছিয়ে আছে?
কোন শিক্ষার্থীর অতিরিক্ত সহায়তা প্রয়োজন?
কোন homework pending?
কোন গুরুত্বপূর্ণ follow-up করতে হবে?»

---

2. SIX CORE PILLARS

1. Admin Management

স্কুলের master data, users, classes, subjects, settings।

2. Teacher Workflow

Teacher-এর প্রতিদিনের কাজ 10–20 taps-এর মধ্যে সম্পন্ন করার লক্ষ্য।

3. Principal Command Center

পুরো স্কুলের real-time operational picture।

4. Parent Access

Verified guardian → নিজের সন্তানের তথ্য।

5. Student Access

শিক্ষার্থী → নিজের academic journey।

6. Privacy & Security

শিশুদের তথ্যের জন্য strict role-based access।

---

3. USER ROLES

ADMIN

ম্যানেজ করবে:

- Students
- Teachers
- Classes
- Sections
- Subjects
- Academic Year
- Routine
- Users
- Permissions
- Special Classes
- Groups
- Projects
- Attendance
- Homework
- Learning
- Exams
- Results
- Notices
- Reports
- Backup
- Audit

PRINCIPAL

Principal হবে School Command Center-এর প্রধান user।

দেখতে পারবে:

- Whole-school dashboard
- Student overview
- Teacher status
- Attendance
- Teaching progress
- Homework
- Learning progress
- Results
- Alerts
- Calendar
- Reports
- Classroom observation
- Special programs
- Audit summary

TEACHER

Teacher দেখতে/করতে পারবে:

- My Classes
- Attendance
- Lesson
- Homework
- Diary
- Learning Record
- Student Support
- Special Classes
- Groups
- Projects

Teacher অপ্রয়োজনীয় private data দেখতে পারবে না।

STUDENT

Student দেখতে পারবে:

- My Profile
- My Class
- Routine
- Attendance
- Homework
- Diary
- Results
- Special Classes
- Groups
- Projects
- Achievements
- Timeline

PARENT

Parent প্রথমে verification করবে।

তারপর শুধু নিজের সন্তানের:

- Attendance
- Homework
- Diary
- Learning Status
- Result
- Notice
- Calendar
- Important Alert

দেখতে পারবে।

---

4. AUTHENTICATION SYSTEM

Login Types

Staff

Admin / Principal / Teacher

Student

Student ID + approved authentication method

Parent

Verified guardian mobile number + OTP

Security

OTP:

- Short expiry
- Attempt limit
- Rate limit
- One-time use
- Re-verification when required

Session:

- Secure session
- Refresh-token protection
- Logout
- Session revocation
- Device/session management

---

5. SCHOOL PROFILE

School master profile:

- School Name
- School Code
- Address
- Contact
- Classes
- Academic Year
- School Photos
- Basic Information
- School Calendar
- Working Days

School: ২ নং বালক সরকারি প্রাথমিক বিদ্যালয়

অ্যাপে supplied school-building reference photos school identity section-এ ব্যবহার করা যাবে।

---

6. STUDENT MASTER PROFILE

এটাই পুরো সিস্টেমের সবচেয়ে গুরুত্বপূর্ণ অংশ।

Rule

«একজন শিক্ষার্থী = একটি Master Profile = একটি Permanent Student ID»

Student Class 1 থেকে Class 5 পর্যন্ত একই profile-এর মধ্যে থাকবে।

Identity

- Student ID
- Name
- Photo
- Date of Birth
- Gender যেখানে প্রয়োজন/আইনসম্মত
- Admission information
- Basic identity fields

Academic Placement

- Academic Year
- Class
- Section
- Roll
- Status

Guardian

- Guardian name
- Relationship
- Approved contact
- Verification status
- Authorization record

Academic History

- Class history
- Section history
- Attendance
- Lesson-related learning records
- Homework
- Diary
- Assessment
- Result

Enrichment

- Special Class
- Study Group
- Project
- Scholarship
- Achievement
- Portfolio

Timeline

Class 1 → Class 5-এর পুরো journey।

---

7. DUPLICATE STUDENT PREVENTION

নতুন student তৈরি করার সময় system সম্ভাব্য duplicate শনাক্ত করবে।

Matching fields:

- Student ID
- Name
- DOB যেখানে applicable
- Guardian information
- Existing school record
- Other approved matching fields

Potential duplicate পাওয়া গেলে:

«“সম্ভাব্য একই শিক্ষার্থীর রেকর্ড পাওয়া গেছে।”»

তারপর Admin যাচাই করবে।

---

8. ACADEMIC STRUCTURE

Hierarchy:

School
→ Academic Year
→ Class
→ Section
→ Subject
→ Teacher
→ Student

Regular Class এবং Special Class আলাদা entity।

Study Group-ও আলাদা।

একজন student একই সঙ্গে:

- Regular Class
- Special Class
- Study Group

এর সদস্য হতে পারবে।

---

9. CLASS & SECTION

Class:

- First
- Second
- Third
- Fourth
- Fifth

Section:

- Section Name
- Class Teacher
- Students
- Subjects
- Routine

Validation:

- একই class/section-এ duplicate roll নয়
- invalid teacher assignment নয়
- inactive student ভুল class-এ থাকবে না

---

10. SUBJECT MASTER

Subject entity:

- Subject ID
- Subject Name
- Class
- Academic Year
- Active status

Teacher assignment:

- Teacher
- Class
- Section
- Subject

---

11. ROUTINE ENGINE

Weekly routine:

- Day
- Period
- Class
- Section
- Subject
- Teacher
- Room
- Special Activity

Teacher View

“My Routine”

Student View

“My Class Routine”

Principal View

“School Routine”

---

12. ANNUAL TEACHING PLAN

Fields:

- Class
- Subject
- Month
- Chapter/Unit
- Topic
- Planned Date
- Completed Date
- Status

Status:

- Planned
- In Progress
- Completed
- Delayed

Dashboard:

Planned vs Completed vs Delayed

---

13. LESSON RECORD

Teacher প্রতিটি lesson-এর record রাখতে পারবে।

Fields:

- Class
- Section
- Subject
- Chapter
- Topic
- Date
- Lesson Summary
- Homework
- Next Lesson Preparation

Principal দেখতে পারবেন:

- কোন class এগিয়ে
- কোন class পিছিয়ে
- কোন lesson pending

---

14. ATTENDANCE SYSTEM

Status:

- Present
- Absent
- Late

Teacher flow:

My Class → Attendance → Select Date → Mark → Review → Submit

Bulk attendance থাকবে।

একজন একজন করে করার প্রয়োজন কমানো হবে।

Analytics

- Daily
- Weekly
- Monthly
- Term
- Yearly

Early Warning

System detect করতে পারবে:

- Repeated absence
- Consecutive absence
- Unusual pattern
- Sudden attendance drop

কিন্তু label হবে:

«Follow-up Required»

“Problem Student” বা public negative label ব্যবহার করা হবে না।

---

15. ABSENCE FOLLOW-UP

Record:

- Parent contacted?
- Reason reported
- Follow-up required?
- Action taken
- Next review date

অপ্রয়োজনীয় medical details সংরক্ষণ করা যাবে না।

---

16. TEACHER ATTENDANCE & AVAILABILITY

Status:

- Present
- Leave
- Official Duty
- Absent
- Available
- Substitute Needed

Principal dashboard-এ দেখা যাবে:

«আজ কোন teacher available?»

---

17. SUBSTITUTE PLANNER

Flow:

Class → Period → Subject → Substitute Teacher

তারপর:

- Updated routine
- Workload
- Class activity

---

18. TEACHER WORKLOAD

System দেখাবে:

- Classes
- Subjects
- Period count
- Special classes
- Group responsibilities
- Project responsibilities

এটি monitoring-এর জন্য।

Teacher ranking তৈরি করার জন্য নয়।

---

19. LEARNING ENGINE

শুধু marks নয়।

Learning status:

- খুব ভালো
- ভালো
- অনুশীলন প্রয়োজন
- অতিরিক্ত সহায়তা প্রয়োজন

Curriculum-approved competency থাকলে:

- Reading
- Writing
- Numeracy
- Problem Solving
- Communication
- Participation
- Practical Activity

---

20. LEARNING EVIDENCE

Evidence type:

- Observation
- Class Activity
- Short Task
- Oral Response
- Written Work
- Project
- Practice Result

Learning status evidence-based হবে।

---

21. LEARNING GAP

System কোনো pattern detect করলে:

«“অতিরিক্ত অনুশীলন প্রয়োজন”»

ধরনের actionable flag তৈরি করবে।

কোনো শিশুকে publicভাবে “দুর্বল” হিসেবে label করা হবে না।

---

22. STUDENT SUPPORT PLAN

Fields:

- Need
- Intervention
- Responsible Teacher
- Start Date
- Review Date
- Outcome

এই তথ্য restricted access-এর মধ্যে থাকবে।

---

23. HOMEWORK

Fields:

- Class
- Section
- Subject
- Task
- Description
- Date
- Deadline
- Attachment

Status:

- New
- Pending
- Completed
- Late

---

24. DIGITAL SCHOOL DIARY

প্রতিদিন:

Today

- What was taught
- Homework
- Teacher note

Tomorrow

- Preparation

Student এবং Parent প্রয়োজনীয় অংশ দেখতে পারবে।

---

25. EXAM ENGINE

Exam:

- Exam Name
- Class
- Subject
- Date
- Syllabus/Coverage
- Full Marks
- Approved criteria

---

26. RESULT WORKFLOW

Result lifecycle:

Draft
→ Teacher Entry
→ Verification
→ Approval
→ Publish

Published result পরিবর্তন:

Change Request
→ Authorization
→ Update
→ Audit Log

---

27. RESULT ANALYTICS

Principal দেখতে পারবেন:

- Class average
- Subject overview
- Distribution
- Trend
- Support areas

Teacher “best/worst” ranking তৈরি করা হবে না।

---

28. SPECIAL CLASS

Examples:

- Remedial
- Enrichment
- Scholarship Preparation
- Subject Support
- Special Exam
- Training

Structure:

- Name
- Type
- Description
- Teacher
- Schedule
- Members
- Attendance
- Homework
- Materials
- Exam
- Result

---

29. STUDY GROUP

Example:

Math Group Study

Fields:

- Group Name
- Subject
- Members
- Teacher
- Schedule
- Activity
- Progress

---

30. PROJECT GROUP

Fields:

- Project
- Team
- Members
- Role
- Task
- Deadline
- Submission
- Assessment

---

31. SCHOLARSHIP

Fields:

- Scholarship Name
- Eligibility
- Selected Students
- Preparation Batch
- Exam
- Marks
- Result
- Achievement

---

32. ACHIEVEMENT

Categories:

- Academic
- Scholarship
- Sports
- Quiz
- Drawing
- Debate
- Cultural
- Competition
- School Achievement

প্রতিটি achievement-এ থাকবে:

- Title
- Date
- Category
- Description
- Verified By
- Verification Date
- Certificate/Attachment যেখানে applicable

---

33. STUDENT TIMELINE

Student timeline হবে:

Admission
→ Class Change
→ Attendance Events
→ Learning
→ Homework
→ Special Class
→ Group
→ Project
→ Exam
→ Result
→ Achievement

এটাই হবে student's longitudinal journey।

---

34. STUDENT PORTFOLIO

Class 1–5 পর্যন্ত:

- Learning
- Result
- Attendance
- Projects
- Achievements
- Certificates

এক জায়গায়।

---

35. PRINCIPAL COMMAND CENTER

Principal Home-এর মূল অংশ:

TODAY'S SCHOOL

Cards:

- Total Students
- Present
- Absent
- Late
- Attendance %
- Teacher Status
- Classes Running
- Lesson Progress
- Homework Pending
- Important Notices
- Upcoming Events
- Open Alerts

---

36. 5-MINUTE PRINCIPAL VIEW

Five sections:

1. Attendance

আজ উপস্থিতির অবস্থা।

2. Teaching

কোন lesson চলছে/পিছিয়ে আছে।

3. Learning

কোথায় support প্রয়োজন।

4. Student Follow-up

কাদের follow-up প্রয়োজন।

5. Operations

Teacher availability, substitute, events, pending tasks।

---

37. SMART ALERTS

Alert হবে actionable।

Example:

«“রহিম — গত ১৪ দিনে ৫ দিন অনুপস্থিত।”»

Button:

Follow-up

---

«“Class 4 — ৮ students homework incomplete।”»

Button:

View Students

---

«“Class 3 Math — ১১ students need extra practice।”»

Button:

View Learning

---

«“Class 2-ক — lesson record pending।”»

Button:

Review

---

38. NOTIFICATION SYSTEM

Target:

- All School
- Teachers
- Students
- Parents
- Specific Class
- Special Class

Priority:

- Normal
- Important
- Urgent

Notification history থাকবে।

---

39. SCHOOL CALENDAR

Event:

- School Day
- Holiday
- Exam
- Parent Meeting
- Sports
- Cultural Program
- Scholarship
- Special Class
- Staff Meeting

---

40. PARENT HOME

MY CHILD TODAY

এক নজরে:

- Attendance
- Homework
- Diary
- Learning Status
- Upcoming Exam
- Notice
- Important Alert

Parent অন্য student's তথ্য দেখতে পারবে না।

---

41. PARENT FEEDBACK

Categories:

- Feedback
- Suggestion
- Complaint

Status:

- Submitted
- Received
- Under Review
- Resolved

---

42. DIRECTORY & PRIVACY

Authorized directory:

Class → Section → Student

Minimum:

- Name
- Class
- Section
- Roll

Photo optional এবং controlled।

Public student directory থাকবে না।

---

43. SCHOOL ADMINISTRATION

Phase অনুযায়ী:

Core

- School Profile
- Academic Year
- Classes
- Teachers
- Subjects
- Calendar
- Notices

Future

- Resources
- Library
- Facility
- ICT
- Safety
- Infrastructure checklist

---

44. FACILITY MANAGEMENT

Track:

- Classroom
- Electricity
- Water
- Sanitation
- Playground
- Library
- ICT
- Safety

---

45. REPORT CENTER

Daily

- Attendance
- Teacher status
- Lesson
- Alerts

Weekly

- Attendance trend
- Homework
- Learning
- Teacher activity

Monthly

- Class performance
- Attendance
- Learning gap
- Result
- Special programs

Yearly

- Student journey
- Progress
- Achievement
- Academic summary

Filters:

- Academic Year
- Class
- Section
- Subject
- Teacher
- Date range
- Student

Export:

- In-App
- PDF
- Print
- Spreadsheet/CSV
- Archive

---

46. DATA QUALITY ENGINE

System automatically check করবে:

- Duplicate student
- Missing roll
- Duplicate roll
- Invalid teacher assignment
- Missing guardian contact
- Missing attendance
- Missing result
- Conflicting academic year

Completeness Dashboard

- Attendance %
- Lesson Record %
- Homework %
- Diary %

---

47. DATA CORRECTION

Critical correction:

Request → Verify → Update → Audit

Student ID বা published result-এর মতো critical field সরাসরি overwrite করা যাবে না।

---

48. OFFLINE-FIRST ARCHITECTURE

Teacher-এর essential কাজ internet না থাকলেও চলবে।

Offline-supported:

- Attendance
- Lesson Record
- Homework
- Basic Assessment

Architecture:

Device
→ Secure Local Queue
→ Server
→ Confirmed Sync

Conflict হলে user-কে জানানো হবে।

Silent overwrite হবে না।

---

49. DATABASE ARCHITECTURE

Core entities:

School
AcademicYear
Student
Guardian
Teacher
User
Role
Permission
Class
Section
Subject
Routine
Curriculum
Lesson
Attendance
LearningRecord
Homework
Diary
Exam
Result
SpecialClass
StudyGroup
Project
Scholarship
Achievement
Notice
Notification
CalendarEvent
Leave
Incident
Report
AuditLog
ConsentAuthorization
DataRetention

সবচেয়ে গুরুত্বপূর্ণ relation

Student
   │
   ├── Class History
   ├── Attendance
   ├── Learning
   ├── Homework
   ├── Diary
   ├── Assessment
   ├── Result
   ├── Special Class
   ├── Study Group
   ├── Project
   ├── Scholarship
   ├── Achievement
   ├── Portfolio
   └── Timeline

সবকিছু Student ID-এর সঙ্গে linked থাকবে।

---

50. PERMISSION ARCHITECTURE

Security model:

User
→ Role
→ Permission
→ Resource
→ Action

Actions:

- View
- Create
- Edit
- Delete
- Approve
- Publish
- Export
- Archive
- Restore

High-risk actions-এর জন্য extra permission।

---

51. AUDIT LOG

প্রতিটি গুরুত্বপূর্ণ পরিবর্তনের record:

- Who
- What
- When
- Record
- Previous Value
- New Value
- Reason

বিশেষ করে:

- Student ID
- Guardian verification
- Published result
- User role
- Sensitive export
- Archive/restore
- Important profile change

---

52. SECURITY

Must-have:

- Encryption in transit
- Encryption at rest where supported
- Strong password hashing
- Least privilege
- Secure backup
- Server access logging
- Session security
- OTP protection
- Role-based access

---

53. CHILD DATA PRIVACY

নীতি:

- Data minimization
- Purpose limitation
- Controlled access
- Retention policy
- Archive policy
- Correction workflow
- Deletion workflow যেখানে আইন/নীতিতে প্রযোজ্য
- Consent/authorization records যেখানে প্রয়োজন

কোনো unnecessary:

- GPS tracking
- Advertising
- Commercial profiling
- Surveillance

থাকবে না।

---

54. INCIDENT / SENSITIVE RECORD

Restricted incident workflow:

- Date
- Category
- Factual Description
- Authority
- Action
- Follow-up

Public label নয়।

Sensitive information শুধু authorized role দেখতে পারবে।

---

55. EMERGENCY INFORMATION

শুধু প্রয়োজনীয়:

- Authorized emergency contact
- Contact status
- Emergency instruction

Sensitive medical information অত্যন্ত restricted থাকবে এবং প্রয়োজনীয়/আইনসম্মত ভিত্তি ছাড়া রাখা হবে না।

---

56. ACCESSIBILITY

UI হবে:

- Large touch targets
- Readable typography
- Clear labels
- Good contrast
- Screen-reader aware
- Color-only indication নয়
- Simple navigation
- Understandable error messages

বাংলা Unicode পুরোপুরি support করতে হবে।

---

57. NAVIGATION

Admin

Home | Students | Classes | Reports | More

Principal

Home | School | Academic | Reports | More

Teacher

Home | My Classes | Students | Attendance | More

Student

Home | My Profile | Classes | Homework | More

Parent

Home | My Child | Notices | Calendar | Profile

---

58. ANDROID APP SCREEN MAP

AUTH

1. Splash
2. Welcome
3. Login
4. Staff Login
5. Teacher Login
6. Parent Access
7. OTP Verification
8. Student Login
9. First Setup
10. Session Management
11. Logout

ADMIN

12. Admin Dashboard
13. Student List
14. Add Student
15. Student Profile
16. Teacher List
17. Teacher Profile
18. Class
19. Section
20. Subject
21. Academic Year
22. Routine
23. Users
24. Roles
25. Permissions
26. School Settings
27. Backup
28. Audit Log

PRINCIPAL

29. Principal Dashboard
30. Attendance Overview
31. Teacher Status
32. Teaching Progress
33. Learning Overview
34. Student Follow-up
35. Alerts
36. Reports
37. Calendar
38. Notices
39. Classroom Observation

TEACHER

40. Teacher Home
41. My Classes
42. Class Students
43. Attendance
44. Lesson Record
45. Homework
46. Diary
47. Learning Record
48. Student Support
49. Special Class
50. Study Group
51. Project
52. Teacher Availability
53. Substitute

STUDENT

54. Student Home
55. My Profile
56. My Class
57. Routine
58. Attendance
59. Homework
60. Diary
61. Result
62. Special Class
63. Group
64. Project
65. Achievement
66. Portfolio
67. Timeline

PARENT

68. Parent Home
69. Child Profile
70. Attendance
71. Homework
72. Diary
73. Learning
74. Result
75. Notice
76. Calendar
77. Feedback

---

59. UI/UX PRINCIPLES

App হবে:

- Clean
- Fast
- Bangla-friendly
- Low cognitive load
- Mobile-first
- Minimal typing
- Large action buttons
- Search + Filter
- Quick actions
- Dashboard cards
- Bottom navigation
- Confirmation for risky actions

Teacher-এর daily workflow-এ unnecessary screens কমাতে হবে।

---

60. HOME SCREEN QUICK ACTIONS

Teacher:

Attendance | Lesson | Homework | Learning

Principal:

Attendance | Teaching | Alerts | Reports

Parent:

My Child Today

Student:

Today | Homework | Routine | Result

---

61. MVP — FIRST RELEASE

Foundation

- Authentication
- Roles
- Permissions
- School Profile
- Student Master Profile
- Student ID
- Teacher
- Class
- Section

Academic

- Subject
- Routine
- Annual Plan
- Attendance
- Lesson
- Learning
- Homework
- Diary
- Exam
- Result

Parent

- Parent Access
- OTP
- Child Profile
- Attendance
- Homework
- Result
- Notice

Administration

- Principal Dashboard
- Reports
- Alerts
- Audit Log

Special Programs

- Special Class
- Study Group
- Achievement

Safety

- Privacy
- Security
- Backup
- Validation

---

62. DEVELOPMENT PHASES

PHASE 0 — DISCOVERY & GOVERNANCE

- Workflow mapping
- Roles
- Data inventory
- Privacy
- Approval
- Existing records
- Academic year
- IPEMIS coexistence

PHASE 1 — FOUNDATION

- Database
- Authentication
- RBAC
- School
- Student
- Teacher
- Class
- Section

PHASE 2 — DAILY OPERATIONS

- Routine
- Attendance
- Teacher availability
- Substitute
- Lesson
- Homework
- Diary

PHASE 3 — LEARNING ENGINE

- Assessment
- Learning Record
- Learning Gap
- Remedial
- Support Plan
- Curriculum coverage

PHASE 4 — RESULT & COMMUNICATION

- Exam
- Result
- Parent OTP
- Notice
- Notification
- Calendar

PHASE 5 — ADVANCED ACADEMIC

- Special Class
- Study Group
- Project
- Scholarship
- Achievement
- Portfolio
- Timeline

PHASE 6 — PRINCIPAL COMMAND CENTER

- Dashboard
- Teacher Activity
- Classroom Observation
- Alerts
- Learning Gap
- Operational Reports

PHASE 7 — GOVERNANCE & SCALE

- Retention
- Export
- Backup/Restore
- Incident
- Corrections
- Advanced Reports
- Approved Integration

---

63. TESTING / QA

Release-এর আগে পরীক্ষা:

Functional

প্রতিটি feature কাজ করছে কি না।

Permission

এক role অন্য role-এর private data দেখতে পারছে কি না।

Data

Duplicate, invalid, missing data।

Security

OTP, session, authorization।

Mobile

Android phone-এর বিভিন্ন screen size।

Bangla

Unicode, font, line wrapping।

Offline

Internet ছাড়া attendance/lesson কাজ করছে কি না।

Sync

Offline data safely server-এ যাচ্ছে কি না।

---

64. PILOT ROLLOUT

প্রথমে পুরো স্কুলে নয়।

Pilot

একটি Class + Section নিয়ে পরীক্ষা।

Teacher test করবে:

- Attendance
- Lesson
- Homework
- Learning

Principal test করবে:

- Dashboard
- Alert
- Report

Parent test করবে:

- OTP
- Child profile
- Homework
- Result

Student test করবে:

- Routine
- Homework
- Result

তারপর feedback অনুযায়ী full rollout।

---

65. SCHOOL KPI

Access

- Student count
- Teacher count

Attendance

- Daily attendance
- Persistent absence trend

Teaching

- Lesson coverage
- Diary completion
- Homework completion

Learning

- Assessment coverage
- Learning gap
- Intervention follow-up

Academic

- Exam status
- Result publication
- Subject trend

Participation

- Special Class
- Project
- Achievement

Operations

- Teacher availability
- Substitute need
- Events
- Open issues

KPI হবে decision support, teacher punishment বা ranking system নয়।

---

66. AI-READY FUTURE

পরবর্তী version-এ AI ব্যবহার করা যেতে পারে:

- Lesson planning
- Homework drafting
- Report summarization
- Learning-gap summary
- Attendance pattern explanation
- Parent communication drafting
- Principal dashboard summary

কিন্তু AI কখনো final decision-maker হবে না:

- Promotion
- Punishment
- Discipline
- Sensitive classification
- Academic labeling

Student data AI-তে পাঠানোর সময়:

- Minimize
- Anonymize/Pseudonymize যেখানে সম্ভব
- Human Review
- Auditability
- Provider privacy review

অবশ্যই থাকবে।

---

67. BACKUP & RECOVERY

Backup:

- Scheduled
- Encrypted
- Multiple recovery points
- Monitoring

অবশ্যই periodic restore test করতে হবে।

শুধু backup নেওয়া যথেষ্ট নয়—backup থেকে সত্যিই restore করা যায় কি না সেটিও পরীক্ষা করতে হবে।

---

68. GOVERNANCE

School authority নির্ধারণ করবে:

- Data Owner
- Approver
- Editor
- Exporter
- Archiver
- Privacy Incident Handler

Data Steward:

- Data quality
- Duplicate correction
- Archive
- Reporting consistency
- Data correction

---

69. IPEMIS RELATIONSHIP

এই app জাতীয় EMIS-এর replacement নয়।

এটি হবে:

«School-level operating layer»

অর্থাৎ বিদ্যালয়ের দৈনন্দিন academic এবং operational workflow পরিচালনা করবে।

যেখানে প্রয়োজন ও অনুমোদিত integration সম্ভব, ভবিষ্যতে national system-এর সঙ্গে সমন্বয়ের architecture রাখা হবে।

---

70. FINAL PRODUCT FLOW

LOGIN
   ↓
ROLE DETECTION
   ↓
HOME DASHBOARD
   ↓
ROLE-SPECIFIC WORKFLOW
   ↓
DATABASE
   ↓
AUDIT + SECURITY
   ↓
REPORTING
   ↓
PRINCIPAL COMMAND CENTER

---

71. COMPLETE SCHOOL DATA FLOW

Student Admission
       ↓
Master Student Profile
       ↓
Permanent Student ID
       ↓
Class + Section
       ↓
Routine
       ↓
Attendance
       ↓
Lesson
       ↓
Homework + Diary
       ↓
Learning Evidence
       ↓
Assessment
       ↓
Learning Support
       ↓
Exam
       ↓
Result
       ↓
Special Class / Group / Project
       ↓
Achievement
       ↓
Portfolio
       ↓
Timeline
       ↓
Class 2
       ↓
Class 3
       ↓
Class 4
       ↓
Class 5

একই Student ID পুরো journey বহন করবে।

---

72. THE MOST IMPORTANT DESIGN RULES

RULE 01

One Student = One Master Profile

RULE 02

One Student = One Permanent Student ID

RULE 03

Regular Class, Special Class এবং Study Group আলাদা entity।

RULE 04

Parent = verified access, duplicate student profile নয়।

RULE 05

Teacher workflow হবে দ্রুত ও সহজ।

RULE 06

Principal dashboard হবে action-oriented।

RULE 07

Learning শুধু marks দিয়ে মাপা হবে না।

RULE 08

Student-এর sensitive information restricted থাকবে।

RULE 09

Critical data change audit ছাড়া হবে না।

RULE 10

Offline data silent overwrite করা যাবে না।

RULE 11

AI final decision-maker হবে না।

RULE 12

সবকিছুর কেন্দ্র হবে Student Learning Journey।

---

73. FINAL PRODUCT DEFINITION

এই অ্যাপের সবচেয়ে সংক্ষিপ্ত সংজ্ঞা:

«“একটি পূর্ণাঙ্গ School Operating System, যার কেন্দ্র হলো শিক্ষার্থীর Class 1 থেকে Class 5 পর্যন্ত সম্পূর্ণ Learning Journey এবং যার Management Center হলো Principal School Command Center।”»

CORE

STUDENT LEARNING JOURNEY

MANAGEMENT CENTER

PRINCIPAL COMMAND CENTER

OPERATING LAYERS

ADMIN + TEACHER + STUDENT + PARENT

FOUNDATION

SECURITY + PRIVACY + DATA QUALITY + AUDIT + OFFLINE-FIRST

---

74. ANDROID DEVELOPMENT TARGET

এই Blueprint থেকে Android development শুরু করার সময় implementation-এর মূল স্তর হবে:

Android App
   │
   ├── Authentication
   ├── Role-Based UI
   ├── Local Database / Offline Cache
   ├── Sync Engine
   ├── API Layer
   ├── Security Layer
   └── Notification Layer

Backend
   │
   ├── Authentication Service
   ├── School Service
   ├── Student Service
   ├── Academic Service
   ├── Attendance Service
   ├── Learning Service
   ├── Result Service
   ├── Parent Service
   ├── Notification Service
   ├── Reporting Service
   ├── Audit Service
   └── Backup / Recovery

---

MASTER PRINCIPLE

স্কুলকে অ্যাপের জন্য বদলানো হবে না।

অ্যাপকে স্কুলের বাস্তব কাজের সঙ্গে মানিয়ে তৈরি করা হবে।

Change the workflow, not the school.

এবং সবশেষে:

«One Student. One Master Profile. One Permanent Student ID. One Complete Learning Journey.»