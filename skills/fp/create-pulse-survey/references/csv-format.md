# CSV Output Format

Use this schema when producing the CSV fallback (Option B in SKILL.md). Imports directly into FeedbackPulse via **Surveys → Templates → Import Questions**.

A blank template can be downloaded from FeedbackPulse at: `GET /survey-templates/import-questions/template`

## Encoding

- **Encoding:** UTF-8 (add UTF-8 BOM if user needs Excel/Google Sheets compatibility)
- **Delimiter:** comma (`,`)
- **Quoting:** double-quote all fields including empty ones (`""`)
- **Line endings:** `\n`
- **Header row:** always included as the first row
- **Max rows:** 100 questions per import file

## Column Schema

| Column | Required | Description |
|---|---|---|
| `question` | yes | Full question text shown to respondents. Max 2000 characters. |
| `type` | yes | Question type. See allowed values below. |
| `is_required` | yes | `"true"` or `"false"`. Always include explicitly. |
| `label_preset` | yes* | For `likert` type: selects the response scale. Use `"agreement"` for all pulse surveys. Use `""` for other types. |
| `low_label` | yes* | For `enps` type: label for score 0 (e.g., `"Not Likely"`). Use `""` for other types. |
| `high_label` | yes* | For `enps` type: label for score 10 (e.g., `"Extremely Likely"`). Use `""` for other types. |

*Always include the column; use `""` when not applicable to the row's question type.

## Allowed Values: type

| Value | Meaning |
|---|---|
| `likert` | 5-point scale (always use `label_preset: "agreement"` for pulse surveys) |
| `text` | Open-ended free-text response |
| `yes_no` | Binary yes/no question |
| `enps` | 0–10 scale for Employee Net Promoter Score |

**Note:** FeedbackPulse only supports 5-point Likert scales. Questions marked `likert_3` in the question library are output as `likert` with `label_preset: "agreement"` (5-point).

## Allowed Values: label_preset (for likert)

| Preset | Scale wording |
|---|---|
| `agreement` | Strongly Disagree → Disagree → Neutral → Agree → Strongly Agree |
| `satisfaction` | Very Dissatisfied → Dissatisfied → Neutral → Satisfied → Very Satisfied |
| `frequency` | Never → Rarely → Sometimes → Often → Always |
| `performance` | Far Below Expectations → Below → Meets → Exceeds → Far Exceeds |

Use `agreement` for all standard pulse questions.

## Preamble

The survey preamble (from Step 3 in SKILL.md) is **not** a CSV row. Present it to the user as separate text to paste into FeedbackPulse's survey intro/description field after import, or pass it as the `description` field in the MCP tool call.

## Example CSV — Pulse Survey

```csv
"question","type","is_required","label_preset","low_label","high_label"
"I feel motivated to do my best work right now.","likert","true","agreement","",""
"My workload feels manageable right now.","likert","true","agreement","",""
"I can maintain a healthy pace of work right now.","likert","true","agreement","",""
"I feel positive about where [Company] is headed.","likert","true","agreement","",""
"My manager genuinely cares about my wellbeing.","likert","true","agreement","",""
"I feel I can be myself at work.","likert","true","agreement","",""
"What is one thing that would most improve your experience at work right now?","text","false","","",""
```

## Example CSV — eNPS

```csv
"question","type","is_required","label_preset","low_label","high_label"
"On a scale of 0–10, how likely are you to recommend [Company] as a great place to work?","enps","true","","Not Likely","Extremely Likely"
"What is the main reason for your score?","text","false","","",""
"What would most improve your experience at [Company]?","text","false","","",""
```

## Compatibility

FeedbackPulse's CSV import supports all columns natively. Other tools (SurveyMonkey, Google Forms, Qualtrics, Typeform) do not support full CSV question import — use the CSV as a reference for manual entry or API calls.
