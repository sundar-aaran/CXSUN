# TODO

This is a concise, incremental checklist for building the CXSUN CMS features. Follow the items top-to-bottom and mark them as complete as we progress.

## Phase 0 — Decisions
- [ ] Confirm persistence provider (EF Core + MariaDB)
- [ ] Confirm tenant strategy (nullable `TenantId` start vs enforce tenant from day one)
- [ ] Confirm application pattern (service classes vs MediatR/CQRS)

## Phase 1 — Foundation
- [ ] Restore and build solution targeting .NET 10
- [ ] Add project scaffolding for modular features: `Modules/Pages`, `Modules/Media`
- [ ] Add shared abstractions: `IUserContext` / `ITenantProvider`, `ICacheService`, logging/telemetry hooks

## Phase 2 — Persistence
- [ ] Add EF Core and MariaDB provider NuGet packages
- [ ] Create `PagesDbContext` and initial EF model for `Page` and `ContentBlock`
- [ ] Add repository interfaces and EF implementations
- [ ] Add EF migrations and local dev configuration

## Phase 3 — Pages module (backend)
- [ ] Define domain entities and DTOs for Pages
- [ ] Implement `IPageRepository` and `PageService` (business rules, slug uniqueness)
- [ ] Add REST controllers: `/api/v1/pages` (GET, POST, PUT, DELETE, publish)
- [ ] Add cache invalidation hooks (Redis output cache)

## Phase 4 — Media module (backend)
- [ ] Define media entity and API `/api/media` (list, upload, download, delete)
- [ ] Implement local filesystem media store and preview endpoints
- [ ] Add content validation and size limits

## Phase 5 — Frontend modules
- [ ] Scaffold frontend `Media` module (TypeScript) per `AI_MODULE_TEMPLATE.md`
- [ ] Implement file upload UI and image preview components
- [ ] Implement Pages admin UI to create/edit pages and reference media

## Phase 6 — Auth, multi-tenant, and security
- [ ] Add JWT authentication skeleton and `IUserContext` integration
- [ ] Protect admin endpoints with role-based policies
- [ ] Implement tenant resolution middleware and optional global query filters

## Phase 7 — QA, tests, CI/CD
- [ ] Add unit tests for domain and services
- [ ] Add integration tests for controllers and media upload
- [ ] Add CI workflow (build, test, lint, publish frontend)

## Phase 8 — Observability and ops
- [ ] Ensure OpenTelemetry exporters configured for traces/metrics
- [ ] Add backup/migration docs and runbook for MariaDB
- [ ] Add rate limiting and input sanitization for rich content

## Notes
- Keep changes modular and incremental. Ask before major design pivots (persistence, tenancy, CQRS).
