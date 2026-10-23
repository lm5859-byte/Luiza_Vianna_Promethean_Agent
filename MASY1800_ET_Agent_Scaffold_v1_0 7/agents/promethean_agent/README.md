# Promethean Technology Classification Agent — Assignment 4

Student-editable specialist based on Chapter 11 of *Identifying Promethean Technologies* and the original frozen MASY1800 scaffold. The agent evaluates barrier dissolution, suppression, multi-tier reach, six criteria, evidence for/against, confidence and abstention. It distinguishes technology significance from consulting-application significance and firm-specific management implications.

## Cases
- `cases/primary.json`: management consulting, moderate/fast follower, research/analysis/deliverables.
- `cases/contrast_1.json`: same technology/application, aggressive hype-driven early adopter.
- `cases/contrast_2.json`: same technology and broad application, heightened client confidentiality and regulatory exposure.

## Next steps
Generate prompt packets with `python tools/build_prompt.py --agent agents/promethean_agent --case agents/promethean_agent/cases/primary.json` (repeat for contrasts). Execute each packet separately, preserve raw model JSON, validate with `tools/validate_response.py`, compare outputs, document actual failure/revision in `records/agent_record.md`, and check frozen-core integrity. No model tests have been executed as part of this build.
