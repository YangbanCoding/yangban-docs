# 로그인
## 설정
- RSA 키 만들기
```bash
openssl genrsa -out private.pem 2048
openssl rsa -in private.pem -pubout > public.pem
```
- 키 텍스트로 표시하기
```bash
awk -v ORS='\\n' '1' private.pem
awk -v ORS='\\n' '1' public.pem
```

## 백엔드
- docker-compose 설정
```yaml
...생략
services:
  graphql-engine:
    environment:
       HASURA_GRAPHQL_ADMIN_SECRET: [관리자 비밀번호]
       HASURA_GRAPHQL_JWT_SECRET: '{"type": "RS256", "key": "[public 키]"}'
       ACTION_BASE_URL: [액션 URL] # 예: http://host.docker.internal:3001/api
...생략
```

## 프론트엔드
