# Campus Notifications Microservice

This repository contains the required submission folders:

- `logging_middleware`: reusable logging package with `Log(stack, level, package, message)`.
- `notification_app_be`: Stage 1 priority notification ranking code.
- `notification_app_fe`: Stage 2 React + Material UI frontend.
- `notification_system_design.md`: architecture and stage design notes.

## Setup

Install all workspace dependencies:

```bash
npm install
```

Create frontend environment values:

```bash
copy notification_app_fe\.env.example notification_app_fe\.env.local
```

Set `VITE_AUTH_TOKEN` in `notification_app_fe/.env.local` to the bearer token returned by the authorization API.

For the Stage 1 Node script, set the same token as `AUTH_TOKEN`:

```bash
$env:AUTH_TOKEN="your_access_token"
npm run stage1
```

For a local algorithm check without the protected API:

```bash
npm run stage1:sample
```

Run the frontend on the required local port:

```bash
npm run dev:frontend
```

Open `http://localhost:3000`.

