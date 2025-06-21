# K-zoosik Portfolio (2025 데이터베이스 Term Project)

[설계서 Notion 링크](https://nano5.notion.site/Spring-Data-JPA-MySQL-1abdaf211d42817581b9e3dd2ed9d21f?pvs=4)

## 프로젝트 개요

K-zoosik Portfolio는 국내 주식 투자자들이 자신만의 포트폴리오를 만들고,  
종목을 추가/삭제하며 투자 비중을 관리할 수 있는 웹 기반 서비스입니다.  


## 주요 기술 스택

- Spring Boot 3.x (Kotlin)
- MySQL 8.x
- Spring Data JPA
- Gradle
- REST API (JSON)

## 데이터베이스 ERD
<pre> ```mermaid erDiagram app_user ||--o{ portfolio : "소유" portfolio ||--o{ portfolio_stock : "구성" stock ||--o{ portfolio_stock : "포함" app_user { INT user_id PK "사용자 ID" VARCHAR username "이름" VARCHAR email "이메일" VARCHAR user_pw "비밀번호" DATETIME created_at "가입일" } portfolio { INT portfolio_id PK "포트폴리오 ID" INT user_id FK "사용자 ID" VARCHAR portfolio_name "포트폴리오명" DATETIME created_at "생성일" } stock { INT stock_id PK "종목 ID" VARCHAR stock_name "종목명" VARCHAR stock_code "종목코드" VARCHAR market "시장" VARCHAR sector "섹터" } portfolio_stock { INT portfolio_id PK,FK "포트폴리오 ID" INT stock_id PK,FK "종목 ID" DECIMAL weight "비중(%)" } ``` </pre>








