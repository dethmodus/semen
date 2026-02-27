# Learnings Log

## [LRN-20260222-001] knowledge_gap

**Logged**: 2026-02-22T16:42:00Z
**Priority**: medium
**Status**: pending
**Area**: config

### Summary
CLAUDE_TOOL_OUTPUT env variable is NOT required for OpenClaw - it's specific to Claude Code/Codex coding agents.

### Details
Self-improving-agent skill shows "blocked" status on Agent37 dashboard due to missing CLAUDE_TOOL_OUTPUT. However, author @pskoett confirmed this requirement was removed for OpenClaw compatibility. The env var is used by Claude Code/Codex hooks (error-detector.sh) to capture tool outputs, but OpenClaw uses different mechanism with workspace-based skill loading and manual logging.

When using self-improvement skill in OpenClaw:
- Just create `.learnings/` folder with ERRORS.md, LEARNINGS.md, FEATURE_REQUESTS.md
- Log manually via tool calls
- No CLAUDE_TOOL_OUTPUT needed
- Hooks (activator.sh, error-detector.sh) are opt-in and mainly for Coding Agents

### Suggested Action
Add note to TOOLS.md about OpenClaw vs Claude Code skill differences to avoid confusion when checking skill status on ClawHub.

### Metadata
- Source: user_feedback
- Related Files: /home/node/.openclaw/workspace/.learnings/
- Tags: openclaw, claude_tool_output, self-improvement, agent37
- See Also: https://clawhub.ai/pskoett/self-improving-agent
- Pattern-Key: openclaw.skill-env-requirements
- Recurrence-Count: 1
- First-Seen: 2026-02-22
- Last-Seen: 2026-02-22

---
