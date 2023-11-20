# ft_transcendence
42 School - Level06

A full stack web application

## Setup

The program requires certain environment variables for the different services:

srcs/.env
Variable | Value
--- | ---
NODE_ENV | `development` or `production`
DATABASE_HOST | hostname for database service
DATABASE_PORT | port for database API
BACKEND_HOST | hostname for backend service
BACKEND_PORT | port for backend API
BACKEND_WS_PORT | port for websocket connections
FRONTEND_HOST | hostname for frontend service
FRONTEND_PORT | port for frontend API
API42_AUTHORIZE | redirect link to the API authorize URL of 42 (use quotes because contains `=`)
PROXY_HOST | hostname for proxy service
DOMAIN_NAME | domain name (must be first part of the certificate)

srcs/requirements/database/.env
Variable | Value
--- | ---
POSTGRES_DB | database name
POSTGRES_USER | database user
POSTGRES_PASSWORD | database password

srcs/requirements/backend/.env
Variable | Value
--- | ---
API42_ID | 42 API ID
API42_SECRET | 42 API secret
API42_REDIRECT | place to be redirected after authorization
JWT_SECRET | jwt secret to validate the session
MFA_APP_NAME | name to be shown in the MFA application (Google Authenticator)

As the proxy expects a secure connection over port 443, there must be a certificate at `srcs/requirements/proxy/tools`.
The key and the certificate must have the respective names: `<domain name>.key` `<domain name>.crt`
