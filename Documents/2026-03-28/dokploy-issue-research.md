# Dokploy Repository Research - Issue Ideas

**Date:** 2026-03-28
**Repository:** Dokploy/dokploy (v0.28.8)
**Task:** Research genuine problems and draft issue proposals

## Files Analyzed
- `apps/dokploy/pages/api/deploy/[refreshToken].ts`
- `apps/dokploy/pages/api/deploy/compose/[refreshToken].ts`
- `apps/dokploy/server/queues/deployments-queue.ts`
- `apps/dokploy/server/utils/deploy.ts`
- `packages/server/src/services/notification.ts`
- `packages/server/src/services/deployment.ts`
- `apps/dokploy/server/wss/docker-container-logs.ts`
- `apps/dokploy/server/wss/terminal.ts`
- `apps/dokploy/server/wss/utils.ts`
- `Dockerfile`, `Dockerfile.server`
- `packages/server/src/db/schema/server.ts`
- Various queue and config files

## Issues Identified
1. extractImageTag returns registry port number instead of "latest" for portless private registry images
2. Deployment worker silently swallows errors, leaving application status permanently stuck on "running"
3. Notification service has inconsistent volumeBackup field handling across providers
