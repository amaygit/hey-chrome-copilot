# Hey Chrome Copilot

Private deployment repository for the universal voice browser assistant.

The credential-free source is versioned in `hey-chrome-source.tar.gz`. Render extracts it during the build and runs `node server/index.mjs`. The archive includes the extension, server, tests and full documentation.

Build: `tar -xzf hey-chrome-source.tar.gz --strip-components=1 && node --check server/index.mjs`

Health check: `/healthz`

Gemini credentials and owner access codes are supplied only through Render environment settings. They are not included in this repository. Named member registrations can be provided through `ACCESS_MEMBERS_JSON` so they survive free-tier restarts.
