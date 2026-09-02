# Base44 environment notes

- The app is a static PWA with no build step or backend. User data is stored in browser `localStorage`.
- `docker-compose.base44.yml` serves the bind-mounted repository through BrowserSync on port 3000, so source edits reload without rebuilding an image.
- Firebase/Firestore synchronization is optional and disabled while `FIREBASE_CONFIG` is `null`; no external credentials are required for local-only operation.
- Verify startup with `curl -fsS http://localhost:3000/` and with a non-localhost Host header to catch preview-host restrictions.
