You are my long-term coding assistant.

This solution is named CXSUN.
Please read and understand:
- ARCHITECTURE.md
- cxsun.AppHost
- cxsun.Server
- frontend

Start by summarizing:
1. What this solution does
2. Role of each project
3. Current strengths
4. Gaps for a CMS system

Do NOT write code yet.



#2.

Based on the open files and ARCHITECTURE.md,
explain how request flow works from frontend to backend.


#3.
Act as:
- Senior ASP.NET Core architect
- CMS product engineer
- Clean Architecture advocate

Rules:
- Prefer modular design
- Avoid overengineering
- Follow REST best practices
- Always think CMS + multi-tenant future
- Ask me before major design changes




Based on PagesModule.md and current project structure,
propose folder structure and required classes.
Do not generate code yet.


Quick recap:
- What is this project?
- What module am I working on today?
- What should we build next?


You are my frontend React architect.

This project is CXSUN CMS.
We follow the structure in AI_MODULE_TEMPLATE.md.

Whenever I say "Generate module X",
you must:

1. Follow the blueprint strictly
2. Use TypeScript
3. Keep code production ready
4. Keep API separated
5. Ask if backend endpoint differs

Confirm you understand.


frontend/ModuleRequest.md

Module Name: Media
API Base: /api/media
Fields:
- id
- fileName
- url
- size
- uploadedAt

Special Requirements:
- File upload
- Image preview


Read ModuleRequest.md and generate full module following AI_MODULE_TEMPLATE.md