# HerFlow-AI
Built an agentic AI companion using Kiro hooks and Anthropic Claude Sonnet to help working women manage mental load by auto-categorizing tasks (HOME / WORK / SELF_CARE), setting priorities, and detecting overwhelm in real time

🌸 HerFlow AI
Women's Mental Load & Wellness Manager
AI-DLC Month Hackathon · Health & Wellness Category · Built with Kiro
---
🎯 The Problem (ONE Daily Problem)
> *Women managing home + work carry an invisible "mental load" — the cognitive burden of constantly remembering, planning, and orchestrating everything for two lives simultaneously. This leads to burnout, anxiety, and neglected self-care.*
Ask any working woman in Madurai or Coimbatore — she will tell you:
She is the one who remembers the school deadline AND the sprint deadline
She carries the grocery list in her head while preparing for client calls
She skips her own wellness while caring for everyone else
---
💡 The Solution: HerFlow AI
An agentic AI companion that doesn't just list tasks — it understands her load and actively protects her wellness.
---
🤖 Kiro Agentic Hooks Used
Hook	What It Does
`onTaskCreate`	Auto-categorizes (HOME/WORK/SELF_CARE), sets priority, detects overwhelm score
`onOverloadDetected`	Fires wellness intervention with breathing exercise + delegate suggestion
`onDayStart`	Generates personalized morning briefing with today's focus + me-time reminder
`onVoiceInput`	Parses natural speech into multiple structured tasks
`onMoodCheck`	Adapts app tone + suggestions based on her emotional state
---
📂 Project Structure
```
herflow-ai/
├── .kiro/
│   ├── hooks/
│   │   ├── onTaskCreate.js        ← AI enrichment on every new task
│   │   ├── onOverloadDetected.js  ← Wellness intervention agent
│   │   ├── onDayStart.js          ← Morning briefing agent
│   │   ├── onVoiceInput.js        ← Voice-to-tasks parser
│   │   └── onMoodCheck.js         ← Mood-adaptive UI agent
│   ├── specs/
│   │   └── herflow.md             ← Project specification
│   └── settings/
│       └── project.json           ← Kiro configuration
├── src/
│   ├── agents/
│   │   └── herflowAgent.js        ← Claude API bridge
│   ├── hooks/
│   │   └── useHerFlow.js          ← React hook connecting UI to Kiro
│   ├── App.jsx                    ← Main UI
│   └── main.jsx
└── package.json
```
---
✨ Key Features
1. 🎙 Voice Task Capture
Tap mic, say: "Remind me to submit the report, call the school, and drink water"
→ AI creates 3 tasks, categorized, with priorities — in seconds
2. 🧠 AI Task Enrichment (onTaskCreate hook)
Every task gets:
Category: HOME / WORK / SELF_CARE
Priority: HIGH / MEDIUM / LOW
Energy estimate
Time estimate
Overwhelm score (0–10)
A gentle AI tip
3. 🌿 Overwhelm Detection (onOverloadDetected hook)
When load hits threshold, AI automatically:
Shows a breathing exercise
Suggests one quick win
Recommends one task to delegate
Shares a genuine affirmation
4. 🌅 Morning Briefing (onDayStart hook)
Every morning: personalized daily focus + energy tip + me-time reminder
5. 😊 Mood-Adaptive UI (onMoodCheck hook)
Rate your mood → AI adapts its tone, hides low-priority stress, suggests what to do now
---
🛠 Tech Stack
Frontend: React 18 + Vite
AI: Anthropic Claude Sonnet via Kiro integration
Agentic Framework: Kiro hooks (`.kiro/hooks/`)
Storage: localStorage (prototype)
Voice: Web Speech API (`en-IN` locale)
---
🚀 How to Run
```bash
# Install dependencies
npm install

# Start development server
npm run dev

# Open in browser
http://localhost:5173
```
---
👩‍💻 Built For
Women in Tier 2 Indian cities balancing professional careers and home responsibilities — the invisible managers of two worlds.
---
Built with 💜 for AI-DLC Month · UG · Kiro + Claude
