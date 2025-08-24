# Lab: Using the Proxy

**Goal:** Route browser traffic for **Juice Shop** through Burp, intercept one request, and forward it.

## Steps
1. Start Juice Shop: `docker start juice-shop` (or run command from README if first time).
2. Configure browser proxy to `127.0.0.1:8080` (see `docs/proxy.md`) and install the Burp CA.
3. Visit `http://localhost:3000` and browse the shop.
4. In Burp **Proxy → Intercept**, turn **Intercept is on** and refresh the page.
5. Observe the paused request; click **Forward** until the page loads.
6. Turn **Intercept is off** and review **HTTP history**.
7. Take a screenshot and save it in `images/`.
