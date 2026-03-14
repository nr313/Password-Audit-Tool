# PWDAUDIT — AI-Powered Password Audit Tool

A browser-based password security tool with three modes — single password analysis, bulk audit, and policy compliance checking — using Claude AI to score strength, identify attack vectors, and generate recommendations.

## Features

- **3 audit modes** — Single password, Bulk audit, Policy compliance
- **Real-time strength meter** — Live feedback as you type with 6 policy checks
- **AI threat analysis** — Attack vectors, estimated crack time, specific weaknesses
- **Bulk auditing** — Audit an entire password list at once with stats breakdown
- **Policy frameworks** — Check compliance against NIST SP 800-63B, PCI DSS, HIPAA, CIS Controls, ISO 27001
- **Zero dependencies** — Single HTML file, runs in any browser

## Modes

### Single Password
- Real-time strength bar and policy checklist
- AI scores 0–100 with grade (Critical / Weak / Moderate / Strong)
- Specific attack vectors that could crack this password
- Estimated crack time
- Targeted improvement recommendations

### Bulk Audit
- One password per line
- Stats breakdown: Critical / Weak / Moderate / Strong counts
- Per-password grade and issue summary
- Policy-level recommendations for the organization

### Policy Compliance
- Check against 5 major security frameworks
- Per-requirement pass/fail breakdown
- Specific remediation steps to achieve compliance

## Getting Started

### 1. Clone the repo
```bash
git clone https://github.com/YOUR_USERNAME/password-audit-tool.git
cd password-audit-tool
```

### 2. Get an Anthropic API key
Sign up at [console.anthropic.com](https://console.anthropic.com) and create a free API key.

### 3. Open in browser
```bash
open password-audit.html
```

### 4. Analyze passwords
1. Enter your API key
2. Select a mode (Single / Bulk / Policy)
3. Enter a password or click **Load sample**
4. Click **Analyze**

## Example Output

For `Summer2024!`:

```
Grade:       WEAK — Score: 45/100
Crack Time:  2-4 hours (dictionary attack)

Attack Vectors:
  Seasonal pattern attack  (Summer + year is extremely common)
  Dictionary + leet speak  (common substitution patterns)
  Credential stuffing      (pattern appears in breach databases)

Recommendations:
  → Add more random characters — avoid season/year patterns
  → Increase length to 16+ characters
  → Use a passphrase instead: 4 random words + symbols
  → Consider a password manager to generate truly random passwords
```

## Supported Policy Frameworks

| Framework | Focus |
|-----------|-------|
| NIST SP 800-63B | Length over complexity, no mandatory rotation |
| PCI DSS | Payment card industry — 7+ chars, complexity required |
| HIPAA | Healthcare — complexity + rotation requirements |
| CIS Controls | Center for Internet Security benchmarks |
| ISO 27001 | International information security standard |
| Corporate Standard | 12+ chars, upper/lower/number/symbol |

## Security Note

This tool is for **educational and security auditing purposes only**. Never enter real production credentials, user passwords, or sensitive authentication data. Passwords are sent directly to the Anthropic API and are not stored anywhere else.

## Technologies

- Vanilla HTML / CSS / JavaScript (zero dependencies)
- [Anthropic Claude API](https://docs.anthropic.com) — `claude-sonnet-4-20250514`
- Courier Prime + Epilogue fonts (Google Fonts)

## Learning Concepts

This project demonstrates practical knowledge of:
- Password security fundamentals and entropy
- Common attack vectors (dictionary, brute force, credential stuffing)
- Password policy frameworks (NIST, PCI DSS, HIPAA, ISO 27001)
- Compliance checking and gap analysis
- Security awareness — what makes passwords weak vs strong
- Organizational password policy assessment

## License

MIT
