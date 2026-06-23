# Security Architecture

OtakuHub uses Flask sessions, CSRF tokens, password hashing, and database-backed users to demonstrate secure user and session management for a remote web application.

## User And Session Management

- Users register with display name, username, email, and password.
- Passwords are hashed with Werkzeug before storage and are never returned by the API.
- Successful registration or login stores `user_id` in the Flask session.
- `/api/auth/me` lets the frontend restore the current user from the session.
- `/api/auth/logout` removes the session user.

## Secure Request Pattern

- All POST, PUT, PATCH, and DELETE requests under `/api/` require a CSRF token.
- Authenticated write routes also require a logged-in session.
- The session cookie is HTTP-only and uses `SameSite=Lax`.
- `SESSION_COOKIE_SECURE=1` can be set in production to require HTTPS cookies.

## Validation And Data Protection

- Registration validates display name length, username format, email format, and password length.
- Uploaded images are limited to JPG, PNG, GIF, and WebP extensions.
- Upload size is capped at 8 MB.
- SQL queries use parameterized placeholders through the database helper layer.
- Secrets and database credentials are loaded from environment variables instead of hard-coded values.

## Role Awareness

The users table includes a `role` field with `user`, `moderator`, and `admin` values. The seeded demo account is an admin account so the project can demonstrate role-based design and can be extended with admin-only moderation routes.
