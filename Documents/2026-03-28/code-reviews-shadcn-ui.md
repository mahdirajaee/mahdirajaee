# Code Reviews on shadcn-ui/ui

## Summary of Changes
Submitted code reviews on three open pull requests in the shadcn-ui/ui repository.

### PR #10215 - fix(sink): replace date input with calendar picker
- Reviewed the serialization fix for `useActionState` crash
- Flagged that calendar state is disconnected from `formState.values.startDate`
- Noted missing `<FieldDescription>` and empty-date edge case
- Called out unrelated `teamSize` schema change

### PR #10201 - separator: fix invisible separator
- Confirmed the root cause: `data-horizontal:` shorthand doesn't match Base UI's `data-orientation="horizontal"` attribute
- Verified fix covers all 5 style variants, RTL variant, and JSON registries
- Suggested grepping for same pattern in other base-ui components

### PR #10213 - fix: pin 10 actions to commit SHA
- Verified all 4 SHAs resolve to valid commits
- Confirmed coverage across all 6 workflow files
- Noted first-party GitHub actions left unpinned (reasonable tradeoff)
- Flagged that `martinbeentjes/npm-get-version-action` is pinned to a `main` commit rather than a release tag

## Files Modified
- No local files modified; reviews submitted via `gh pr review --comment`

## Date
2026-03-28
