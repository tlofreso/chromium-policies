# Chromium URL allowlist policy

Locks Chromium down to a fixed set of sites, blocks common bypass routes.

- **`URLBlocklist`/`URLAllowlist`** - blocks all sites except those listed in `URLAllowlist`.
- **Incognito, Guest mode, extra profiles** - disabled, so the allowlist can't be sidestepped.
- **DevTools** - disabled (prevents inspecting/bypassing network requests).
- **Extensions** - all blocked.
- **Proxy** - locked to system settings.
- **`ManagedBookmarks`** - placeholder; fill in once `URLAllowlist` has real domains.
- Password manager on, sync off, metrics reporting off.

## Deploy

```bash
sudo install -m 644 kids.json /etc/chromium/policies/managed/
```
