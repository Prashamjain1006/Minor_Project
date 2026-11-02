# KAIROS — AI-Powered Early Cognitive Screening & Personalized Memory Assistance Platform

> **College Minor Project Frontend Prototype**  
> **Developed by:** Team Kairos  
> **Department:** Computer Science & Engineering  
> **Institution:** Acropolis Institute of Technology & Research (AITR), Indore (M.P.), India  
> **Reference Paper:** *"AI-Powered Early Cognitive Screening and Personalized Memory Assistance Platform for Alzheimer's Patients: A Review and Proposed Framework"*

---

## 🏥 Executive Project Summary

**KAIROS** is a specialized digital healthcare support platform designed to bridge the gap between older adults experiencing cognitive changes, their family caregivers, and consulting clinicians. 

The platform brings together:
1. **Multimodal Early Cognitive Screening (10-minute wizard):** Evaluates 5 core cognitive domains (Orientation, Word Memory & Delayed Recall, Attention & Working Memory, Category Verbal Fluency, and Visuospatial Clock Construction) along with a Caregiver Functional Observation Survey.
2. **Transparent Illustrative Scoring & Traffic-Light Concern Bands:** Assigns Green (Stable), Amber (Attention Warranted), or Red (Clinical Consultation Recommended) with clear explanations of why specific patterns were flagged.
3. **Self-Referential Baseline & Rolling Median Tracking:** Compares current scores against the individual's personal history rather than arbitrary population norms, using a rolling median to protect against transient bad days caused by fatigue or sleep loss.
4. **Personalized Spoken Family Voice Reminders:** Enables sons, daughters, and grandchildren to record loving medication and hydration cues in their own voice, proven to reduce startle agitation and increase compliance.
5. **Printable Clinician Summary:** Generates an A4 summary with longitudinal graphs, domain breakdowns, and ruled clinician note sections via standard browser print-to-PDF.
6. **Senior-Friendly Accessibility:** Built-in Hindi (`हिंदी`) and English localization, Large Text font scaling (125% scale with 52px touch targets), High Contrast dark-mode styling, and browser text-to-speech audio prompts.

---

## 🛠️ Technology Stack

- **Core Framework:** React 19 + Vite 8
- **Icons & Visuals:** Lucide React (`lucide-react`)
- **Animations & Delight:** Canvas Confetti (`canvas-confetti`)
- **Design System:** Custom Vanilla CSS Design System with CSS Tokens (`src/index.css`), zero external build-tool bottlenecks, full High Contrast and Large Text modes, and `@media print` A4 formatting
- **Data Persistence:** Browser `localStorage` (offline-first, zero cloud data leaks)
- **Audio & Speech:** Browser `MediaRecorder` API with simulated fallback + Web Speech Synthesis (`window.speechSynthesis`)
- **Clinician Export:** Browser Native `window.print()`

---

## 🚀 Quick Start / How to Run Locally

### Prerequisites
- Node.js (v18, v20, or v22)
- npm or npx

### Installation & Launch Commands
```bash
# 1. Clone or navigate to the project root directory
cd "c:\Users\Hp\Desktop\MINOR PROJECT"

# 2. Install dependencies (if not already installed)
npm install

# 3. Start the Vite local development server
npm run dev

# 4. Open the application in your browser
# URL: http://127.0.0.1:5173
```

---

## 📋 Faculty Evaluation Demonstration Sequence (15-Step Guide)

For a live evaluation demo in front of college faculty and reviewers, follow this smooth sequence:

1. **Step 1: Welcome & Landing Page (`/landing`)**
   - Present the project title, Team Kairos branding, and Acropolis Institute credits.
   - Explain the 3 core pillars: Early Cognitive Screening, Personalized Reminders, and Caregiver Support.
   - Highlight the responsible healthcare disclosure: *Educational prototype supporting families; not a replacement for clinical diagnosis*.

2. **Step 2: Consent & Privacy Agreement (`/consent`)**
   - Click **"Get Started"**.
   - Review the explanation of the 5 cognitive domains tested.
   - Note the local storage privacy disclosure (no cloud uploads).
   - Check the mandatory consent box and click **"Proceed to Screening"**.

3. **Step 3: Care Recipient Profile (`/profile`)**
   - Review the fictional demonstration profile: **Meera Sharma (72y, Female)**.
   - Primary Caregiver: **Anita Sharma (Daughter)**.
   - Review emergency contact, preferred language, and physician details.

4. **Step 4: Caregiver Dashboard (`/dashboard`)**
   - Review personalized greeting: *"Good morning, Anita"*.
   - Inspect the **5 required summary metric cards**:
     1. Today's Reminders (e.g. 4 pending of 5)
     2. Screening Sessions Completed (4 sessions logged)
     3. Latest Concern Band (Amber • Attention Warranted, 71/100)
     4. Cognitive Activities Completed (38 plays across 5 mini-games, 4-day streak)
     5. Last Screening Date (24 Oct 2026)
   - Point out the **Gentle Sustained Change Alert** explaining Meera's mild downward variation from her baseline of 77.
   - Observe the live offline indicator badge (*"Device Mode"*).

5. **Step 5: Cognitive Screening Wizard (`/screening`)**
   - Click **"Start Screening Session"**.
   - Walk through the **7 interactive steps**:
     - **Task 1 (Orientation):** Select Year (2026), Month (October), and Place (At home with family).
     - **Task 2 (Word Learning):** Memorize the 3 words (*Mango, River, Chair* / *आम, नदी, कुर्सी*) with optional audio readout.
     - **Task 3 (Attention):** View sequence `[3, 8, 2, 9]` and tap keypad in reverse order `[9, 2, 8, 3]`.
     - **Task 4 (Verbal Fluency):** Name animals/birds with quick accessible suggestion chips (Cow, Dog, Elephant, etc.) within the 45-second timer.
     - **Task 5 (Clock Construction):** Adjust interactive clock hands to show 10 past 11 (11:10).
     - **Task 6 (Delayed Recall):** Identify the 3 memorized words from Task 2 (Mango, River, Chair).
     - **Task 7 (Caregiver Survey):** Answer 5 functional everyday routine questions (*"No change"*, *"Sometimes"*, *"Often"*).
   - Click **"Finish & View Results"** (celebratory confetti triggers).

6. **Step 6: Screening Results & Transparent Explanations (`/screeningResults`)**
   - View overall score (e.g. 71/100) and traffic-light Concern Band (**Amber**).
   - Review the transparent explanation: *Delayed recall and verbal fluency variance noted*.
   - Examine the **Domain Breakdown Chart** (Orientation: 10/10, Recall: 7/10, Attention: 8/10, Fluency: 7/10, Clock: 8/10, Caregiver: 8/10).
   - View the baseline comparison against personal rolling median.

7. **Step 7: Playable Cognitive Mini-Activities (`/activities`)**
   - Click **"Cognitive Activities"** in the sidebar.
   - Explore the 5 interactive games:
     - **Activity 1: Names and Faces** (Match family avatar with relationship clue).
     - **Activity 2: Picture Tile Matching** (4 pairs memory card flip game).
     - **Activity 3: Daily Routine Ordering** (Arrange morning routine cards 1-4).
     - **Activity 4: Visual Patterns** (Identify alternating shapes & numbers).
     - **Activity 5: Attention Game** (Spot all 5 Gold Stars among geometric distractors).

8. **Step 8: Personalized Reminders Management (`/reminders`)**
   - Click **"Personal Reminders"**.
   - Filter by categories: *Medicine, Water, Appointment, Daily Routine*.
   - Click the checkmark to mark a reminder completed.
   - Click **"Listen"** to trigger speech synthesis reading the medication instructions aloud.
   - Click **"Add Reminder"** to demonstrate creating a new schedule item.

9. **Step 9: Family Voice Reminders Interface (`/familyVoice`)**
   - Click **"Family Voice"** in the sidebar.
   - Play existing recorded messages from daughter Anita and grandson Rohan.
   - Demonstrate the **Voice Recording Console** (supports browser microphone with graceful simulated demonstration fallback).
   - Show the **"Synthetic Voice"** alternative button.

10. **Step 10: Progress & Personal Baseline (`/progress`)**
    - View the **Longitudinal Trajectory Chart** comparing 4 sessions (scores: 80, 76, 78, 71) against the green/amber zones.
    - Highlight the **Rolling Median Reference Line (77 pts)**.
    - Explain why the rolling median is scientifically superior to an average in elderly care (outlier-resistant against transient fatigue or sleep loss).

11. **Step 11: Printable Clinician Report (`/clinicianReport`)**
    - Click **"Clinician Report"**.
    - Review formal A4 layout with patient demographics, session summary, domain breakdown, and ruled clinician note lines.
    - Click **"Print / Save as PDF"** to trigger `window.print()` (clean print preview without sidebars or headers).

12. **Step 12: Bilingual Language Switching (Hindi / English)**
    - Click the **"हिंदी"** toggle in the top header.
    - Observe that the entire interface (navigation, headings, instructions, buttons, concern bands) instantly adapts to authentic Hindi.
    - Toggle back to **"English"**.

13. **Step 13: Large Text Mode (Senior Accessibility)**
    - Click the **"A+"** button in the header.
    - Observe the root typography scaling to 125% and touch targets expanding to 52px for elderly comfort.

14. **Step 14: High Contrast Mode**
    - Click the **Eye icon** in the header.
    - Observe the deep dark slate background, high-contrast borders, and gold indicators.

15. **Step 15: Demonstration Data Reset**
    - Click the red **"Reset"** button in the header or in Settings.
    - Confirm reset to restore the sample dataset back to its default demonstration baseline.

---

## 🔒 Responsible Healthcare Communication Disclosures

This platform is an academic prototype developed for college minor project evaluation.
- It does **NOT** diagnose Alzheimer's disease, mild cognitive impairment (MCI), or any medical condition.
- It does **NOT** compute artificial clinical accuracy percentages, disease probabilities, or life expectancy.
- It does **NOT** claim that cognitive mini-games cure or prevent dementia.
- It does **NOT** store data on unsecured remote clouds; all responses remain in local browser memory.
- Results and concern bands are illustrative indicators intended to guide discussions with certified healthcare specialists.

---

## 👥 Team Kairos Credits

- **Institution:** Acropolis Institute of Technology and Research (AITR), Indore (M.P.), India
- **Department:** Computer Science & Engineering
- **Project:** Minor Project Prototype Demonstration (2026)
