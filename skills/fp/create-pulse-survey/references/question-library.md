# Pulse Survey Question Library

Curated questions for each pulse theme. Questions are inspired by FeedbackPulse and leading engagement frameworks including Gallup Q12.

Each question includes:
- **Type:** `likert_5` (5-point agreement scale) or `open_ended`
- **Flag:** `core` (prioritise first) or `supplementary` (add to reach target length)

**Type mapping for output:**
- `likert_5` → MCP `type: likert` with `options.label_preset: agreement` / CSV `type: likert`, `label_preset: agreement`
- `open_ended` → MCP `type: text` / CSV `type: text`

Replace `[Company]` with the actual company name when known. If unknown, leave as `[Company]` and note it in your response.

---

## eNPS (Employee Net Promoter Score)

*Fixed structure — do not add Likert questions or mix with other themes. See Step 1b in SKILL.md for full guidance.*

| # | Question | Type | Flag |
|---|---|---|---|
| NPS1 | On a scale of 0–10, how likely are you to recommend [Company] as a great place to work? | enps | core |
| NPS2 | What is the main reason for your score? | open_ended | core |
| NPS3 | What would most improve your experience at [Company]? | open_ended | supplementary |

---

## morale

*General employee sentiment, motivation, and happiness at work.*

| # | Question | Type | Flag |
|---|---|---|---|
| M1 | I feel motivated to do my best work right now. | likert_5 | core |
| M2 | Overall, I am happy working at [Company] at the moment. | likert_5 | core |
| M3 | I feel positive about where [Company] is headed. | likert_5 | core |
| M4 | I can maintain a healthy pace of work right now. | likert_5 | core |
| M5 | I feel proud to work at [Company]. | likert_5 | supplementary |
| M6 | What is one thing that would most improve your experience at work right now? | open_ended | supplementary |

---

## manager-trust

*Relationship quality, feedback, support, and communication from the direct manager.*

| # | Question | Type | Flag |
|---|---|---|---|
| MT1 | My manager genuinely cares about my wellbeing. | likert_5 | core |
| MT2 | I receive useful feedback from my manager on a regular basis. | likert_5 | core |
| MT3 | I feel comfortable raising concerns or questions with my manager. | likert_5 | core |
| MT4 | My manager keeps me informed about decisions that affect my work. | likert_5 | core |
| MT5 | My manager recognises me when I do good work. | likert_5 | supplementary |
| MT6 | What could your manager do differently to better support you? | open_ended | supplementary |

---

## workload

*Capacity, sustainable pace, priority clarity, and resource availability.*

| # | Question | Type | Flag |
|---|---|---|---|
| W1 | My workload feels manageable right now. | likert_5 | core |
| W2 | I have enough time to complete my core responsibilities. | likert_5 | core |
| W3 | I have clarity on my priorities this week. | likert_5 | core |
| W4 | I feel comfortable switching off from work outside of working hours. | likert_5 | supplementary |
| W5 | I have the resources and support I need to do my job well. | likert_5 | supplementary |
| W6 | What would help you manage your workload or priorities better? | open_ended | supplementary |

---

## change-management

*Reactions to a reorg, layoff, leadership change, strategic pivot, merger, or major announcement. Send 2–4 weeks after the event.*

| # | Question | Type | Flag |
|---|---|---|---|
| C1 | I understand why the recent changes were made. | likert_5 | core |
| C2 | Leadership has communicated clearly about recent changes. | likert_5 | core |
| C3 | I feel supported by my manager through this period of change. | likert_5 | core |
| C4 | I feel confident in the direction [Company] is taking. | likert_5 | core |
| C5 | Leadership is taking visible actions to support employees through this change. | likert_5 | supplementary |
| C6 | What questions do you have about recent changes that have not been answered yet? | open_ended | supplementary |

---

## dei

*Belonging, inclusion, fair treatment, and feeling respected across all backgrounds.*

| # | Question | Type | Flag |
|---|---|---|---|
| D1 | I feel I can be myself at work. | likert_5 | core |
| D2 | People from all backgrounds are treated fairly at [Company]. | likert_5 | core |
| D3 | My voice is heard and taken seriously in team discussions. | likert_5 | core |
| D4 | I feel included and respected by the people I work with. | likert_5 | supplementary |
| D5 | I see [Company] taking meaningful action on diversity and inclusion. | likert_5 | supplementary |
| D6 | What would make [Company] a more inclusive place to work? | open_ended | supplementary |

---

## remote-hybrid

*Ongoing experience, connection, and productivity in remote or hybrid working arrangements.*

| # | Question | Type | Flag |
|---|---|---|---|
| RH1 | I have the tools and technology I need to work effectively from home or remotely. | likert_5 | core |
| RH2 | I feel connected to my teammates despite our remote or hybrid arrangement. | likert_5 | core |
| RH3 | I am able to disconnect from work outside of my working hours. | likert_5 | core |
| RH4 | Our team has effective ways to collaborate and communicate when working remotely. | likert_5 | supplementary |
| RH5 | I feel included in team discussions and decisions regardless of where I work from. | likert_5 | supplementary |
| RH6 | What would improve your remote or hybrid working experience? | open_ended | supplementary |

---

## onboarding

*New hire experience — suited to the first 30, 60, or 90 days.*

| # | Question | Type | Flag |
|---|---|---|---|
| O1 | I have the information and resources I need to do my job. | likert_5 | core |
| O2 | My onboarding experience has set me up to do my job effectively. | likert_5 | core |
| O3 | I understand how my role contributes to [Company]'s goals. | likert_5 | core |
| O4 | I know where to go and who to ask when I have questions. | likert_5 | supplementary |
| O5 | I feel like I am becoming part of the team. | likert_5 | supplementary |
| O6 | What has been missing or could be improved in your onboarding experience? | open_ended | supplementary |

---

## team-cohesion

*Within-team collaboration, mutual trust, and sense of camaraderie.*

| # | Question | Type | Flag |
|---|---|---|---|
| TC1 | My team works well together. | likert_5 | core |
| TC2 | I trust my teammates to follow through on their commitments. | likert_5 | core |
| TC3 | We have effective ways to resolve disagreements on my team. | likert_5 | core |
| TC4 | I feel a genuine sense of camaraderie with my teammates. | likert_5 | supplementary |
| TC5 | My team has a shared understanding of our goals and priorities. | likert_5 | supplementary |
| TC6 | What would strengthen collaboration or trust on your team? | open_ended | supplementary |

---

## leadership-communication

*Confidence in senior leadership direction, strategy clarity, and organisational trust. Distinct from manager-trust, which covers the direct manager relationship.*

| # | Question | Type | Flag |
|---|---|---|---|
| LC1 | I have confidence in the decisions made by senior leadership. | likert_5 | core |
| LC2 | Senior leadership communicates a clear direction for [Company]. | likert_5 | core |
| LC3 | I understand where [Company] is heading over the next 12 months. | likert_5 | core |
| LC4 | I trust that senior leadership acts with integrity. | likert_5 | supplementary |
| LC5 | Senior leadership is visible and accessible to employees. | likert_5 | supplementary |
| LC6 | What would you like to see more of from senior leadership? | open_ended | supplementary |

---

## psychological-safety

*Feeling safe to speak up, take risks, and learn from mistakes without fear of negative consequences.*

| # | Question | Type | Flag |
|---|---|---|---|
| PS1 | I feel safe to speak up when I disagree with a decision or approach. | likert_5 | core |
| PS2 | I can try new approaches without fear of negative consequences if they don't work out. | likert_5 | core |
| PS3 | When things go wrong, we focus on learning rather than assigning blame. | likert_5 | core |
| PS4 | I feel comfortable asking for help when I need it. | likert_5 | supplementary |
| PS5 | My ideas and contributions are genuinely welcomed by my team. | likert_5 | supplementary |
| PS6 | What would make you feel safer to speak up or experiment at work? | open_ended | supplementary |

---

## l-and-d

*Career growth opportunities, learning resources, and development support.*

| # | Question | Type | Flag |
|---|---|---|---|
| LD1 | I have opportunities to learn and grow in my role. | likert_5 | core |
| LD2 | My manager actively supports my professional development. | likert_5 | core |
| LD3 | I have access to the learning resources and training I need. | likert_5 | core |
| LD4 | I can see a clear path for my career development at [Company]. | likert_5 | supplementary |
| LD5 | The work I do challenges me in a positive way. | likert_5 | supplementary |
| LD6 | What learning or development opportunities would be most valuable to you? | open_ended | supplementary |

---

## all-hands

*Post-event feedback for an all-hands meeting, town hall, or company offsite. Send within 48 hours of the event; keep open for 3–5 business days. Use 3–5 questions only.*

| # | Question | Type | Flag |
|---|---|---|---|
| AH1 | The all-hands communicated a clear message. | likert_5 | core |
| AH2 | I feel more informed about [Company]'s direction after this event. | likert_5 | core |
| AH3 | My questions or concerns were adequately addressed. | likert_5 | core |
| AH4 | I found the Q&A session useful and authentic. | likert_5 | supplementary |
| AH5 | I feel more connected to [Company]'s leadership after this event. | likert_5 | supplementary |
| AH6 | What topic would you most like leadership to address in the next all-hands? | open_ended | supplementary |
