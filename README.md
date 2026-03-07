# ALICE-Browser SaaS

Semantic web browser engine API

## License

AGPL-3.0

## Architecture

```
Frontend :3000  -->  API Gateway :8080  -->  Core Engine :8081
```

| Layer | Port | Technology |
|-------|------|-----------|
| Frontend | 3000 | Next.js 14, Tailwind CSS |
| API Gateway | 8080 | Rust, Axum |
| Core Engine | 8081 | Rust, Axum, ALICE-Browser |

## Endpoints

| Method | Path | Description |
|--------|------|-------------|
| `POST /api/v1/render` | ページレンダリング |
| `POST /api/v1/parse` | HTML/CSSパース |
| `GET  /api/v1/capabilities` | レンダリング機能一覧 |
| `GET`  | `/health` | ヘルスチェック |

## Quick Start

```bash
cd services/core-engine
cargo run --release
curl http://localhost:8081/health
```

## Author

Moroya Sakamoto
