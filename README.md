# ft_transcendence
42 School - Level06

A full stack web application

## Setup

The program requires certain environment variables for the different services:

srcs/.env
Variable | Value
--- | ---
NODE_ENV | `development` or `production`
DATABASE_HOST | Hostname for database service
DATABASE_PORT | Port for database API
BACKEND_HOST | Hostname for backend service
BACKEND_PORT | Port for backend API
BACKEND_WS_PORT | Port for websocket connections
FRONTEND_HOST | Hostname for frontend service
FRONTEND_PORT | Port for frontend API
API42_AUTHORIZE | Redirect link to the API authorize URL of 42 (use quotes)
PROXY_HOST | Hostname for proxy service
DOMAIN_NAME | Domain name (must be first part of the certificate)

srcs/requirements/database/.env
Variable | Value
--- | ---
POSTGRES_DB | Database name
POSTGRES_USER | Database user
POSTGRES_PASSWORD | Database password

srcs/requirements/backend/.env
Variable | Value
--- | ---
API42_ID | 42 API ID
API42_SECRET | 42 API secret
API42_REDIRECT | Place to be redirected after authorization
JWT_SECRET | Jwt secret to validate the session
MFA_APP_NAME | Name to be shown in the MFA application (Google Authenticator)

As the proxy expects a secure connection over port 443, there must be a certificate at `srcs/requirements/proxy/tools`.
The key and the certificate must have the respective names: `<domain name>.key` `<domain name>.crt`
