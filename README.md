# Dots

The Dots platform has three repositories:

| Repo | Contents |
|---|---|
| [dots-backend](https://github.com/ai-agent-projetct/dots-backend) | Node.js/Express API, knex migrations and seeds, and the MySQL database dump (`database/dots.sql`) |
| [dots-frontend](https://github.com/ai-agent-projetct/dots-frontend) | Admin panel (React + TypeScript + Vite) |
| [dots-mobile](https://github.com/ai-agent-projetct/dots-mobile) | Flutter apps: `user_app` (customers) and `provider_app` (service providers) |

## Run order

1. **Backend**: import `database/dots.sql` (or `npm run db:init`), then `npm start` (port 8080).
2. **Frontend**: set `VITE_API_BASE_URL=http://localhost:8080/api/`, then `npm run dev`.
3. **Mobile**: `flutter run --dart-define=API_BASE_URL=http://<backend host>:8080`.

Each repo's README has full setup steps.
