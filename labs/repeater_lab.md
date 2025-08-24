# Lab: Repeater Basics

**Goal:** Capture a search request from **Juice Shop** and replay it with different query values.

## Steps
1. With proxy configured, use the shop's search feature.
2. In **HTTP history**, locate the request (path typically includes `/rest/products/search`).
3. Right-click → **Send to Repeater**.
4. Change the search term parameter (e.g., `q=notebook` → `q=shirt`) and click **Send**.
5. Compare response length/status. Save screenshots to `images/`.
