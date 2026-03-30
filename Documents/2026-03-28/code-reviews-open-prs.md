# Code Reviews on Open PRs

**Date:** 2026-03-28
**Author:** Mahdi Rajaee

## Summary

Reviewed 6 open pull requests across 3 repositories, submitting detailed technical review comments via `gh pr review --comment`.

## PRs Reviewed

1. **streamlit/streamlit #14546** - Case-insensitive `st.switch_page`: Noted `.lower()` vs `casefold()` for Unicode safety; test coverage is solid.
2. **streamlit/streamlit #14552** - File extension dedup in uploader: Clean `EXTENSION_PAIRS` design; flagged potential frontend/backend drift of the pairs list.
3. **fastapi/sqlmodel #1823** - Validate table models on init: Breaking change for users relying on missing-required-field construction; thorough test suite covering validators and ORM load bypass.
4. **fastapi/sqlmodel #1831** - Async session tutorial: Flagged misleading `sqlite_url` variable name, missing error handling, and non-self-contained code blocks.
5. **platformio/platformio-core #5302** - Fix hardcoded PASSED status: Correct use of `status.name` and `to_ansi_color()`; noted unrelated `piobuild.py` changes in the diff.
6. **platformio/platformio-core #5303** - Circular extends detection: Silent skip vs warning on cycle detection; noted mixed concerns in the diff.

## Files Modified

No files in this repository were modified. Reviews were submitted as GitHub PR comments via the `gh` CLI.
