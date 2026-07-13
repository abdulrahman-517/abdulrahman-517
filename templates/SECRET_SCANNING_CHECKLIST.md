# Secret-Scanning Checklist

Search the current tree and Git history for:

- API keys and bearer tokens
- Passwords and connection strings
- Supabase service-role keys and database URLs
- SSH private keys and deployment keys
- `.env` and `.env.local`
- WhatsApp/Baileys authentication sessions
- Cookies, session JSON, QR credentials, and device identity files
- TLS certificates and private keys
- Cloud credentials
- Webhook secrets
- OAuth client secrets
- Database dumps
- Customer data and personally identifiable information
- Internal server IPs, usernames, and sensitive deployment paths

Recommended commands:

```bash
gitleaks detect --source . --verbose
git log -p --all | grep -Ei "api[_-]?key|secret|token|password|BEGIN .*PRIVATE KEY"
git ls-files | grep -Ei "(\.env|credentials|session|auth|private|\.pem|\.key|dump)"
```

When a secret is found:

1. Treat it as compromised.
2. Rotate or revoke it first.
3. Remove it from the current tree.
4. Decide whether history rewriting is required.
5. Coordinate history rewriting before force-pushing.
6. Document the incident without copying the secret into an issue or README.
