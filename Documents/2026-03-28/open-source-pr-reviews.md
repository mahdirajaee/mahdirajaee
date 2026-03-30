# Open Source PR Code Reviews

**Date:** 2026-03-28
**Author:** Mahdi Rajaee

## Summary

Reviewed 6 open pull requests across 3 high-star open source repositories, submitting constructive code review comments on each.

## PRs Reviewed

### supabase/supabase-js
1. **PR #2198** - Add `success` discriminator field to PostgREST response types
   - Reviewed type-safety of the discriminant field and truthiness check vs explicit null comparison.
2. **PR #2186** - Reject excess properties in insert, update, and upsert
   - Reviewed the `RejectExcessProperties` utility type pattern and potential duplication in overload signatures.

### vercel/swr
3. **PR #4232** - Fix `useSWRImmutable` revalidation on focus
   - Reviewed the config mutation bug and the spread-based fix preventing config leakage between hooks.
4. **PR #4224** - Guard against undefined global state in `createCacheHelper`
   - Reviewed defensive coding for React Native New Architecture and the implications of silently skipping state updates.

### gradio-app/gradio
5. **PR #13159** - Add Starlette 1.0 compatibility
   - Reviewed the version constraint change and flagged potential breaking API changes in Starlette 1.0.
6. **PR #13156** - Fix unbounded memory growth in queue event tracking
   - Reviewed the dict-to-LRUCache migration and active cleanup logic in event processing.

## Files Modified

- No files in this repository were modified. Reviews were submitted as comments on external GitHub pull requests.
