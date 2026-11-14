# LearnNova AI – Adaptive, Multi-Agent Learning Platform

An AI-powered learning platform that analyses a learner's skills, identifies gaps against a target career, builds a personalized roadmap, and adapts when the learner changes goals or performs poorly in an assessment.

## Features
- **User Profile** – skills (0–5), certifications, projects, career goal
- **Skill Analysis** – strengths/gaps, radar chart, KPI dashboard
- **Career Matching** – match % for Full Stack, Frontend, Backend, Data Scientist, DevOps
- **Learning Recommendations** – courses, tutorials and practice projects, ordered by prerequisites
- **Progress Tracking** – resource checklist, assessments, score history, weekly study schedule
- **AI Mentor** – chat guidance (next steps, time estimate, weak areas, readiness)

## Agentic Architecture
| Agent | Responsibility |
|---|---|
| Profile Agent | Maintains learner data |
| Skill Analyst | Finds strengths and gaps |
| Career Matcher | Scores fit and detects hidden prerequisites |
| Resource Curator | Builds and re-plans the roadmap |
| Progress Evaluator | Grades assessments (pass threshold 60%) |
| AI Mentor | Guides and motivates the learner |

Pipeline: `Profile → Analyst → Matcher → Curator → Evaluator → Mentor`

**Adaptive behaviour**
- Score < 60% → Curator adds remedial resources and re-queues the weak prerequisite (e.g. React → JavaScript); Mentor explains the change.
- Career goal change → roadmap rebuilt; existing skills carry over.

## Sample Scenario
Student with Python, SQL, basic HTML → target Full Stack Developer → gaps: JavaScript, React, Node.js (+ prerequisites). Click **Load sample scenario** on the dashboard.

## Run
No installation needed. Open `index.html` in any browser. Data is saved in browser localStorage.

## Tech Stack
HTML, CSS, vanilla JavaScript (rule-based agent orchestration, SVG charts).

## Future Work
LLM-backed agents (mentor, quiz generation), real course APIs, user accounts and a database, team/university dashboards.
