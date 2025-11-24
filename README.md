# 🛡️ LogSaver: Client-Side SOC Log Sanitizer

**LogSaver** is a secure, privacy-first tool for sanitizing sensitive SOC logs (SIEM, Firewall, Cloud) directly in your browser. No data ever leaves your device.

## 🚀 Live Demo
**(Optional) Enable GitHub Pages to host this tool instantly!**
1.  Go to your repository **Settings**.
2.  Click **Pages** on the left sidebar.
3.  Under **Source**, select `main` branch and `/ (root)` folder.
4.  Click **Save**. Your tool will be live at `https://<your-username>.github.io/<repo-name>/`.

---

## 🧐 What is LogSaver?
**LogSaver** is a tool built for Security Analysts, Incident Responders, and DevSecOps professionals who need to share logs but cannot risk leaking sensitive data.

### Security Assessment (Why Trust This?)
*   **✅ Secure by Design**: The entire logic executes within your browser's JavaScript engine. No data is sent over the network.
*   **✅ No Persistence**: Data is volatile. Refreshing the page wipes the memory, ensuring no sensitive data lingers.
*   **✅ Transparent**: The code is open source and unminified. Any analyst can "View Source" to verify safety.

---

## 📊 Feature Analysis

| Feature | Analyst Benefit | Rating |
| :--- | :--- | :--- |
| **Smart Redaction** | Saves hours of manual "Find & Replace". Automatically detects and sanitizes PII (Emails, IPs), Secrets (AWS Keys, JWTs), and System Paths. | ⭐⭐⭐⭐⭐ |
| **Fake Data** | Replaces sensitive info with realistic fake data (e.g., `alice@example.com` instead of `[REDACTED]`). This keeps the log's "shape" valid for SIEM parsers. | ⭐⭐⭐⭐⭐ |
| **Interactive Whitelist** | Critical for triage. Select specific values (like your own IP) to keep them visible while sanitizing everything else. | ⭐⭐⭐⭐ |
| **JSON Awareness** | Respects JSON structure. Unlike regex-only tools that break JSON, LogSaver parses and traverses the tree to sanitize values safely. | ⭐⭐⭐⭐⭐ |

---

## 🎯 Target Audience
*   **SOC Analysts**: Sanitize logs before attaching them to public tickets (Jira, ServiceNow) or asking for help on forums.
*   **Incident Responders**: Share Indicators of Compromise (IOCs) with external partners without revealing internal network architecture.
*   **DevSecOps**: Clean production logs for use in staging or test environments.

---

## 🛠️ Usage
1.  **Open the Tool**:
    -   **Online**: Visit the GitHub Pages link.
    -   **Local**: Double-click `static/index.html` to open it in any browser.
2.  **Load a Sample**: Use the dropdown to load sample logs (AWS, Azure, Splunk, etc.).
3.  **Configure**:
    -   **Strategy**: Choose Redact, Mask, Hash, or Fake Data.
    -   **Whitelist**: Select text in the input and click "Whitelist Selection" to keep it.
    -   **Custom Tags**: Select text and click "Sanitize Selection" to redact it.
4.  **Run**: Click **Sanitize Log** to process.

---

## 🗺️ Future Roadmap
We are constantly improving LogSaver. Here is what's coming next:

### Phase 1: Usability
- [ ] **Drag & Drop File Upload**: Process large log files line-by-line.
- [ ] **Persistence**: Save custom tags and whitelist settings locally.
- [ ] **Dark Mode Toggle**: Switch between light and dark themes.

### Phase 2: Advanced Features
- [ ] **CIDR Support**: Whitelist IP ranges (e.g., `192.168.0.0/24`).
- [ ] **Export to File**: Download sanitized logs as `.json` or `.txt`.
- [ ] **CLI Version**: Node.js script for pipeline integration.

---

## 📄 License
[MIT](LICENSE) - **Privacy & Liability Disclaimer**: This tool is provided "as is". The user assumes full responsibility for verifying sanitized output. No data is stored or transmitted by the authors.
