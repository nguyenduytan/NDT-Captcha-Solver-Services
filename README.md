<div align="center">

<h1>🧩 NDT Captcha Solver Services</h1>
<p><a href="LICENSE"><img alt="MIT license" src="https://img.shields.io/badge/License-MIT-64748b?style=flat-square"></a> <img alt="Pricing review date" src="https://img.shields.io/badge/Price_review-2026--10--27-2563eb?style=flat-square"></p>


**CAPTCHA solver APIs, AI services, human-in-the-loop providers, scoring tools and defensive CAPTCHA resources.**

[![Language](https://img.shields.io/badge/language-English-d97706?style=for-the-badge)](README.md) [![Tiếng Việt](https://img.shields.io/badge/README-Ti%E1%BA%BFng%20Vi%E1%BB%87t-16a34a?style=for-the-badge)](README.vi.md) [![Direct links](https://img.shields.io/badge/links-direct%20%7C%20no%20affiliate-16a34a?style=for-the-badge)](#methodology)

**[Comparison](#solver-comparison) · [By challenge](#choose-by-challenge) · [Scoring](#detection-and-scoring) · [Defensive CAPTCHA](#if-you-are-building-a-captcha)**

</div>

> [!IMPORTANT]
> Use solver services only for authorized QA, accessibility, internal testing and lawful automation. Do not use them to bypass authentication, create fake accounts or defeat security controls.

## Quick picks

| Need | Start with | Why |
|---|---|---|
| Low-cost OCR/image | [10Captcha](https://10captcha.com/), [AZcaptcha](https://azcaptcha.com/), [SolveCaptcha](https://solvecaptcha.com/) | Low public per-1K rates and simple APIs |
| Broad challenge coverage | [2Captcha](https://2captcha.com/), [Anti-Captcha](https://anti-captcha.com/), [CapSolver](https://www.capsolver.com/) | Large catalogs and integrations |
| AI subscription | [CaptchaAI](https://captchaai.com/), [NopeCHA](https://nopecha.com/pricing) | Thread/day/month plans |
| Build a defense | [reCAPTCHA](https://www.google.com/recaptcha/about/), [Turnstile](https://www.cloudflare.com/products/turnstile/), [hCaptcha](https://www.hcaptcha.com/) | Defensive products and test environments |

<a id="solver-comparison"></a>
## Solver comparison

Prices remain in the provider's own unit. Image recognition, tokens, successful solves, threads and monthly subscriptions are not interchangeable.

| Service | Model | Public price example | Coverage / integration | Buying read |
|---|---|---:|---|---|
| [10Captcha](https://10captcha.com/) | AI, pay per solve | Image $0.10/1K; v2 $0.25; v3 $0.30 | REST API and 300+ integrations | Low public price for listed types; FunCaptcha/GeeTest shown as coming soon |
| [AZcaptcha](https://azcaptcha.com/pricing) | Automated API | Image $0.40; v2 $1; Turnstile $1.20 | REST, webhooks, Python/PHP/Node | Charges successful solves; $5 minimum top-up |
| [SolveCaptcha](https://solvecaptcha.com/) | Automated | Image $0.35; v2 $0.55; Turnstile $0.80 | API, extension, Selenium, Puppeteer | Measure acceptance and speed in your own flow |
| [CapSolver](https://docs.capsolver.com/en/pricing/) | AI/automated | v2 $0.80; v3 $1; Turnstile $1.20; image $0.40 | API, SDKs, extension, Playwright, MCP | Confirm exact task type and dashboard price |
| [CapMonster Cloud](https://capmonster.cloud/en/) | AI | v2 $0.60/1K tokens; Turnstile $1.30; text $0.30/1K; classification $0.04/1K images | JSON API, C#, Python, JS, Go, PHP | Image classification is not a full token solve |
| [Anti-Captcha](https://anti-captcha.com/) | Workforce/API | Image $0.50–0.70; v2 $0.95–2; Turnstile $2 | API and many languages | Established coverage; load affects price and latency |
| [2Captcha](https://2captcha.com/pricing) | Human workforce + API | Image £0.45–0.89; v2 £0.80–2.45; Arkose £1.20–41 | SDKs, browser automation and broad catalog | Prices are shown in GBP on the reviewed page; do not compare directly with USD |
| [CaptchaAI](https://captchaai.com/) | AI subscription | $15/month/5 threads; $30/15; $90/50 | API, Chrome extension | Subscription can win at sustained volume; thread count is the limit |
| [NopeCHA](https://nopecha.com/pricing) | AI subscription | $4.99/month/2,000 solves/day; $19.99/20,000 | Chrome/Firefox, Python, JS | Compare daily cap and concurrency |
| [EZCaptcha](https://www.ez-captcha.com/) | AI | v2 $0.60; Turnstile $1; hCaptcha $3 | API and developer plan | Verify current task list and billing |
| [EndCaptcha](https://endcaptcha.com/) | Workforce | Live pricing; advertises 7-second SLA | API and extension | Consider predictable latency over lowest price |
| [Death By Captcha](https://deathbycaptcha.com/) | Workforce/automated | Live dashboard pricing | API and libraries | Obtain a current quote for the exact task |

### Pricing conditions and limitations

- CapSolver's dedicated pricing page is used because its documentation homepage shows different prices. Confirm the dashboard rate before topping up.
- 2Captcha values remain in GBP; no currency conversion is implied.
- CapMonster's $0.04 image classification rate differs from $0.60 for a complete v2 token; text CAPTCHA is $0.30/1K.
- Speed and success figures advertised by vendors are not independent measurements.

### Additional services awaiting verification

| Service | Direct link | Review status |
|---|---|---|
| BestCaptchaSolver | [Website](https://bestcaptchasolver.com/) | Website opened; per-challenge pricing not finalized |
| CapGuru | [Website](https://cap.guru/en/) | Page access blocked; do not reuse historical prices |
| HardCaptcha | [Website](https://hardcaptcha.com/) | Page unavailable during review; current status unverified |
| MetaBypass | [Website](https://metabypass.tech/) | Unexpected redirect during review; not shortlisted |
| CapCat | [Website](https://capcat.one/) | Research candidate; pricing/features unverified |
| Captcha.run | [Website](https://captcha.run/) | Research candidate; pricing/features unverified |

This directory covers the services reviewed, not the entire market. A failed page request does not establish that a business has closed.

<a id="choose-by-challenge"></a>
## Choose by challenge

| Challenge | Candidates | Main variables |
|---|---|---|
| Image/text OCR | 10Captcha, CapMonster, AZcaptcha, SolveCaptcha | Image quality, language, distortion, retries |
| reCAPTCHA v2 | CapSolver, SolveCaptcha, Anti-Captcha, 2Captcha | Site key, proxy/geo and browser context |
| reCAPTCHA v3 | CapSolver, EZCaptcha, 2Captcha, CaptchaAI | Score, action, IP reputation and browser |
| Enterprise | CapSolver, AZcaptcha, Anti-Captcha, 2Captcha | Task type and same session context |
| Turnstile | CapSolver, AZcaptcha, SolveCaptcha, Anti-Captcha | Managed/non-interactive mode and proxy |
| Arkose/FunCaptcha | EZCaptcha, Anti-Captcha, 2Captcha | Large price variation; test only authorized cases |
| GeeTest | CapSolver, Anti-Captcha, 2Captcha | Version, mode and locale |
| Amazon WAF | CapSolver, Anti-Captcha, AZcaptcha | WAF variant and browser context |
| hCaptcha | EZCaptcha and providers with current docs | Enterprise/standard mode and reputation |
| ALTCHA | Anti-Captcha, AZcaptcha, 2Captcha | Widget version and proof-of-work |

## Cost analysis

```text
cost per 1,000 accepted workflows
= (solver + proxy + compute + retry cost) / accepted workflows × 1,000
```

Per-solve APIs suit irregular volume. Subscriptions only win when the included threads or daily capacity are actually used. Human services may handle unusual tasks but have queue and quality variability. AI services can be fast and cheap for common tasks while failing on a particular version.

Example: 100,000 v2 tokens at $0.60/1K costs $60. If only 80,000 workflows are accepted, solver cost is $0.75 per 1K accepted workflows before proxy and compute costs. This is a calculation example, not a benchmark.

The nominal break-even point between CaptchaAI at $15/month and an API at $0.60/1K is 25,000 tasks/month, only if task type, acceptance and throughput are comparable. NopeCHA's daily allowance cannot be pooled into a single day's run.

Proxyless tasks are not always appropriate when an application binds a challenge to an IP/session. Check whether failures are billable and how refund requests work.

## Detection and scoring

- [Cloudflare Turnstile demo](https://nowsecure.nl/)
- [Google reCAPTCHA v3 demo](https://recaptcha-demo.appspot.com/recaptcha-v3-request-scores.php)
- [AntCPT score detector](https://antcpt.com/score_detector/)
- [2Captcha demos](https://2captcha.com/demo)
- [BrowserLeaks](https://browserleaks.com/), [CreepJS](https://abrahamjuliot.github.io/creepjs/), [Fingerprint Playground](https://demo.fingerprint.com/playground)

For authorized QA, record challenge type, browser/version, proxy country/ASN, solve time, callback, server verification, acceptance and cost. A returned token is not proof that the end-to-end workflow succeeded.

### QA for applications you own

Prefer official test keys or sandbox modes for reproducible integration tests. Cover challenge creation, callback, server-side verification, expiry and invalid-token rejection. See [Turnstile testing](https://developers.cloudflare.com/turnstile/troubleshooting/testing/), [reCAPTCHA docs](https://developers.google.com/recaptcha) and [hCaptcha docs](https://docs.hcaptcha.com/). Never publish API keys, cookies or user data in benchmark logs.

<a id="if-you-are-building-a-captcha"></a>
## If you are building a CAPTCHA

| Product | Position | Evaluation |
|---|---|---|
| [Google reCAPTCHA](https://www.google.com/recaptcha/about/) | Broad ecosystem | Integration, privacy and score behavior |
| [Cloudflare Turnstile](https://www.cloudflare.com/products/turnstile/) | Low-friction managed challenge | Widget model and Cloudflare integration |
| [hCaptcha](https://www.hcaptcha.com/) | Managed bot/fraud controls | Pro, enterprise and accessibility |
| [Friendly Captcha](https://friendlycaptcha.com/) | Proof-of-work | Reduces image puzzles |
| [ALTCHA](https://altcha.org/) | Open-source/self-hosted | Useful for self-host and privacy-sensitive apps |
| [Private Captcha](https://github.com/PrivateCaptcha/PrivateCaptcha) | Open-source | Self-hosted proof-of-work |
| [Arkose Labs](https://www.arkoselabs.com/) | Risk-based enterprise | Fraud and abuse prevention |

## Libraries and documentation

- [2Captcha SDKs](https://github.com/2captcha), [CapSolver docs](https://docs.capsolver.com/en/), [CapMonster docs](https://docs.capmonster.cloud/)
- [reCAPTCHA docs](https://developers.google.com/recaptcha), [Turnstile docs](https://developers.cloudflare.com/turnstile/), [hCaptcha docs](https://docs.hcaptcha.com/)
- [Friendly Captcha integrations](https://friendlycaptcha.com/integrations/), [ALTCHA docs](https://altcha.org/docs/), [PrivateCaptcha](https://github.com/PrivateCaptcha/PrivateCaptcha)
- [svg-captcha](https://github.com/produck/svg-captcha), [Captcha for Laravel](https://github.com/mewebstudio/captcha), [Gregwar Captcha](https://github.com/Gregwar/Captcha)

<a id="methodology"></a>
## Notes and contributions

Prices were checked on 2026-10-27 and are not quotes. Provider links are direct and contain no affiliate parameters. Vendor uptime and success claims are not independent benchmarks. See [CONTRIBUTING.md](CONTRIBUTING.md).

## Related NDT projects

- [NDT Proxy Scraper](https://github.com/nguyenduytan/NDT-Proxy-Scraper)
- [NDT Proxy Providers List](https://github.com/nguyenduytan/NDT-Proxy-Providers-List)
- [NDT Antidetect Tools](https://github.com/nguyenduytan/NDT-Antidetect-Tools)

> [!WARNING]
> Use these services only for lawful, authorized QA, accessibility, fraud-prevention testing and internal automation.
