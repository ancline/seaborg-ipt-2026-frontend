# Seaborg IPT 2026 - Frontend

Angular 21 frontend for the Seaborg IPT 2026 authentication boilerplate with email sign-up, verification, JWT authentication, and forgot password.

## Live URLs

| Service      | URL                                                       |
| ------------ | --------------------------------------------------------- |
| Frontend     | https://seaborg-ipt-2026-frontend.onrender.com            |
| Backend API  | https://seaborg-ipt-2026-backend.onrender.com             |
| Swagger Docs | https://seaborg-ipt-2026-backend.onrender.com/api-docs    |

## Tech Stack

- Angular 21
- TypeScript
- JWT Authentication (access + refresh tokens)
- Reactive Forms
- Bootstrap

## Features

- User registration with email verification
- Login with JWT access and refresh tokens
- Forgot password / reset password flow
- Role-based access control (Admin / User)
- Admin panel to manage accounts
- Profile update and account deletion

## Pages

| Route                          | Description               | Access |
| ------------------------------ | ------------------------- | ------ |
| `/account/login`               | Login                     | Public |
| `/account/register`            | Register                  | Public |
| `/account/verify-email`        | Email verification        | Public |
| `/account/forgot-password`     | Forgot password           | Public |
| `/account/reset-password`      | Reset password            | Public |
| `/profile/update`              | Update profile            | User   |
| `/admin/accounts`              | Manage all accounts       | Admin  |
| `/admin/accounts/add`          | Create account            | Admin  |
| `/admin/accounts/edit/:id`     | Edit account              | Admin  |

## Setup Instructions

### Prerequisites

- Node.js v18+
- Angular CLI v21+

### Local Development

1. Clone the repository:

```bash
git clone https://github.com/ancline/seaborg-ipt-2026-frontend.git
cd seaborg-ipt-2026-frontend
```

2. Install dependencies:

```bash
npm install
```

3. Update the API URL in `src/environments/environment.ts`:

```ts
export const environment = {
  production: false,
  apiUrl: 'http://localhost:4000'
};
```

4. Run the development server:

```bash
ng serve
```

5. Open `http://localhost:4200` in your browser.

### Production Build

```bash
ng build --configuration production
```

## Notes

- The free Render instance may take **50+ seconds** to wake up after inactivity
- Make sure the backend is running before testing authentication flows
- The first registered account is automatically assigned the **Admin** role