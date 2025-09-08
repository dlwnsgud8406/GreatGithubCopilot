```instructions
---
description: 'API specification template for REST services'
applyTo: '**/*.md'
---

# API Specification Template

This is a reusable template for documenting REST API endpoints. Replace the example content with your service-specific details.

## Endpoint Documentation Template

### Example Endpoint

- **METHOD /api/resource**
  - Description: Brief description of what this endpoint does
  - Request Body (JSON):
    ```json
    {
      "field_name": "example_value"
    }
    ```
  - Response:
    - 200 OK
    - Body:
      ```json
      {
        "id": 1,
        "field_name": "example_value"
      }
      ```

### Example Collection Endpoint

- **GET /api/resources**
  - Description: Retrieve all resources
  - Response:
    - 200 OK
    - Body:
      ```json
      [
        {"id": 1, "name": "Resource 1"},
        {"id": 2, "name": "Resource 2"}
      ]
      ```

## Guidelines

- Use clear, descriptive endpoint names
- Include request/response examples for all endpoints
- Document required fields and validation rules
- Specify HTTP status codes for different scenarios

```

## 2. 회식 이벤트 목록 조회

- **GET /api/events**
  - 설명: 생성된 모든 회식 이벤트를 조회합니다.
  - 응답:
    - 200 OK
    - Body:
      ```json
      [
        {"event_id": 1, "name": "2025년 7월 회식"},
        {"event_id": 2, "name": "2025년 8월 회식"}
      ]
      ```

## 3. 메뉴 후보 제안 (이벤트별)

- **POST /api/events/{event_id}/menus**
  - 설명: 특정 회식 이벤트에 메뉴 후보를 제안합니다.
  - 요청 Body (JSON):
    ```json
    {
      "name": "삼겹살"
    }
    ```
  - 응답:
    - 201 Created
    - Body:
      ```json
      {
        "id": 1,
        "event_id": 1,
        "name": "삼겹살"
      }
      ```

## 4. 메뉴 후보 목록 조회 (이벤트별)

- **GET /api/events/{event_id}/menus**
  - 설명: 특정 이벤트에 제안된 모든 메뉴 후보를 조회합니다.
  - 응답:
    - 200 OK
    - Body:
      ```json
      [
        {"id": 1, "event_id": 1, "name": "삼겹살"},
        {"id": 2, "event_id": 1, "name": "치킨"}
      ]
      ```

## 5. 메뉴 후보에 투표 (이벤트별)

- **POST /api/events/{event_id}/votes**
  - 설명: 특정 이벤트의 메뉴 후보에 투표합니다.
  - 요청 Body (JSON):
    ```json
    {
      "menu_id": 1
    }
    ```
  - 응답:
    - 201 Created
    - Body:
      ```json
      {
        "vote_id": 10,
        "event_id": 1,
        "menu_id": 1
      }
      ```

## 6. 투표 현황/결과 조회 (이벤트별)

- **GET /api/events/{event_id}/results**
  - 설명: 특정 이벤트의 각 메뉴 후보별 투표 수를 조회합니다.
  - 응답:
    - 200 OK
    - Body:
      ```json
      [
        {"menu_id": 1, "name": "삼겹살", "votes": 5},
        {"menu_id": 2, "name": "치킨", "votes": 3}
      ]
      ```

---

## 공통 사항

- 모든 요청/응답은 JSON 형식 사용
- 익명 참여(별도의 인증 없음)
- 에러 발생 시 표준 HTTP 상태코드 및 메시지 반환