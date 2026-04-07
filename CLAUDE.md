# Project: Magentus Salesforce Metadata

## Salesforce Flow Skill

When creating or editing Salesforce Flow XML files (`.flow-meta.xml`), follow the sf-flow skill instructions at:
`~/.claude/plugins/marketplaces/sf-skills/sf-flow/SKILL.md`

### Key references:
- **Templates**: `~/.claude/plugins/marketplaces/sf-skills/sf-flow/templates/`
- **Docs**: `~/.claude/plugins/marketplaces/sf-skills/sf-flow/docs/`
- **Examples**: `~/.claude/plugins/marketplaces/sf-skills/sf-flow/examples/`
- **Validation script**: `python3 ~/.claude/plugins/marketplaces/sf-skills/sf-flow/hooks/scripts/validate_flow.py <flow-file>`
- **Simulation script**: `python3 ~/.claude/plugins/marketplaces/sf-skills/sf-flow/hooks/scripts/simulate_flow.py <flow-file> --test-records 200`

### Flow generation workflow:
1. Read the appropriate template from the templates directory
2. Generate Flow XML following SKILL.md best practices (API 62.0, auto-layout, no DML in loops, fault paths on all DML)
3. Write to `force-app/main/default/flows/`
4. Validate with the validation script
5. Always ask before committing or pushing
