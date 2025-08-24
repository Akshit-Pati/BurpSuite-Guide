# Intruder (Community)

**Intruder** automates sending many requests with varying inputs. Community edition is limited but fine for learning.

> **Use Intruder only against the local training apps described here or systems you own/are authorized to test.**

## Quick Demo (number fuzzing)
1. Capture a request with a numeric parameter (e.g., product `id` on your local app).
2. **Send to Intruder** → **Positions**: Clear § then highlight just the number → **Add §**.
3. **Payloads**: Choose **Numbers**; set a small range (e.g., 1–10).
4. **Start attack** and observe responses for differences (status, length).