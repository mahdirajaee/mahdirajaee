# Code Reviews: cal.com Open PRs

**Date:** 2026-03-28
**Author:** Mahdi Rajaee

## Summary

Submitted code reviews on four open pull requests in the calcom/cal.com repository. Each review analyzed correctness, security implications, edge cases, and code quality.

## PRs Reviewed

### PR #28621 — fix: return 404 instead of Prisma error when cancelling non-existent booking
- **Verdict:** Solid change. 404 is the correct status code. Suggested verifying that callers don't have stale `NotFoundError` catch blocks.
- **File modified by PR:** `packages/features/bookings/lib/getBookingToDelete.ts`

### PR #28619 — fix: add Content-Security-Policy header for XSS defense-in-depth
- **Verdict:** Raised significant concerns. The CSP uses `unsafe-inline` and `unsafe-eval` which largely negate XSS protection. Overly permissive `connect-src` and `img-src` directives. Recommended nonce-based CSP or `Report-Only` mode first.
- **File modified by PR:** `apps/web/next.config.ts`

### PR #28618 — fix: validate signup input and return 400 instead of 500 for invalid data
- **Verdict:** Improvement in error handling. Noted the PR description doesn't match the actual implementation (claims explicit ZodError handling but relies on `getServerErrorFromUnknown`). Flagged unrelated import reordering.
- **Files modified by PR:** `apps/web/app/api/auth/signup/route.ts`, `packages/prisma/zod-utils.ts`

### PR #28601 — fix: upgrade kysely to fix SQL injection vulnerability
- **Verdict:** Version bump is correct. Flagged a yarn.lock artifact where `workspace:*` changed to `npm:*` for `@calcom/lyra` dependencies, which could affect monorepo resolution. Also noted inconsistent `updatedAt` test mock left as `Date` while `createdAt` was changed to string.
- **Files modified by PR:** `packages/kysely/package.json`, `apps/web/components/booking/BookingListItem.tsx`, `apps/web/components/booking/types.ts`, `apps/web/components/booking/actions/bookingActions.test.ts`, `yarn.lock`
