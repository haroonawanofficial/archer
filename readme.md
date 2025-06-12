#  Archer

> **Archer: Server-aware, WAF-aware, lightning-fast XSS hunter—zero false noise.**

---

## Features
| Capability | Description |
|------------|-------------|
| **Server-Aware Scanning** | Dynamically adapts payloads to the target server stack. |
| **WAF-Aware Scanning** | Dynamically adapts payloads to the target WAF stack. |
| **Server-Side Intelligence** | Detects web-server type and tunes obfuscation chains automatically. |
| **False-Noise Filtering** | Built-in fingerprints for common error strings eliminate false positives. |
| **Parallel Recon** | Multi-threaded crawler + scanner hits thousands of URLs per minute. |
| **Autonomous Mode** | “Fire-and-forget” CLI flags for full gather-→-scan-→-report pipeline. |
| **Rich Reporting** | Generates HTML, CSV, Excel & JSON reports out-of-the-box. |

---

## Installation

```bash
git clone https://github.com/haroonawanofficial/archer.git
cd archer
python3 -m pip install -r requirements.txt
```

- Crawl a domain, then scan top 100 links with adaptive payloads
python archer.py --domain example.com --test-links 100 --adaptive --report report.html


- Use an existing URL list, skip duplicate tests after 5 hits, and restrict filters to the top 25 obfuscation chains
python archer.py --list urls.txt --skip-duplicate 5 --use-filters 25 --thread 100 --report report.html


- Released under the MIT License – see LICENSE for details.
> Made with ❤️ by Haroon
