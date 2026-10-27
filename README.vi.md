<div align="center">

<h1>🧩 NDT Captcha Solver Services</h1>

**So sánh API giải CAPTCHA, AI solver, human-in-the-loop, công cụ scoring và thư viện defensive CAPTCHA.**

[![Pricing research date](https://img.shields.io/badge/Price_review-27%20Oct%202026-d97706?style=for-the-badge)](https://github.com/nguyenduytan)
[![Direct links](https://img.shields.io/badge/links-direct%20%7C%20no%20affiliate-16a34a?style=for-the-badge)](#methodology)
[![License](https://img.shields.io/badge/license-MIT-64748b?style=for-the-badge)](LICENSE)

**[So sánh dịch vụ](#solver-comparison) · [Theo loại CAPTCHA](#choose-by-challenge) · [Điểm số](#detection-and-scoring) · [Xây dựng CAPTCHA](#if-you-are-building-a-captcha)**

<p align="center"><a href="README.md">English</a> · <strong>Tiếng Việt</strong></p>

</div>

> [!IMPORTANT]
> Chỉ dùng dịch vụ cho QA, accessibility, internal testing và automation hợp pháp. Không dùng để bypass đăng nhập, tạo account giả, gian lận hoặc truy cập hệ thống không được phép.

<a id="quick-picks"></a>
## Chọn nhanh

| Nhu cầu | Shortlist | Vì sao |
|---|---|---|
| OCR/image giá thấp | [10Captcha](https://10captcha.com/), [AZcaptcha](https://azcaptcha.com/), [SolveCaptcha](https://solvecaptcha.com/) | Giá per-1K thấp, API đơn giản |
| Coverage rộng | [2Captcha](https://2captcha.com/), [Anti-Captcha](https://anti-captcha.com/), [CapSolver](https://www.capsolver.com/) | Nhiều loại challenge và integration |
| AI subscription | [CaptchaAI](https://captchaai.com/), [NopeCHA](https://nopecha.com/pricing) | Tính theo thread/ngày/tháng |
| Defensive CAPTCHA | [reCAPTCHA](https://www.google.com/recaptcha/about/), [Turnstile](https://www.cloudflare.com/products/turnstile/), [hCaptcha](https://www.hcaptcha.com/) | Dùng để bảo vệ ứng dụng và test integration |

<a id="solver-comparison"></a>
## So sánh dịch vụ giải CAPTCHA

Giá ghi theo **1,000 successful solves/tokens** nếu provider dùng đơn vị này. Subscription, thread và image không được quy đổi giả thành per-1K.

| Service | Model | Giá công khai mẫu | Coverage / integration | Phân tích |
|---|---|---:|---|---|
| [10Captcha](https://10captcha.com/) | AI, pay per solve | Image $0.10/1K; v2 $0.25; v3 $0.30 | REST API, 300+ integrations | Mức giá công bố thấp trong bảng; FunCaptcha/GeeTest còn ghi coming soon |
| [AZcaptcha](https://azcaptcha.com/pricing) | Automated API | Image $0.40; v2 $1; Turnstile $1.20 | REST, webhook, Python/PHP/Node | Chỉ charge successful solve; minimum top-up $5 |
| [SolveCaptcha](https://solvecaptcha.com/) | Automated | Image $0.35; v2 $0.55; Turnstile $0.80 | API, extension, Selenium, Puppeteer | Giá công bố thấp; tốc độ và acceptance cần đo thực tế |
| [CapSolver](https://docs.capsolver.com/en/pricing/) | AI/automated | v2 $0.80; v3 $1; Turnstile $1.20; image $0.40 | API, SDK, extension, Playwright, MCP | Có SDK/integration; kiểm tra đúng task type và giá dashboard |
| [CapMonster Cloud](https://capmonster.cloud/en/) | AI | v2 $0.60/1K tokens; Turnstile $1.30; text $0.30/1K; reCAPTCHA classification $0.04/1K images | JSON API, C#, Python, JS, Go, PHP | Classification ảnh reCAPTCHA không phải OCR hoặc token hoàn chỉnh |
| [Anti-Captcha](https://anti-captcha.com/) | Workforce/API | Image $0.50–0.70; v2 $0.95–2; Turnstile $2 | API, plugin, nhiều ngôn ngữ | Dịch vụ lâu năm, coverage rộng; giá phụ thuộc tải |
| [2Captcha](https://2captcha.com/pricing) | Human workforce + API | Image £0.45–0.89; v2 £0.80–2.45; Arkose £1.20–41 | SDK, browser automation, nhiều challenge | Có danh mục challenge rộng; Arkose rất biến động giá |
| [CaptchaAI](https://captchaai.com/) | AI subscription | $15/tháng/5 threads; $30/15; $90/50 | API, Chrome extension, image catalog | Hợp volume đều; giới hạn chính là thread |
| [NopeCHA](https://nopecha.com/pricing) | AI subscription | $4.99/tháng/2,000 solves/ngày; $19.99/20,000 | Chrome/Firefox, Python, JS | Tốt cho browser testing; so daily cap và concurrency |
| [EZCaptcha](https://www.ez-captcha.com/) | AI | v2 $0.60; Turnstile $1; hCaptcha $3 | API, developer plan | Nhiều task; revenue share developer không phải giá khách hàng |
| [EndCaptcha](https://endcaptcha.com/) | Workforce | Giá live; quảng cáo SLA 7 giây | API, extension, quality/outage insurance | Hợp nơi latency predictable quan trọng hơn giá thấp |
| [Death By Captcha](https://deathbycaptcha.com/) | Workforce/automated | Giá live qua dashboard | API và libraries lâu năm | Lấy quote mới theo task trước khi benchmark |

### Điều kiện giá và giới hạn

- CapSolver: bảng giá chuyên biệt được ưu tiên hơn homepage docs vì hai trang hiển thị giá khác nhau. Kiểm tra dashboard trước nạp.
- 2Captcha: nguồn đọc được đang hiển thị **GBP (£)**. Bảng giữ nguyên tiền tệ; không so trực tiếp con số này với USD và không tự quy đổi.
- CapMonster: $0.04 cho nhận diện ảnh reCAPTCHA khác $0.60 cho token v2 đầy đủ; text CAPTCHA là $0.30/1K.
- Các thông số tốc độ/success trên website là vendor claims; bảng không xếp hạng chất lượng khi chưa benchmark.

### Danh bạ mở rộng và mục chưa xác minh

| Service | Link trực tiếp | Trạng thái nghiên cứu |
|---|---|---|
| BestCaptchaSolver | [Website](https://bestcaptchasolver.com/) | Đã mở website; chưa chốt bảng giá từng challenge |
| CapGuru | [Website](https://cap.guru/en/) | Nguồn bị chặn truy cập; không dùng giá cũ |
| HardCaptcha | [Website](https://hardcaptcha.com/) | Không đọc được nguồn; chưa xác minh tình trạng |
| MetaBypass | [Website](https://metabypass.tech/) | Lần đọc bị chuyển hướng bất thường; không đưa vào shortlist |
| CapCat | [Website](https://capcat.one/) | Ứng viên nghiên cứu; chưa xác minh giá/tính năng |
| Captcha.run | [Website](https://captcha.run/) | Ứng viên nghiên cứu; chưa xác minh giá/tính năng |

Danh sách bao phủ các dịch vụ được khảo sát, không khẳng định liệt kê toàn bộ thị trường. Lỗi đọc trang không tự chứng minh dịch vụ đã ngừng hoạt động.

<a id="choose-by-challenge"></a>
## Chọn theo loại CAPTCHA

| Challenge | Nên thử trước | Biến số chính |
|---|---|---|
| Image/text OCR | 10Captcha, CapMonster, AZcaptcha, SolveCaptcha | Chất lượng ảnh, ngôn ngữ, distortion, retry |
| reCAPTCHA v2 | CapSolver, SolveCaptcha, Anti-Captcha, 2Captcha | Site key, proxy/geo, browser context |
| reCAPTCHA v3 | CapSolver, EZCaptcha, 2Captcha, CaptchaAI | Score, action, IP reputation, browser |
| Enterprise | CapSolver, AZcaptcha, Anti-Captcha, 2Captcha | Task type và session cùng IP/browser |
| Turnstile | CapSolver, AZcaptcha, SolveCaptcha, Anti-Captcha | Managed/non-interactive, site key, proxy |
| Arkose/FunCaptcha | EZCaptcha, Anti-Captcha, 2Captcha | Giá biến động lớn; test case được phép |
| GeeTest | CapSolver, Anti-Captcha, 2Captcha | Version, challenge mode, locale |
| Amazon WAF | CapSolver, Anti-Captcha, AZcaptcha | WAF variant và browser context |
| hCaptcha | EZCaptcha; provider khác cần xác nhận docs hiện hành | Enterprise/standard, image task, reputation |
| ALTCHA | Anti-Captcha, AZcaptcha, 2Captcha | Widget version và proof-of-work |

<a id="cost-analysis"></a>
## Phân tích chi phí

```text
chi phí / 1.000 workflow hợp lệ
= (solver + proxy + compute + retry + phí bắt buộc) / workflow hợp lệ × 1.000
```

- **Per-solve API** phù hợp volume không đều và task đã biết.
- **Subscription** chỉ rẻ khi dùng đủ thread/daily capacity; unused plan là chi phí thật.
- **Human service** xử lý task lạ tốt hơn nhưng có queue, tốc độ và biến động chất lượng.
- **AI service** nhanh/rẻ ở task phổ biến nhưng có thể yếu ở một version cụ thể.
- **Proxyless** không luôn tốt: nếu app bind challenge vào IP/session, solver phải dùng cùng context được phép.
- Kiểm tra failed task có bị charge không; nhiều service chỉ refund theo policy hoặc support.

### Ví dụ tính giá và chọn subscription

Giả sử 100,000 token v2 đều bị tính phí: rate $0.60/1K cho hóa đơn $60. Nếu chỉ 80,000 workflow được ứng dụng chấp nhận, solver cost hiệu dụng là $0.75/1K workflow, chưa cộng proxy/compute. Đây là phép tính giả định, không phải số liệu đo.

CaptchaAI $15/tháng so với API $0.60/1K có điểm hòa vốn danh nghĩa 25,000 task/tháng, **chỉ khi** cùng loại task, tỷ lệ chấp nhận và năng lực xử lý đáp ứng. NopeCHA giới hạn theo ngày nên không được gộp quota 30 ngày để chạy hết trong một ngày. Không thể dùng giá nhận diện ảnh để tính token đầy đủ.

<a id="detection-and-scoring"></a>
## Kiểm tra phát hiện và điểm số

- [Cloudflare Turnstile demo](https://nowsecure.nl/)
- [Google reCAPTCHA v3 demo](https://recaptcha-demo.appspot.com/recaptcha-v3-request-scores.php)
- [AntCPT score detector](https://antcpt.com/score_detector/)
- [2Captcha demos](https://2captcha.com/demo)
- [BrowserLeaks](https://browserleaks.com/)
- [CreepJS](https://abrahamjuliot.github.io/creepjs/)
- [Fingerprint Playground](https://demo.fingerprint.com/playground)

Khi test, ghi challenge type, site key class, browser/version, proxy country/ASN, solve time, callback, accepted/rejected và chi phí. Token trả về không đồng nghĩa workflow end-to-end thành công.

### QA trên hệ thống mình sở hữu

Ưu tiên test keys / sandbox do nhà cung cấp CAPTCHA cung cấp để kiểm thử integration ổn định. Tách test thành tạo challenge, callback, xác minh phía server, token hết hạn và từ chối token sai. Xem [Turnstile testing](https://developers.cloudflare.com/turnstile/troubleshooting/testing/), [reCAPTCHA docs](https://developers.google.com/recaptcha) và [hCaptcha docs](https://docs.hcaptcha.com/). Không gửi API key, cookie hoặc dữ liệu người dùng vào log benchmark công khai.

<a id="if-you-are-building-a-captcha"></a>
## Khi bạn cần xây dựng CAPTCHA

| Product | Vị trí | Phân tích |
|---|---|---|
| [Google reCAPTCHA](https://www.google.com/recaptcha/about/) | Ecosystem rộng | Dễ tích hợp; cân nhắc privacy và score |
| [Cloudflare Turnstile](https://www.cloudflare.com/products/turnstile/) | Low-friction managed challenge | Widget miễn phí, tích hợp Cloudflare |
| [hCaptcha](https://www.hcaptcha.com/) | Managed bot/fraud controls | Có Pro và Enterprise |
| [Friendly Captcha](https://friendlycaptcha.com/) | Proof-of-work | Giảm image puzzle |
| [ALTCHA](https://altcha.org/) | Open-source/self-hosted | Hợp self-host/GDPR-sensitive |
| [Private Captcha](https://github.com/PrivateCaptcha/PrivateCaptcha) | Open-source | Proof-of-work self-host |
| [Arkose Labs](https://www.arkoselabs.com/) | Risk-based enterprise | Tập trung fraud/abuse prevention |

<a id="libraries-and-docs"></a>
## Thư viện và tài liệu

- [2Captcha SDKs](https://github.com/2captcha), [CapSolver docs](https://docs.capsolver.com/en/), [CapMonster docs](https://docs.capmonster.cloud/)
- [reCAPTCHA docs](https://developers.google.com/recaptcha), [Turnstile docs](https://developers.cloudflare.com/turnstile/), [hCaptcha docs](https://docs.hcaptcha.com/)
- [Friendly Captcha integrations](https://friendlycaptcha.com/integrations/), [ALTCHA docs](https://altcha.org/docs/), [PrivateCaptcha](https://github.com/PrivateCaptcha/PrivateCaptcha)
- [svg-captcha](https://github.com/produck/svg-captcha), [Captcha for Laravel](https://github.com/mewebstudio/captcha), [Gregwar Captcha](https://github.com/Gregwar/Captcha)

<a id="methodology"></a>
## Lưu ý khi sử dụng

Giá là snapshot ngày 27/10/2026, có thể thay đổi theo kỳ hạn, cấu hình và khuyến mại. Chưa benchmark toàn bộ dịch vụ; các mục chưa xác minh được đánh dấu riêng. Link provider là link trực tiếp, không affiliate. Xem [hướng dẫn đóng góp](CONTRIBUTING.md).

<a id="related-ndt-lists"></a>
## Dự án NDT liên quan

- [NDT Proxy Scraper](https://github.com/nguyenduytan/NDT-Proxy-Scraper)

- [NDT Proxy Providers List](https://github.com/nguyenduytan/NDT-Proxy-Providers-List)
- [NDT Antidetect Tools](https://github.com/nguyenduytan/NDT-Antidetect-Tools)

> [!WARNING]
> Chỉ dùng cho authorized QA, accessibility, fraud-prevention testing và internal automation. Không dùng để bypass security controls.
