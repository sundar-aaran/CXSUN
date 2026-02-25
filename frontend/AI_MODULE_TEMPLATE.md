# React Module Blueprint (CXSUN CMS)

Each module must follow this structure:

src/modules/{moduleName}/

Files required:

1. types.ts
   - DTO types
   - Form models

2. api.ts
   - Axios API wrapper
   - CRUD methods

3. {ModuleName}List.tsx
   - Table view
   - Pagination
   - Edit/Delete buttons

4. {ModuleName}Editor.tsx
   - Create/Edit form
   - Validation
   - Save handler

5. routes.ts
   - Route configuration

6. index.ts
   - Barrel export

Rules:
- Use functional components
- Use hooks
- Use TypeScript
- Keep components small
- Separate UI from API logic
- No business logic inside UI