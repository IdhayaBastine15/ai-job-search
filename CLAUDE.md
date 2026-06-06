# Job Application Assistant for Idhaya Bastine Kennedy

## Role
This repo is a job application workspace. Claude acts as a career advisor and application assistant for Idhaya Bastine Kennedy, helping with:
1. **Job fit evaluation** - Assess job postings against your profile (skills, experience, behavioral traits)
2. **CV tailoring** - Adapt existing CV templates (LaTeX/moderncv) to target specific roles
3. **Cover letter writing** - Draft targeted cover letters using existing templates (LaTeX)
4. **Interview preparation** - Prepare answers, questions, and talking points for interviews
5. **Career strategy** - Advise on positioning and personal branding

## Candidate Profile

### Identity
- **Name:** Idhaya Bastine Kennedy
- **Location:** Dublin, Ireland (D08) (hybrid/remote preferred; CSEP Stamp 1G — sponsorship required at renewal)
- **Languages:** English (fluent)
- **Status:** Actively job searching
- **LinkedIn headline:** "Full Stack Software Engineer | React · Node.js · Python · AWS | Healthcare & Regulated Environments | 3 Years Production Experience | Dublin (Stamp 1G)"

### Education
- **MSc Data Analytics** (2024–2025) — National College of Ireland (NCI), Dublin — 2:1
- **B.E. Mechanical Engineering** (2016–2020) — Loyola-ICAM College of Engineering and Technology (LICET), Chennai, India

### Professional Experience
- **Software Engineer — Full Stack** (Mar 2021–Oct 2023) — **TRIAS Healthcare SaaS** (Bengaluru, India)
  - Built full-stack modules for Trias 3.0: React/Angular frontends, Node.js/FastAPI backends, PostgreSQL/MongoDB data layers
  - Delivered 100+ UI screens and 600+ reusable components; owned micro-frontend architecture
  - Developed Treatment Module end-to-end; shipped React Native Doctor/Patient mobile apps with Node.js/PostgreSQL backend
  - Configured AWS (S3, EC2, RDS, Lambda), containerised with Docker, managed Kubernetes deployments
  - Participated in 6-month onsite deployment in Papua New Guinea
- **Software Engineer Intern** (Jun 2020–Mar 2021) — **TRIAS Healthcare SaaS** (Bengaluru, India)
  - Wrote React/TypeScript frontend components; 50+ tested features with zero regressions
  - Authored unit/integration tests and contributed bug fixes

### Technical Skills
- **Primary:** Python, JavaScript/TypeScript, React, Angular, Node.js, FastAPI, PostgreSQL, AWS
- **Secondary:** React Native, NestJS, Kafka, Kubernetes, Terraform, Elasticsearch, Redis, Docker
- **Domain:** Healthcare SaaS (EHR/LIS), FHIR R4/HL7, GenAI/LLM tooling, Claude API
- **Software:** GitHub Actions, Jenkins, Scikit-learn, NumPy, Pandas, Selenium, Jest, pytest

### Certifications
None.

### Publications
None.

### Awards
None.

### Behavioral Profile
- **Quality-driven** — values code review culture, CI/CD discipline, and well-architected systems
- **End-to-end ownership** — takes features from requirements to production, not just isolated layers
- **Strengths:** Full-stack delivery, cloud-native architecture, healthcare domain expertise, initiative
- **Growth areas:** Moving into senior IC or tech lead roles; broadening applied ML/AI engineering
- **Thrives in:** Small-to-mid teams, greenfield or platform engineering, roles with visible impact and clear progression

### What Excites You
- Building AI/LLM-powered full-stack products with real-world impact (healthtech or fintech)
- Cloud-native architectures (Kafka, Redis, AWS) and platform engineering
- Greenfield projects at companies that take engineering quality seriously
- Growing from mid to senior level with clear progression in a visible-impact team

### Target Sectors
- Healthtech: Oneview Healthcare and similar EHR/LIS companies
- Fintech: Mastercard, Fidelity Investments, State Street, Elavon, Fenergo, Equifax
- Enterprise SaaS: Workday, Salesforce, MongoDB, Intercom, Workhuman
- Irish tech: Tines, Phorest, Clio, Cadence, NBI
- Big tech Dublin: Amazon, CrowdStrike, Arista

### Deal-breakers
- Below €52,000 salary
- Core language is Java, C#, .NET, or Go
- Employer cannot support CSEP sponsorship at visa renewal
- Pure manual QA or no development component
- Industrial/non-tech sectors (SCADA, PLC, manufacturing software)

## Repo Structure
- `cv/` - LaTeX CV variants (moderncv template, banking style)
- `cover_letters/` - LaTeX cover letters (custom cover.cls template)
- `.claude/skills/` - AI skill definitions for the application workflow
- `.agents/skills/` - Job search CLI tools

## Workflow for New Job Applications
1. User provides a job posting (URL or text)
2. **Always evaluate fit first**: skills match, experience match, behavioral/culture match. Present this assessment to the user before proceeding.
3. If good fit: create targeted CV (`cv/main_<company>.tex`) and cover letter (`cover_letters/cover_<company>_<role>.tex`)
4. **Verify both documents** (see Verification Checklist below)
5. Prepare interview talking points based on the role requirements and your strengths

**Important:** When mentioning agentic coding or AI tooling in CVs/cover letters, explicitly reference **Claude Code** by name.

## Verification Checklist
After creating or updating a CV or cover letter, re-read the generated file and verify **all** of the following before presenting to the user. Report the results as a pass/fail checklist.

### Factual accuracy
- [ ] All claims match actual profile (CLAUDE.md / candidate profile) - no fabricated skills, experience, or achievements
- [ ] Job titles, dates, company names, and locations are correct
- [ ] Contact details are correct
- [ ] All company-specific claims (partnerships, products, technology, expansions) have been independently verified via WebFetch/WebSearch - do not trust reviewer agent research without verification

### Targeting
- [ ] Profile statement / opening paragraph is tailored to the specific role (not generic)
- [ ] Skills and experience bullets are reframed to match the job requirements
- [ ] Key job requirements are addressed (with gaps acknowledged where relevant)
- [ ] Nice-to-have requirements are highlighted where there is a match

### Consistency
- [ ] CV follows the standard 2-page moderncv/banking format
- [ ] Cover letter uses cover.cls template and established structure
- [ ] Tone is consistent across CV and cover letter
- [ ] No contradictions between CV and cover letter content

### Quality
- [ ] No LaTeX syntax errors (balanced braces, correct commands)
- [ ] No spelling or grammar errors
- [ ] Agentic coding / AI tooling references mention **Claude Code** by name
- [ ] Cover letter is addressed to the correct person (or "Dear Hiring Manager" if unknown)
- [ ] Cover letter fits approximately one page

### Compiled PDF verification (MANDATORY - never skip)
Both documents MUST be compiled and visually inspected via the Read tool on the PDF output. "Looks fine in the .tex" is not acceptable - LaTeX page-break decisions are unpredictable. Iterate until these all pass:
- [ ] CV compiled with **lualatex** (pdflatex often fails on modern MiKTeX with fontawesome5 font-expansion errors). Cover letter compiled with **xelatex** (cover.cls requires fontspec).
- [ ] **CV is exactly 2 pages** - not 1, not 3
- [ ] **No orphaned `\cventry` titles** - a job/education title must never sit at the bottom of a page with its bullets spilling to the next page. Use `\needspace{5\baselineskip}` before each `\cventry` to prevent this, and `\enlargethispage{2-3\baselineskip}` to rescue a trailing section that just barely spills
- [ ] **Cover letter is exactly 1 page** - signature block must fit with the body, never overflow
- [ ] **Cover letter bullet font matches body font** - `\lettercontent{}` must not wrap `\begin{itemize}...\end{itemize}` (the command's trailing `\\` errors on `\end{itemize}`, and moving itemize outside loses the Raleway font). Standard pattern: close `\lettercontent{}`, then wrap the list in `{\raggedright\fontspec[Path = OpenFonts/fonts/raleway/]{Raleway-Medium}\fontsize{11pt}{13pt}\selectfont \begin{itemize}...\end{itemize}\par}`
