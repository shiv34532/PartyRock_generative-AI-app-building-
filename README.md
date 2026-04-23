PartyRock_generative-AI-app-building-
Practical AI project demonstrating prompt engineering, responsible AI, and AWS generative AI concepts.
Generative AI project built with AWS PartyRock during the AWS AI Practitioner Challenge by Udacity.
StudyFlow is a next-generation academic coaching tool that leverages the power of generative AI 
to eliminate the guesswork from studying. Whether you're cramming for a final exam, managing 
multiple assignments, or building a semester-long learning plan, StudyFlow acts as your personal 
academic coach — available 24/7, infinitely patient, and always personalized to *you*.

Built entirely on **Amazon PartyRock** with **Amazon Bedrock** foundation models at its core, 
StudyFlow demonstrates how no-code AI application development can produce genuinely useful, 
production-quality educational tools without writing a single line of code.

> 💡 **What makes StudyFlow different?** Unlike generic study timers or static planners, 
> StudyFlow understands *your* subject matter, *your* goals, and *your* available time — 
> then crafts a study experience that adapts to you.

---

## ✨ Features

### 🎯 Core Study Planning Features

| Feature | Description |
|---|---|
| 🍅 **Pomodoro Study Sessions** | AI-generated session plans using the proven Pomodoro technique with custom intervals |
| 📖 **Subject-Specific Strategies** | Tailored learning approaches for STEM, humanities, languages, and more |
| 💪 **Motivational Coaching** | Personalized encouragement, focus techniques, and mental wellness tips |
| 🤖 **Interactive AI Study Coach** | Real-time chat with an AI tutor for questions, clarifications, and guidance |
| 📄 **Document Upload Integration** | Upload syllabi, notes, or assignments for hyper-personalized recommendations |
| 🗺️ **Long-Term Study Roadmap** | Multi-week and semester-length planning with milestone tracking |
| 🔥 **Daily Streak Tracker** | Gamified progress logging with streak motivation and consistency rewards |
| 🎭 **Avatar Personalization** | Choose your study companion avatar for a more engaging experience |

### 🧠 AI-Powered Intelligence Features

- **Adaptive Difficulty Scaling** — Recommendations adjust based on your self-reported confidence levels
- **Context-Aware Suggestions** — The AI remembers your subject, goals, and constraints throughout the session
- **Multi-Subject Balancing** — Intelligently distributes study time across multiple subjects
- **Exam Countdown Integration** — Urgency-aware planning that intensifies as deadlines approach
- **Learning Style Recognition** — Identifies whether you're a visual, auditory, or kinesthetic learner
- **Break Optimization** — Scientifically-informed break recommendations to prevent burnout

### 🎨 User Experience Features

- **Zero Setup Required** — Start studying in under 60 seconds
- **No Account Needed** — Fully accessible without registration
- **Mobile-Friendly Interface** — Responsive design works on any device
- **Instant Results** — AI responses generated in real-time
- **Shareable Plans** — Export or share your study plans with classmates

---

## 🏗️ App Structure & Widget Architecture

StudyFlow is built using a carefully orchestrated system of PartyRock widgets that work together 
to create a seamless, intelligent study planning experience. The architecture follows a 
**Input → Process → Output** pipeline with an interactive chat layer.

prpgect structure: beta v1.0





### 📥 Input Widgets

#### 1. Subject Input Widget

Type: Text Input
Label: "What subject are you studying?"
Placeholder: "e.g., Calculus II, World History, Python Programming"
Required: true
Character Limit: 200
Purpose: Primary context for all AI-generated content



2. Goals & Objectives Widget
Type: Text Area
Label: "What do you want to achieve in this session?"
Placeholder: "e.g., Master integration by parts, finish Chapter 5 review"
Required: true
Character Limit: 500
Purpose: Defines success criteria for the study plan


3. Study Duration Widget
Type: Dropdown / Slider
Label: "How much time do you have?"
Options: [25 min, 50 min, 90 min, 2 hours, 3+ hours, Custom]
Required: true
Purpose: Calibrates Pomodoro intervals and content depth



4. Study Type Selector Widget
Type: Multi-Select Dropdown
Label: "What type of studying are you doing?"
Options:
  - 📖 Reading & Note-Taking
  - 🔄 Review & Memorization
  - ✏️ Problem Solving & Practice
  - 📝 Essay Writing & Research
  - 🎯 Exam Preparation
  - 🆕 Learning New Material
Required: true
Purpose: Determines strategy type and technique recommendations



5. Avatar Selection Widget
Type: Image Selector / Radio Button
Label: "Choose your study companion"
Options: [Scholar Owl, Focus Fox, Zen Panda, Rocket Rabbit, Ninja Cat]
Required: false
Default: Scholar Owl
Purpose: Personalizes motivational messages and coaching tone




6. Materials Upload Widget
Type: Document Upload
Label: "Upload your study materials (optional)"
Accepted Formats: [PDF, TXT, DOCX, PNG, JPG]
Max Size: 10MB
Required: false
Purpose: Enables document-aware personalized recommendations
📤 AI Output Widgets



7. Personalized Study Plan Widget
Type: AI Text Generation
Model: Claude Sonnet (Amazon Bedrock)
Input Dependencies: [Subject, Goals, Duration, Study Type, Materials]
Output Format: Structured Pomodoro schedule with time blocks
Refresh: On input change
Purpose: Core study session plan with minute-by-minute guidance



8. Motivation & Focus Tips Widget
Type: AI Text Generation
Model: Claude Sonnet (Amazon Bedrock)
Input Dependencies: [Subject, Goals, Avatar, Study Type]
Output Format: Bulleted motivational coaching with techniques
Refresh: On input change
Purpose: Psychological support and focus enhancement strategies


9. Long-Term Roadmap Widget
Type: AI Text Generation
Model: Claude Sonnet (Amazon Bedrock)
Input Dependencies: [Subject, Goals, Duration]
Output Format: Weekly milestone plan with checkpoints
Refresh: On demand
Purpose: Extended planning beyond single study sessions




10. Streak & Progress Tracker Widget
Type: AI Text Generation + Static Display
Model: Claude Sonnet (Amazon Bedrock)
Input Dependencies: [Goals, Study Type, Duration]
Output Format: Daily log template + streak motivation message
Refresh: Daily
Purpose: Gamified consistency tracking and habit formation
💬 Interactive Chat Widget



11. AI Study Coach Chat
Type: Chatbot Widget
Model: Claude Sonnet (Amazon Bedrock)
Context Injection: Subject + Goals + Study Type from input widgets
Persona: Encouraging, knowledgeable academic tutor
Capabilities:
  - Answer subject-specific questions
  - Explain difficult concepts
  - Quiz the student on material
  - Provide additional resources
  - Adjust study plan in real-time
Purpose: On-demand tutoring and adaptive coaching
📊 Tracking Widget



12. Progress Log Widget
Type: User Input + AI Response
Label: "Log today's progress"
Input: Free-text progress notes
AI Response: Encouragement + next session recommendations
Purpose: Reflection, accountability, and continuity between sessions


### 🔢 Problem Set Practice
> *"I have 30 physics problems to complete on thermodynamics."*

StudyFlow delivers:
- Problem-batching strategy (group by difficulty/type)
- Time allocation per problem type
- When to skip and return vs. persevere
- Formula review checkpoints
- AI coach availability for stuck moments

---

### 🗓️ Long-Term Course Preparation
> *"I'm starting Organic Chemistry next semester and want to prepare over 8 weeks."*

StudyFlow builds:
- 8-week progressive learning roadmap
- Prerequisite concept identification
- Weekly milestone checkpoints
- Resource recommendations by week
- Habit formation and consistency strategies



## 📖 How to Use

### 🚀 Quick Start (Under 60 Seconds)


1. Open the StudyFlow app via the live link
2. Enter your subject in the first field
3. Describe your study goals
4. Select your available time
5. Choose your study type
6. Click Generate → Your personalized plan appears instantly!





📋 Step-by-Step User Guide
Step 1: Enter Your Subject 📚
✅ Good: "AP Chemistry - Stoichiometry and Mole Calculations"
✅ Good: "JavaScript - Async/Await and Promises"  
✅ Good: "Spanish B2 - Subjunctive Mood"
❌ Too vague: "Science"
❌ Too vague: "Math stuff"
Pro Tip: The more specific your subject, the more targeted your study plan will be.

Step 2: Define Your Goals 🎯
✅ Good: "Understand how to balance chemical equations and solve 
         stoichiometry problems from scratch"
✅ Good: "Complete practice problems 1-20 from Chapter 7 and 
         review my notes from Tuesday's lecture"
❌ Too vague: "Study for test"
❌ Too vague: "Learn stuff"
Pro Tip: Include both what you want to learn and why it matters (upcoming test,
assignment due, etc.)

Step 3: Set Your Duration ⏱️
25 minutes  → Single focused Pomodoro sprint
50 minutes  → Classic Pomodoro with one break
90 minutes  → Deep work session with strategic breaks
2 hours     → Extended session with multiple topics
3+ hours    → Full study day with energy management
Pro Tip: Be honest about your available time. A realistic 50-minute plan beats
an ambitious 3-hour plan you won't complete.

Step 4: Select Study Type 📝
Reading & Note-Taking    → New material, textbook chapters
Review & Memorization    → Flashcards, spaced repetition, quizzing
Problem Solving          → Math, science, coding exercises
Essay Writing            → Research papers, written assignments
Exam Preparation         → Mixed review, practice tests
Learning New Material    → Concepts you've never seen before



Step 5: Choose Your Avatar 🎭 (Optional)
🦉 Scholar Owl    → Wise, methodical, detail-oriented coaching
🦊 Focus Fox      → Sharp, efficient, time-management focused
🐼 Zen Panda      → Calm, mindful, stress-reduction emphasis
🐰 Rocket Rabbit  → Energetic, fast-paced, high-motivation
🐱 Ninja Cat      → Stealthy, strategic, precision-focused


Step 6: Upload Materials 📄 (Optional but Recommended)
What to upload:
  ✅ Course syllabus (PDF)
  ✅ Lecture notes (PDF, DOCX)
  ✅ Assignment instructions (PDF)
  ✅ Textbook chapter photos (JPG, PNG)
  ✅ Practice exam (PDF)

What NOT to upload:
  ❌ Personal information
  ❌ Files over 10MB
  ❌ Unrelated documents


Step 7: Interact with Your AI Coach 💬
Great questions to ask your Study Coach:
  → "Can you explain [concept] in simpler terms?"
  → "Quiz me on what I should know for this topic"
  → "I'm stuck on [specific problem], can you help?"
  → "What are the most important things to focus on?"
  → "I only have 20 minutes left, what should I prioritize?"
  → "Can you give me a practice problem?"

Step 8: Log Your Progress 📊
After each session, log:
  ✅ What you completed
  ✅ What was challenging
  ✅ Your confidence level (1-10)
  ✅ What to review next time


## Screenshots

### Home Screen
![Home Screen]<img width="1836" height="922" alt="Home Screen" src="https://github.com/user-attachments/assets/7bbb6d8f-acd1-41a8-831a-b526a7f4f227" />


### Sample Input
![Sample Input]<img width="1392" height="757" alt="Sample Input" src="https://github.com/user-attachments/assets/c239690c-aaaf-4c61-9e8b-48341ba7f99c" />


### Generated Output
![Generated Output]<img width="1607" height="722" alt="Generated Output" src="https://github.com/user-attachments/assets/e45bb5f5-3833-46dd-843b-051c1427500b" />


### Project Overview
![Project Overview]<img width="1877" height="902" alt="Project Overview" src="https://github.com/user-attachments/assets/11b227ce-eec9-4805-b9dd-00533a03ba7b" />





