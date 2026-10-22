VX 405 — Security & Reconnaissance Toolkit

██╗   ██╗██╗  ██╗     ██╗  ██╗ ██████╗ ███████╗
██║   ██║╚██╗██╔╝     ██║  ██║██╔═████╗██╔════╝
╚██╗ ██╔╝ ╚███╔╝      ███████║██║██╔██║███████╗
 ╚████╔╝  ██╔██╗      ╚════██║████╔╝██║╚════██║
  ╚██╔╝  ██╔╝ ██╗         ██║╚██████╔╝███████║
   ╚═╝   ╚═╝  ╚═╝         ╚═╝ ╚═════╝ ╚══════╝

             .  *  .  +  .  *  .
                 .-─────-.
              .-'  \  |  /'-.
             /  ─────●───── \
            |    /  |  \    |
             \   RADAR     /
              '-._______.-'

    ╔══════════════════════════════════════╗
    ║       VX 405 - SECURITY TOOLKIT      ║
    ╚══════════════════════════════════════╝

         OSINT & Security Recon Toolkit
                CREATE BY JAVAS
                     v1.0.0

Version: 1.0.0
Author: JAVAS
Platform: Termux · Linux · Python
Category: OSINT · Reconnaissance · Security Auditing

---

About VX 405

VX 405 is a Python-based security toolkit for authorized reconnaissance, open-source intelligence (OSINT), network diagnostics, and web application security auditing.

It provides a terminal-based interface for organizing security utilities in one place. The project is intended for security researchers, developers, system administrators, and students learning defensive cybersecurity.

Features

- OSINT: Gather publicly available information about domains, IP addresses, and online services.
- DNS Lookup: Inspect A, AAAA, MX, NS, TXT, and CNAME records.
- WHOIS Lookup: Retrieve domain registration information when available.
- Subdomain Discovery: Identify publicly documented subdomains.
- HTTP Header Analysis: Review security-related response headers.
- TLS Certificate Inspection: Examine certificate validity and issuer information.
- Technology Detection: Identify publicly exposed website technologies.
- Security Auditing: Check common web security configuration issues.
- Network Diagnostics: Test connectivity and response latency.
- Interactive Menu: Access available modules from the terminal.
- Termux Support: Run supported modules on Android.
- Reporting: Save assessment results for later review, if enabled in the implementation.

Available functionality depends on the modules implemented in the current source code.

Requirements

- Python 3.8 or newer, depending on dependency compatibility.
- pip.
- Termux or a compatible Linux environment.
- Internet access for online lookups.

Installation

1. Install the requirements on Termux

pkg update && pkg upgrade
pkg install python git

2. Download the project

If the project is hosted in a Git repository:

git clone YOUR_REPOSITORY_URL
cd VX-405

Alternatively, upload or extract the project files into your preferred directory.

3. Create a virtual environment

python -m venv venv
source venv/bin/activate

4. Install dependencies

If "requirements.txt" exists:

python -m pip install --upgrade pip
pip install -r requirements.txt

5. Run VX 405

If the entry-point file is "vx405.py":

python vx405.py

If your main file has another name, replace "vx405.py" with the correct filename.

Usage

1. Start VX 405 from your terminal.
2. Choose an available module from the interactive menu.
3. Enter the domain, IP address, or URL you are authorized to assess.
4. Review the output.
5. Save relevant findings and apply recommended fixes.

Recommended workflow

- Begin with passive reconnaissance.
- Review publicly available information.
- Perform non-destructive security checks.
- Validate findings on authorized systems.
- Document and remediate identified weaknesses.

Tool Categories

1. OSINT & Reconnaissance

Potential modules include:

Module| Purpose
IP Lookup| Retrieve public IP and network information
WHOIS Lookup| Inspect domain registration data
DNS Lookup| Review DNS records
Subdomain Discovery| Find publicly documented subdomains
HTTP Headers| Inspect HTTP security headers
TLS Certificate| Review certificate details
Technology Detection| Identify website technologies
Security.txt| Check vulnerability disclosure information
Metadata Analysis| Review metadata in supplied files

2. Web Security Auditing

Modules can help assess:

- Missing security headers.
- Cookie security attributes.
- CORS configuration.
- Clickjacking protections.
- TLS configuration.
- Exposed development files.
- Common web application misconfigurations.

Active security testing should be limited to explicitly authorized targets and safe validation methods.

3. Network Diagnostics

Potential functionality includes:

- DNS resolution.
- TCP connectivity checks.
- Service availability checks.
- Connection latency measurements.
- TLS connectivity diagnostics.

4. Reports

Where implemented, the reporting module can organize:

- Target information.
- Assessment timestamps.
- Findings and severity.
- Evidence from authorized checks.
- Remediation recommendations.

Configuration

Example configuration values:

APP_NAME = "VX 405"
VERSION = "1.0.0"
AUTHOR = "JAVAS"
REQUEST_TIMEOUT = 10
MAX_WORKERS = 5
VERIFY_TLS = True

These values are examples and must be connected to the application code before they affect runtime behavior.

Keep API keys and other credentials out of source control.

Running on a Hosting Panel

For a Python hosting panel such as Pterodactyl:

1. Upload the project files.
2. Ensure the selected runtime supports the required Python version.
3. Install dependencies from "requirements.txt".
4. Configure the startup command to match the actual entry point.
5. Start the application and review the console output.

A terminal-based application does not automatically provide a website. A browser-accessible dashboard requires a separately implemented web server and appropriate network configuration.

Troubleshooting

Missing Python modules

pip install -r requirements.txt

Check Python syntax

python -m py_compile vx405.py

Application fails to start

Check the entry-point filename, dependency versions, and traceback in the terminal.

Network requests fail

Verify your internet connection, DNS configuration, target availability, and request timeout.

Project Structure

Suggested directory layout:

VX-405/
├── vx405.py
├── requirements.txt
├── README.md
├── config.py
├── modules/
│   ├── osint.py
│   ├── reconnaissance.py
│   ├── web_audit.py
│   └── reporting.py
├── reports/
└── tests/

The actual directory structure may differ from this example.

Authorization & Responsible Use

VX 405 is intended for:

- Authorized security assessments.
- Defensive cybersecurity research.
- Educational exercises.
- Auditing systems owned by the operator.
- Testing conducted under written permission.

Users must obtain authorization before performing active tests, respect privacy, avoid disruptive activity, and comply with applicable laws and service terms.

Disclaimer

VX 405 is provided for educational and authorized security testing purposes. The operator is responsible for ensuring that all activities comply with applicable laws and the scope of authorization.

The author assumes no liability for unauthorized use or damage caused by misuse of the software.

License

Add a license file before redistributing this project. Unless a license grants additional rights, copyright remains with the respective copyright holder.

---

VX 405 Security Toolkit
CREATE BY JAVAS

Discover. Audit. Secure.            |── HTTP GET ──────────────────► |
    |                                |   ... ×50 per multicall        |
    |                                |                                |
    |── system.multicall ──────────► |  (next request)                |
    |   (another 50x pingback.ping)  |                                |
    |                                |── HTTP GET ──────────────────► |  ×50 more
```

**Amplification math**: with 192 relays, 10 threads/relay, and batch size 50:
- You send: 1,920 concurrent multicall streams
- Each multicall triggers 50 pingbacks
- The victim receives up to ~38,400 HTTP requests/second from 192 different IPs, none of which are yours

During the attack, a live status line shows:
- Total pingbacks triggered
- Total HTTP requests sent to relays
- Rate (pingbacks/second)
- Errors
- Per-relay breakdown

### Why Both Vectors Are Required

`system.multicall` and `pingback.ping` serve different roles in the amplification chain:

| Vector | Role |
|--------|------|
| `pingback.ping` | The actual DDoS primitive — WordPress makes an HTTP GET to the victim URL to "verify" the pingback source |
| `system.multicall` | The multiplier — batches N `pingback.ping` calls into a single HTTP request, so 1 request from you = N requests from the relay |

Without `system.multicall`, you can only send one `pingback.ping` per HTTP request (1:1 ratio, no amplification). Without `pingback.ping`, `system.multicall` has nothing to batch. Both are needed for the amplification to work.

### Botnet Menu

| Option | Description |
|--------|-------------|
| 1 | **XML-RPC Multicall Pingback Amplification** - Uses all saved relays to flood a victim URL. Configurable threads per relay (1-50), pings per multicall batch (1-500), and duration (1-300s). Shows live stats with per-relay pingback counts, HTTP request counts, and total rate. |
| 2 | **Add zombie manually** - Add a WordPress site URL to the database without scanning it first. |
| 3 | **Remove zombie** - Remove a specific zombie from the database by number. |
| 4 | **Clear all zombies** - Wipe the entire database. |
| 5 | **Benchmark relay reliability & power** - Tests relay health, speed, and attack readiness. Choose a single relay, a range (e.g. `1-5`), or all relays at once. See [Relay Benchmark](#relay-benchmark) below. |
| 0 | Back to main menu |

The menu header shows the total number of zombies in the database. Each zombie is listed with its URL, CMS type, discovered vectors, and the date it was added.

### Relay Benchmark

Before launching an attack, you can verify which relays are actually usable. The benchmark runs four checks on each selected relay:

| Phase | What it tests |
|-------|---------------|
| **Connectivity** | Is the site reachable? Measures base HTTP latency. |
| **XML-RPC check** | Does `/xmlrpc.php` respond? Are `pingback.ping` and `system.multicall` still available? |
| **Burst throughput** | Sends N consecutive `system.listMethods` requests (configurable, 1-50) and measures success rate and average response time. |
| **Grading** | Assigns a letter grade based on all results. |

**Grading system:**

| Grade | Meaning |
|-------|---------|
| **A** | Excellent — fast (<500ms avg), reliable (>90% success), both vectors present |
| **B** | Good — decent speed (<1500ms), mostly reliable (>70% success) |
| **C** | Usable — slow or with some failures, but vectors are present |
| **D** | Degraded — XML-RPC active but missing `pingback.ping` or `system.multicall` |
| **E** | Broken — site is online but XML-RPC is dead |
| **F** | Offline — site is unreachable |

The output is a summary table showing each relay's grade, latency, XML-RPC status, vector availability, and burst results. Relays graded **E** or **F** are flagged for removal.

### JSON Database

Zombies are stored in `botnet_zombies.json` in the project root. The file is created automatically the first time both DDoS vectors are discovered on a target. Each entry contains:

```json
{
  "url": "https://example.com",
  "cms": "WordPress",
  "vectors": ["pingback.ping", "system.multicall"],
  "xmlrpc_url": "https://example.com/xmlrpc.php",
  "added": "2026-02-19T14:30:00.000000",
  "last_seen": "2026-02-19T14:30:00.000000"
}
```

| Field | Description |
|-------|-------------|
| `url` | The base URL of the WordPress site |
| `cms` | Detected CMS (WordPress, Manual, etc.) |
| `vectors` | List of confirmed DDoS vectors — always contains both `pingback.ping` and `system.multicall` for auto-discovered sites |
| `xmlrpc_url` | Full URL to the XML-RPC endpoint |
| `added` | ISO timestamp of when the zombie was first discovered |
| `last_seen` | ISO timestamp of the most recent scan that confirmed the zombie |

If you scan the same site again, the existing entry is updated (vectors are merged, `last_seen` is refreshed) rather than creating a duplicate.

### Web Map Dashboard

Press `W` from the main menu to launch the **Botnet Web Map Dashboard**. This locally hosted interface allows you to visualize your zombie database on an interactive Leaflet world map. 
When launched, ARGUS automatically resolves the IP of each zombie and geolocates it. It hosts the dashboard utilizing a built-in Python HTTP server on port 8080 and opens it in your default browser. Features include:
- Interactive world map using dark tile layers
- Red markers pinpointing the physical locations of your collected bots
- Clicking a bot shows a popup with its URL, IP, CMS, vectors, and geographical data.

---

## API Backend

The `api/` folder contains the backend that powers AI Search. It is a FastAPI application deployed on Vercel that uses Groq (LLM inference) to match natural language queries against the full ARGUS tool catalog.

### Structure

```
api/
├── main.py              # FastAPI app with /search and /tools endpoints
├── tools_catalog.py     # Static catalog of all 82 tools with descriptions
├── requirements.txt     # Python dependencies (fastapi, groq, uvicorn)
├── vercel.json          # Vercel deployment configuration
└── .env.example         # Template for the GROQ_API_KEY environment variable
```

### Endpoints

| Endpoint | Method | Description |
|----------|--------|-------------|
| `/search?q=...` | GET | Takes a natural language query, sends it to Groq (Llama 3.3 70B), and returns up to 3 matching tools with relevance explanations |
| `/tools` | GET | Returns the full catalog of all 82 tools |

### Self-hosting

If you want to host the API yourself:

```bash
cd api
pip install -r requirements.txt
export GROQ_API_KEY=gsk_your_key_here
uvicorn main:app --reload
```

Then set the `API_URL` environment variable before running ARGUS:

```bash
export API_URL=http://localhost:8000
python3 argus.py
```

By default, ARGUS connects to the hosted instance at `https://argusbackend-psi.vercel.app`.

---

## Stealth Mode

ARGUS includes a hardened **Stealth Mode** that anonymizes all network traffic generated by the tool. Access it by pressing `S` from the main menu.

> **Important:** Stealth Mode protects traffic made by ARGUS only. It does not affect your browser, system DNS, or other applications. For full system anonymity, use a system-wide VPN or configure your browser to use the Tor SOCKS proxy at `127.0.0.1:9050`.

### Protection Layers

| Layer | What it does | How it works |
|-------|-------------|--------------|
| **Proxy routing** | Routes all HTTP/HTTPS requests and TCP connections through Tor, SOCKS5, or HTTP proxy | Monkey-patches `requests` and `socket.socket` at runtime. Every tool benefits automatically without per-tool configuration. |
| **IPv6 leak blocking** | Prevents IPv6 traffic from bypassing the proxy | Forces `AF_INET` (IPv4) on all sockets and `getaddrinfo` calls. Tor and most SOCKS proxies do not support IPv6, so any IPv6 connection would leak your real address. |
| **DNS leak prevention** | Blocks local DNS resolution that would expose your IP to DNS servers | `socket.gethostbyname` and `socket.getaddrinfo` are patched to **block** (not just warn) hostname resolution when stealth is active. Proxied connections resolve DNS remotely through the SOCKS proxy (`socks5h://` with remote DNS). |
| **DNS resolver TCP forcing** | Forces `dnspython` queries through the proxy | When stealth is active, `dns.resolver.Resolver.resolve()` is forced to use TCP instead of UDP. TCP connections go through the SOCKS proxy; UDP cannot be proxied and would leak your IP. |
| **HTTP fingerprint randomization** | Prevents server-side browser fingerprinting | Every request gets a randomized set of headers: `User-Agent` (15+ realistic browsers), `Accept-Language` (10 locales), `Accept`, `Accept-Encoding`, `Sec-Fetch-*`, `DNT`, and `Upgrade-Insecure-Requests`. |
| **MAC address spoofing** | Hides your hardware identifier on the local network | Generates a random locally-administered MAC and applies it to the active interface via `ip link`. The original MAC is saved and restored when stealth is disabled. |
| **Tor circuit rotation** | Prevents correlation between operations | Sends `SIGNAL NEWNYM` to Tor's ControlPort (9051) to request a fresh circuit with a new exit IP. |

### Kill-Switch

Stealth Mode includes a **kill-switch** that prevents any connection from leaking your real IP:

- Before every HTTP request, ARGUS verifies the proxy is reachable (cached check every 10 seconds). If the proxy is down, the request is **blocked** with a `ConnectionError` instead of falling through to a direct connection.
- At the socket level, `_SmartSocksSocket` never falls back to a direct TCP connection. If the SOCKS proxy fails, the exception propagates up and the connection is refused.
- If PySocks is not installed and a SOCKS/Tor proxy is configured, all requests are blocked with a clear error message.
- On stealth activation, ARGUS automatically verifies your identity by checking the external IP via `api.ipify.org`. If verification fails, it offers to disable stealth to prevent accidental exposure.

### Stealth Menu Options

| Option | Description |
|--------|-------------|
| 1 | Enable via **Tor** (auto-detects or starts Tor on `127.0.0.1:9050`) |
| 2 | Enable via a **custom SOCKS5 proxy** |
| 3 | Enable via a **custom HTTP proxy** |
| 4 | **Disable** Stealth Mode (also restores original MAC if spoofed) |
| 5 | **Test connection** via Tor Project API (confirms Tor routing) |
| 6 | **Show current external IP** (via ipify.org) |
| 7 | **Spoof MAC address** (randomizes MAC on active interface, requires sudo) |
| 8 | **Restore original MAC** |
| 9 | **New Tor identity** (rotates circuit, shows new exit IP. Requires ControlPort 9051) |
| 0 | Back to main menu |

### Supported Proxy Types

| Type | URI format | Notes |
|------|-----------|-------|
| **Tor** | `socks5h://127.0.0.1:9050` | Requires a running Tor service. ARGUS will attempt to auto-start it via `systemctl` if not running. |
| **SOCKS5** | `socks5h://host:port` | Any SOCKS5 proxy. The `h` suffix forces remote DNS resolution. |
| **HTTP** | `http://host:port` | Any HTTP proxy. Socket-level proxying uses HTTP CONNECT. |

### Known Limitations

These are inherent limitations of the proxy/Tor architecture and cannot be fully resolved in software:

| Limitation | Explanation |
|-----------|-------------|
| **RAW/UDP sockets bypass the proxy** | Tools that use `SOCK_RAW` or `SOCK_DGRAM` (Traceroute, Ping Sweep, UDP Flood, ICMP Flood, DNS Flood) cannot be routed through SOCKS. ARGUS displays a warning and requires explicit consent before running these tools in stealth mode. |
| **Your ISP sees Tor usage** | Your ISP can observe that you are connecting to the Tor network (but not what you are doing). To hide Tor usage from your ISP, use a Tor bridge with pluggable transports. |
| **Tor exit node sees unencrypted traffic** | If a tool makes plain HTTP (not HTTPS) requests, the Tor exit node can observe the content. Most ARGUS tools use HTTPS. |
| **Timing correlation** | An adversary monitoring both your entry and exit traffic could theoretically correlate requests by timing. Circuit rotation (option 9) mitigates this. |
| **Stealth Mode scope** | Only ARGUS traffic is anonymized. Your browser, system DNS, and other applications are not affected. |

---

## Tools

### OSINT and Reconnaissance

41 tools for gathering open-source intelligence and mapping attack surfaces.

| # | Tool | Description |
|---|------|-------------|
| 1 | Username Search | Searches for a username across 22+ social platforms and websites to find existing accounts. |
| 2 | Email Lookup | Queries public information associated with an email address, including Gravatar and MX records. |
| 3 | Phone Number Lookup | Validates and analyzes a phone number using Google's libphonenumber: country, carrier, line type (mobile/fixed/VoIP), timezone, and international/national/E.164 formatting. Falls back to prefix-based analysis (100+ countries) if the library is not installed. |
| 4 | IP Address Lookup | Geolocates an IP address and returns ISP, organization, AS number, and approximate coordinates. |
| 5 | WHOIS Lookup | Performs a WHOIS query on a domain to retrieve registrar, creation/expiration dates, name servers, and registrant details. |
| 6 | DNS Lookup | Resolves DNS records (A, AAAA, MX, NS, TXT, CNAME) for a given domain. |
| 7 | Subdomain Enumeration | Discovers subdomains via certificate transparency logs (crt.sh). |
| 8 | HTTP Headers Analysis | Fetches and displays HTTP response headers, highlighting security-relevant headers (HSTS, CSP, X-Frame-Options). |
| 9 | Website Technology Detection | Fingerprints the technology stack of a website (CMS, frameworks, server software, JavaScript libraries). |
| 10 | Port Scanner | Scans a host for open TCP ports on 16 common services with multi-threaded execution. |
| 11 | Reverse DNS Lookup | Resolves an IP address back to its associated hostname (PTR record). |
| 12 | MAC Address Lookup | Identifies the manufacturer/vendor associated with a given MAC address using the IEEE OUI database. |
| 13 | Email Breach Check | Checks whether an email address has appeared in known data breaches via Have I Been Pwned. |
| 14 | Metadata Extractor | Extracts EXIF metadata from images (GPS coordinates, camera model, timestamps). |
| 15 | Social Media Scraper | Collects publicly available profile information from GitHub and Reddit. |
| 16 | SSL/TLS Certificate Info | Retrieves and displays details of a domain's SSL/TLS certificate (issuer, validity, SANs, serial). |
| 17 | Wayback Machine Lookup | Queries the Internet Archive's Wayback Machine for historical snapshots of a URL. |
| 18 | Robots.txt and Sitemap Analyzer | Fetches and parses a website's robots.txt and sitemap.xml to reveal structure and access rules. |
| 19 | Link Extractor | Crawls a webpage and extracts all internal and external hyperlinks. |
| 20 | Google Dorks Generator | Generates 25 targeted Google search queries (dorks) to find exposed files, login pages, and sensitive data. |
| 21 | Traceroute | Traces the network route to a target host using ICMP/UDP with TTL increments. |
| 22 | Hash Identifier and Lookup | Identifies the type of a hash (MD5, SHA1, SHA256, etc.) and attempts to crack it via online rainbow tables. |
| 23 | ASN Lookup | Retrieves Autonomous System Number information for an IP or domain via BGPView. |
| 24 | Website Screenshot | Captures a screenshot of a webpage using a headless rendering service. |
| 25 | Reverse Image Search | Generates reverse image search URLs for Google, Bing, and TinEye. |
| 26 | CVE Search | Searches the MITRE CVE and NIST NVD databases for known vulnerabilities. |
| 27 | Paste / Code Search | Generates search links for GitHub, GitLab, Pastebin, and Stack Overflow. |
| 28 | DNS Zone Transfer Check | Tests whether a domain's name servers are vulnerable to unauthorized DNS zone transfers (AXFR). |
| 29 | SSL/TLS Suite Scanner | Tests TLS 1.2/1.3 support and enumerates cipher suites. |
| 30 | Shodan Host Lookup | Queries the Shodan InternetDB API for open ports, CPEs, and known vulnerabilities. |
| 31 | Favicon Hash Lookup | Downloads a site's favicon, computes its MurmurHash3 fingerprint, and generates a Shodan search query. |
| 32 | DMARC / SPF / DKIM Check | Queries DNS TXT records for SPF, DMARC, and DKIM (17 common selectors) to assess email security. |
| 33 | Security.txt Checker | Fetches and parses /.well-known/security.txt for vulnerability disclosure policy. |
| 34 | HTTP Methods Discovery | Probes a target with all HTTP methods (GET, POST, PUT, DELETE, PATCH, HEAD, OPTIONS, TRACE, CONNECT) and flags dangerous ones. |
| 35 | Cloud Storage Finder | Tests 16 naming mutations across AWS S3, Azure Blob, GCP Storage, and DigitalOcean Spaces for exposed buckets. |
| 36 | JS Endpoint Extractor | Fetches JavaScript files from a page and extracts API endpoints, AWS keys, tokens, emails, and IPs via regex. |
| 37 | WAF / CDN Detector | Detects 12 WAF/CDN vendors (Cloudflare, Akamai, AWS WAF, Sucuri, Imperva, etc.) from headers, cookies, and response bodies. |
| 38 | Banner Grabbing | Connects to specified ports and retrieves service banners (SSH, FTP, SMTP, HTTP, MySQL, Redis, etc.). |
| 39 | Subdomain Bruteforce | DNS brute-forces ~130 common subdomain names with multi-threaded resolution. Supports custom wordlists. |
| 40 | Ping Sweep / Host Discovery | Scans a CIDR range or IP range for live hosts via TCP connect on ports 80, 443, and 22. |
| 41 | Vibe-Coded Site Finder | Given a project or app name, checks for its existence across 25+ vibe-coding hosting platforms (Vercel, Netlify, Lovable, Replit, Render, Railway, Firebase, Cloudflare Pages, HuggingFace Spaces, Streamlit, Heroku, Glitch, Framer, Webflow, and more). Normalizes the input and scans all platforms in parallel. |

### Exploitation Testing

21 tools for vulnerability assessment. All require authorization confirmation before use.

| # | Tool | Description |
|---|------|-------------|
| 42 | SQL Injection Tester | Tests URL parameters with 20 SQL injection payloads (union, blind, time-based, error-based). |
| 43 | XSS Scanner (Reflected) | Scans URL parameters with 18 XSS payload vectors including event handlers and encoding bypasses. |
| 44 | Directory / File Bruteforcer | Discovers hidden directories and files on a web server using a 67-entry wordlist with multi-threading. |
| 45 | CORS Misconfiguration Scanner | Checks whether a target's CORS policy allows unauthorized cross-origin requests. |
| 46 | Open Redirect Scanner | Tests URL parameters with 15 open redirect payloads including protocol and hostname confusion tricks. |
| 47 | LFI / Path Traversal Tester | Tests 20 LFI payloads with 6 file signature detections (path traversal, PHP wrappers, log injection). |
| 48 | Subdomain Takeover Check | Checks whether subdomains point to unclaimed external services and are vulnerable to takeover. |
| 49 | Reverse Shell Generator | Generates reverse shell one-liners in 11 languages (Bash, Python, Perl, PHP, Ruby, PowerShell, Java, Netcat, socat, Lua, xterm). |
| 50 | CMS Vulnerability Scanner | Scans for known vulnerabilities in WordPress, Joomla, and Drupal installations. For WordPress, performs deep XML-RPC analysis: tests `system.multicall` brute-force amplification, `pingback.ping` SSRF, and username oracle attacks. **If both `system.multicall` and `pingback.ping` are confirmed active, the site is automatically saved to the Botnet zombie database for multicall amplification.** |
| 51 | Payload Encoder / Decoder | Encodes and decodes payloads in 11 modes (URL, Base64, Hex, HTML entities, Unicode, double URL, MD5/SHA hashing). |
| 52 | CRLF Injection Tester | Tests 10 CRLF payloads for header injection and HTTP response splitting. |
| 53 | SSRF Tester | Tests 20 SSRF payloads targeting localhost, cloud metadata endpoints (AWS/GCP/Azure), and internal services. |
| 54 | JWT Analyzer | Decodes JWT headers and payloads, checks expiry, analyzes algorithm security, and brute-forces common HMAC secrets. |
| 55 | Clickjacking Tester | Checks X-Frame-Options and CSP frame-ancestors, generates proof-of-concept HTML if vulnerable. |
| 56 | XXE Tester | Tests 6 XML External Entity payloads (file read, SSRF, PHP wrappers) against XML-accepting endpoints. |
| 57 | Command Injection Tester | Tests 20 OS command injection payloads with time-based and output-based detection. |
| 58 | Host Header Injection | Tests 10 host header manipulation vectors (X-Forwarded-Host, Forwarded, X-Original-URL, etc.). |
| 59 | Insecure Cookie Checker | Analyzes all Set-Cookie headers for missing Secure, HttpOnly, and SameSite flags. |
| 60 | CSRF Token Analyzer | Scans HTML forms for CSRF token presence and quality, checks meta tags and CORS headers. |
| 61 | Prototype Pollution Scanner | Tests prototype pollution via query parameters and JSON body payloads. |
| 62 | Supabase RLS Auditor | Scans a website using Supabase for exposed project URLs and anon keys, then tests all discoverable tables for Row-Level Security (RLS) misconfigurations. |

### Stress Testing

10 tools for load and resilience testing. All require double authorization (confirmation + "I ACCEPT ALL RESPONSIBILITY").

| # | Tool | Description |
|---|------|-------------|
| 63 | HTTP Flood (GET/POST) | Sends a high volume of HTTP requests with random user-agents and X-Forwarded-For spoofing. Configurable threads (1-200) and duration (1-300s). |
| 64 | Slowloris | Holds concurrent connections open by sending partial HTTP headers, exhausting the server's connection pool. |
| 65 | Slow POST (R.U.D.Y.) | Sends HTTP POST requests with extremely slow body transmission to keep connections occupied. |
| 66 | TCP Connection Flood | Opens a large number of raw TCP connections to a target host and port. |
| 67 | UDP Flood | Sends a continuous stream of random UDP packets to a target host and port. |
| 68 | ICMP Ping Flood | Sends a high volume of ICMP echo request packets (requires root/admin privileges on some systems). |
| 69 | HTTP Slow Read | Sends legitimate HTTP requests but reads the response extremely slowly, tying up server resources. |
| 70 | GoldenEye (Keep-Alive Flood) | Floods with HTTP requests using persistent Keep-Alive connections and randomized headers. |
| 71 | DNS Flood | Floods a DNS server with queries for random subdomains. Configurable threads and duration. |
| 72 | WebSocket Flood | Opens multiple WebSocket connections and floods with masked frames. Configurable connections, duration, and message size. |

### Phishing Simulation

10 tools for authorized phishing simulations and red-team engagements. All require double authorization (confirmation + "I ACCEPT ALL RESPONSIBILITY").

| # | Tool | Description |
|---|------|-------------|
| 73 | Homoglyph Domain Generator | Generates lookalike domains using Unicode/Cyrillic homoglyphs, typo swaps, missing/doubled chars, and QWERTY adjacency. Optionally checks registration. |
| 74 | Phishing URL Analyzer | Scores a suspicious URL (0-100) by checking for IP usage, suspicious TLDs, brand impersonation, encoding, URL shorteners, and urgency keywords. |
| 75 | Email Spoofing Checker | Evaluates a domain's email spoofing resistance by checking SPF, DMARC, DKIM, and MTA-STS records. |
| 76 | Typosquatting Generator | Generates typosquatted domain variations via bit-flips, vowel swaps, dot insertion, prefix/suffix abuse, and hyphenation. Optionally checks registration. |
| 77 | Credential Harvester Template Generator | Generates 8 ready-to-use phishing page templates (Generic Login, Office 365, Google, VPN Portal, WiFi Captive Portal, Password Reset, 2FA, File Share) with configurable callback URL and company name. |
| 78 | URL Obfuscator | Obfuscates a URL using 10+ techniques: decimal/hex/octal IP, @ redirect, subdomain spoof, RTL Unicode override, URL credentials, fragment trick. |
| 79 | Email Header Analyzer | Analyzes raw email headers for phishing indicators: SPF/DKIM/DMARC results, From/Return-Path mismatch, Reply-To mismatch, suspicious mailers, and urgency tactics. Outputs a phishing score. |
| 80 | IDN Homograph Attack Generator | Generates internationalized domain names using Cyrillic character substitution with punycode output. Supports single, multi, and full-script replacement. |
| 81 | Phishing Kit Detector | Scans a suspicious URL for signatures of 11 known phishing kits (GoPhish, Evilginx2, King Phisher, SET, Modlishka, etc.) plus behavioral indicators. |
| 82 | Phishing Campaign Planner | Generates an intelligence report for a target domain: email security posture, mail infrastructure, web presence, ranked pretexts, timing recommendations, and evasion tips. |

---

## Authorization System

ARGUS enforces a three-tier authorization model based on tool category:

| Category | Tools | Authorization |
|----------|-------|---------------|
| OSINT / Reconnaissance | 1-41 | None required. Runs immediately. |
| Exploitation Testing | 42-62 | Single confirmation: you must confirm you have authorization to test the target. |
| Stress Testing | 63-72 | Double confirmation: confirm authorization **and** type `I ACCEPT ALL RESPONSIBILITY`. |
| Botnet Mode | B | Double confirmation: confirm authorization **and** type `I ACCEPT ALL RESPONSIBILITY`. |
| Phishing Simulation | 73-82 | Double confirmation: confirm authorization **and** type `I ACCEPT ALL RESPONSIBILITY`. |

To streamline the workflow, once you accept the disclaimer for a specific category (Exploitation, Stress, or Phishing), your consent is saved to an `accepted_responsibility.json` file in the project directory, bypassing future redundant prompts for that specific module category.

---

## Built-in Payloads and Wordlists

ARGUS ships with extensive built-in payload databases so no external wordlist files are needed:

- 20 SQL injection payloads (union, blind, time-based, error-based)
- 18 XSS payload vectors
- 67 common directories and files
- 15 open redirect payloads
- 20 LFI / path traversal payloads
- ~130 subdomain names for brute-forcing
- 10 CRLF injection payloads
- 20 SSRF payloads (localhost, cloud metadata, internal services)
- 6 XXE payloads
- 20 OS command injection payloads
- CMS-specific wordlists (WordPress plugins, themes, usernames, passwords)
- Homoglyph and IDN character mappings
- 11 phishing kit signature fingerprints
- 12 WAF/CDN detection signatures
- Service takeover fingerprint database
- 25 vibe-coding platform domains (Vercel, Netlify, Lovable, Replit, Render, Railway, etc.)

---

## Dependencies

All dependencies are listed in `requirements.txt`:

| Package | Purpose | Required |
|---------|---------|----------|
| requests | HTTP requests for all web-based tools | Yes |
| colorama | Colored terminal output | Yes |
| python-whois | WHOIS domain lookups | Optional |
| dnspython | DNS record resolution, zone transfers, DMARC/SPF/DKIM checks | Optional |
| beautifulsoup4 | HTML parsing for scraping, link extraction, tech detection, JS extraction, CSRF analysis | Optional |
| Pillow | Image processing and EXIF metadata extraction | Optional |
| PySocks | SOCKS proxy support for Stealth Mode (Tor / SOCKS5). **Required for full stealth protection.** | Optional |
| phonenumbers | Phone number validation, carrier/line type detection, formatting (Google libphonenumber) | Optional |

Install all at once with:

```bash
pip install -r requirements.txt
```

Tools with missing optional dependencies will display a warning and skip gracefully rather than crashing.

---

## License

This project is provided as-is for educational and authorized testing purposes only.
