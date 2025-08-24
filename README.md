# BurpSuite-Guide 🧰🛡️
*A beginner-friendly guide + labs for learning Burp Suite using safe, legal practice targets.*

> **Legal & ethical only.** Use these techniques **only on systems you own or have explicit permission to test**.  
> The labs here use intentionally vulnerable apps (OWASP Juice Shop, DVWA) running locally.

## ✨ What you'll learn
- What Burp Suite is and when to use it
- Setting up browser → Burp proxy (HTTP/S)
- Core tools: **Target**, **Proxy**, **HTTP history / Logger**, **Repeater**, **Intruder** (Community), **Decoder**, **Comparer**, **Sequencer**
- Hands-on labs on local training apps

## 📦 Quick start
1. **Install Burp Suite Community** (free): https://portswigger.net/burp/communitydownload  
2. **Install Docker** (recommended for labs): https://docs.docker.com/get-docker/  
3. **Run practice targets locally** (one-time each):
   ```bash
   # OWASP Juice Shop (Port 3000)
   docker run -d --name juice-shop -p 3000:3000 bkimminich/juice-shop

   # DVWA (Ports 8080 web, 3306 mysql); initial creds in DVWA docs
   docker run -d --name dvwa -p 8080:80 vulnerables/web-dvwa
   ```
4. **Open the targets** in your browser:
   - Juice Shop → http://localhost:3000
   - DVWA →   http://localhost:8080
5. **Open Burp** and configure your browser to send traffic through Burp (see `docs/proxy.md`).

## 🗂️ Repository map
```
BurpSuite-Guide/
 ├─ README.md
 ├─ LICENSE
 ├─ docs/
 │  ├─ introduction.md
 │  ├─ installation.md
 │  ├─ features.md
 │  ├─ proxy.md
 │  ├─ repeater.md
 │  ├─ intruder.md
 │  ├─ decoder.md
 │  ├─ comparer.md
 │  ├─ sequencer.md
 │  └─ tips-tricks.md
 ├─ labs/
 │  ├─ proxy_lab.md
 │  ├─ repeater_lab.md
 │  ├─ intruder_lab.md
 │  └─ decoder_lab.md
 └─ images/  (place your screenshots here)
```

## 🧭 How to use this repo
- Start with `docs/introduction.md` → `docs/installation.md` → `docs/proxy.md`.
- Do the labs in `labs/` in order; each lab is < 20 mins and uses only **local** training apps.
- Save your own screenshots inside `images/` and link them in the lab files.

## 🚀 Upload to GitHub (two options)
### A) **Easiest (Web UI)**
1. Create a new repo on GitHub → **BurpSuite-Guide** (Public).
2. Click **Add file → Upload files**, drag-and-drop the contents of this folder.
3. Commit → Done.

### B) **Git (CLI)**
```bash
cd BurpSuite-Guide
git init
git add .
git commit -m "Initial commit: Burp Suite beginner guide + labs"
git branch -M main
git remote add origin https://github.com/<your-username>/BurpSuite-Guide.git
git push -u origin main
```

## 📝 License
This project is released under the **MIT License** (see `LICENSE`).

---

> Made for learners: simple steps, no jargon, and safe practice targets.
