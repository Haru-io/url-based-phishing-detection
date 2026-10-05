# Sentinel Frontend

Open `sentinel-single-file.html` in a browser for the standalone UI.

For live scanning, start the FastAPI backend on `http://localhost:8000`.
The frontend calls:
- `POST /api/v1/predict` with `{ "url": "...", "inspect_web": true }`
- `GET /api/v1/history`
- `GET /health`

The backend includes the original XGBoost model plus the safe HTML/web inspection layer. The XGBoost model itself is not retrained or modified.
