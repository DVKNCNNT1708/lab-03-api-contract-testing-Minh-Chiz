# Consumer–Provider Handshake

## Thông tin chung

- Lab: FIT4110 Lab 03
- Ngày: 26/05/2026
- Provider team: team-vision
- Consumer team: team-gate
- Provider service: AI Vision API
- Consumer service: Access Gate Service

## Contract

- Contract file: contracts/ai-vision.openapi.yaml
- Mock base URL: http://localhost:4011
- Auth method: Bearer Token (JWT)
- Endpoint được test: POST /detect

## Smoke test

### Request

```http
POST /detect
Authorization: Bearer lab-token
Content-Type: application/json

{
  "camera_id": "CAM01",
  "image_url": "[https://example.com/frame.jpg](https://example.com/frame.jpg)"
}

{
  "detection_id": "DET001",
  "camera_id": "CAM01",
  "label": "person",
  "confidence": 0.91,
  "risk_level": "medium"
}