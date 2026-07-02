# GitHub Issue Resolution Workflow

**Trigger**: ONLY when the user pastes a GitHub issue link AND explicitly says they are assigned to it (e.g. "I'm assigned to this issue", "this is assigned to me"). Do NOT auto-trigger this workflow for random issue links or general questions.
**important** after the plan create a new branch wrt the repository guidelines and then only proceed w the edits

Follow this exact workflow:

## 1. Analyze & Understand
- Read the repository's CONTRIBUTING.md / README.md for project guidelines
- Fetch and read the full issue (title, body, comments)
- Explore codebase to locate the issue and understand root cause
- Check issue comments for any existing proposed plans
- **If anything is unclear: ASK QUESTIONS** — do not assume. Ask until 100% clear.

## 2. Plan
- Formulate a complete step-by-step plan comparing your analysis with any proposed plan in comments
- **Present the plan and wait for explicit approval** — no edits, no branch creation before approval

## 3. Execute (only after approval)
- Create a new branch following repository guidelines
- Implement the fix only — no unrelated edits, no test/build commits unless explicitly asked
- If you find other bugs: note them, report them, do NOT fix them

## 4. Verify & Commit
- Recheck the fix against the original issue requirements
- Ensure CI checks will pass
- **Ask for approval before committing**
- For UI/visual changes: provide clear steps to verify the change visually

## 5. PR Comments (if requested)
- Focus only on the original fix done for the issue
- Be very concise and human-like
- all comments (assignement and pr comments) i ask should be in a proper copy pastable md format
