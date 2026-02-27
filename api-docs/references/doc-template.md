# API 문서 출력 템플릿

아래 형식에 맞춰 API 문서를 생성한다.

---

## {모듈명} API

> 마지막 업데이트: {날짜}

### 개요

- Base Path: `/api/v1/{module}`
- 컨트롤러: `{ControllerName}`
- 총 엔드포인트: {N}개

---

### 엔드포인트 목록

| # | Method | Path | 설명 | Guard |
|---|--------|------|------|-------|
| 1 | GET | `/api/v1/example` | 예시 조회 | JwtAuthGuard |
| 2 | POST | `/api/v1/example` | 예시 생성 | JwtAuthGuard, RolesGuard |

---

### 엔드포인트 상세

#### 1. {설명}

```
{METHOD} {Full Path}
```

**Guard**: `{Guard 목록}`

**Request**

| 위치 | 파라미터 | 타입 | 필수 | 설명 |
|------|---------|------|------|------|
| Body | name | string | Y | 이름 |
| Query | page | number | N | 페이지 번호 (기본값: 1) |
| Param | id | number | Y | 리소스 ID |

**Request DTO**: `{DtoClassName}`

```typescript
{
  name: string;       // 이름
  description?: string; // 설명 (선택)
}
```

**Response**

```typescript
{
  id: number;
  name: string;
  createdAt: Date;
}
```

---

### DTO 정의

#### {DtoClassName}

| 필드 | 타입 | 필수 | 검증 규칙 | 설명 |
|------|------|------|----------|------|
| name | string | Y | @IsString, @MaxLength(50) | 이름 |
| description | string | N | @IsOptional, @IsString | 설명 |
