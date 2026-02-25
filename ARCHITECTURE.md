# CXSUN CMS – Architecture Overview

This is a CMS platform for building client websites.

Tech stack:
- Backend: ASP.NET Core (.NET 8+)
- Frontend: React
- Orchestration: Microsoft Aspire
- Database: mariadb (planned)
- Auth: JWT (planned)

Projects:
- cxsun.AppHost:
  Aspire orchestration and service wiring

- cxsun.Server:
  CMS backend API
  Responsibilities:
  - Page management
  - Content blocks
  - Media management
  - SEO metadata
  - Multi-tenant (future)

- frontend:
  React frontend for CMS UI
  Admin dashboard + website rendering

Design goals:
- Modular CMS
- Multi-tenant ready
- API-first
- Clean architecture