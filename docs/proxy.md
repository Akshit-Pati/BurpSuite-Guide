# Proxy Setup (HTTP & HTTPS)

> Goal: Send your browser traffic through Burp so you can observe and test requests **to local training apps**.

## 1) Burp Proxy Listener
- Open Burp → **Proxy** → **Proxy settings** → **Proxy Listeners**.
- Ensure a listener is running on **127.0.0.1:8080** (default).

## 2) Browser Proxy Settings
### Firefox
1. **Settings** → **Network Settings** → **Manual proxy configuration**.
2. HTTP Proxy: `127.0.0.1` Port: `8080`  
   Check **Use this proxy server for all protocols**.
3. Visit `http://burp` in the browser to download the **CA certificate**.

### Chrome (via OS settings)
- Set system proxy to **127.0.0.1:8080**, or use an extension like **FoxyProxy** to toggle.

## 3) Trust the Burp CA (for HTTPS)
- Open `http://burp` → **CA Certificate** → save.
- In **Firefox**: Settings → Privacy & Security → Certificates → **View Certificates…** → **Authorities** → **Import** → select the file → **Trust to identify websites**.
- In **Chrome** (Windows): Settings → Security → Manage certificates → **Trusted Root Certification Authorities** → **Import**.

## 4) Intercept On/Off
- **Proxy → Intercept** → toggle **Intercept is on**.  
- When ON, requests pause in Burp before reaching the server; click **Forward** to send.  
- When OFF, traffic flows through but is still captured in **HTTP history**.

> **Reminder:** Keep your testing to **local training apps or systems you own/are authorized to test**.
