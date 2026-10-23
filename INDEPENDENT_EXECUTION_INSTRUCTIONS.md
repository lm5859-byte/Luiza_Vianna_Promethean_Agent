# Assignment 4 — independent execution and completion guide

## Status
The saved prompt packets have **not** been independently executed. The existing `analyst_authored_*.json` files are illustrative scenario analyses, not actual test evidence. Do not rename them as actual responses.

## Execute three separate runs
In three separate new model conversations or independently configured model runs, paste the **complete contents** of each of the following files as the user prompt. Request the response in JSON only, without markdown fences, then save the entire returned JSON **unaltered**:

| Prompt packet | Output filename |
|---|---|
| `work/promethean_agent_primary_prompt.txt` | `agents/promethean_agent/responses/actual_primary_response.json` |
| `work/promethean_agent_contrast_1_prompt.txt` | `agents/promethean_agent/responses/actual_contrast_1_response.json` |
| `work/promethean_agent_contrast_2_prompt.txt` | `agents/promethean_agent/responses/actual_contrast_2_response.json` |

If the model adds code fences or other text, preserve the original raw text in a separate `.txt` file; do not claim an edited JSON is the raw output. Record execution date, model and settings, and any formatting problems.

## Validate each raw response
From the scaffold root:

```bash
python tools/validate_response.py agents/promethean_agent/responses/actual_primary_response.json
python tools/validate_response.py agents/promethean_agent/responses/actual_contrast_1_response.json
python tools/validate_response.py agents/promethean_agent/responses/actual_contrast_2_response.json
python tools/check_frozen_core.py
```

## Compare the tests
Compare general classification, barrier statement, suppression logic, multi-tier reach, six criteria, confidence, strongest counterevidence, application-level significance, and management action. The general classification should not change solely because the firm's adoption posture or client-risk context changes.

## Preserve a genuine observed defect
If a real response overclaims irreversible societal dependence, confuses task productivity with categorical dissolution, treats hype as evidence, or fails to adapt local recommendations, copy the **unedited** failing output to the evidence directory. Revise only `agents/promethean_agent/specialist_instructions.md`, document the exact change and reason, rebuild the corresponding prompt with the unchanged case, rerun that case separately, and preserve both original and revised outputs. Do not invent a failure or improvement if no failure occurs; report the limitation honestly.

## Final deliverables
Complete the Agent Record using actual results, update the half-page independent judgment, AI/verification note, and <=100-word Craft Gained reflection to reflect what genuinely happened, and zip the scaffold. The assignment also requires an agent output report. The existing drafts in `work/` are not evidence of independent execution.
