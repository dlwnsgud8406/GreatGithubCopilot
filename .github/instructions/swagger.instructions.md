---
applyTo: '**'
---

# Swagger/OpenAPI Documentation Template

This template provides guidance for projects using Swagger/OpenAPI documentation, particularly with auto-generated docs like FastAPI.

## Swagger UI Access

For projects with auto-generated Swagger documentation:
- **Swagger UI**: Usually available at `http://localhost:PORT/docs`
- **OpenAPI Schema**: Typically at `http://localhost:PORT/openapi.json`
- Replace `PORT` with your application's port (commonly 8000, 3000, etc.)

## Using Swagger UI

- View API endpoint specifications, parameters, and examples
- Use "Try it out" feature to test endpoints directly
- Review request/response schemas and validation rules
- Test authentication flows if applicable

## Documentation Guidelines

- Ensure documented endpoints match actual API implementation
- Keep request/response examples up to date
- Use Swagger UI for manual testing during development
- Verify all endpoints return expected status codes
- Document authentication requirements clearly
- 예시 요청/응답은 실제 명세(api_spec.instructions.md)와 일치해야 합니다.
- Swagger UI를 통한 테스트 방법을 구체적으로 안내하세요.

## 4. 기타

- 모든 요청/응답은 JSON 형식입니다.
- Swagger 문서는 FastAPI가 자동으로 생성하므로 별도 설정이 필요 없습니다.
- 문서화된 엔드포인트를 기준으로 테스트 및 코드 생성을 진행하세요.

## Swagger / Manual Verification
- uvicorn으로 앱을 실행한 뒤 `/docs`가 열리는지 확인한다.
- 모든 엔드포인트의 request/response 예시가 표시되는지 확인한다.
- 최소 1개 happy-path를 Swagger "Try it out"으로 호출해 2xx를 확인한다.

## Quickstart
```bash
source .venv/bin/activate
uvicorn app.main:app --reload


API Docs
Swagger UI: http://127.0.0.1:8000/docs
ReDoc: http://127.0.0.1:8000/redoc