# 🛠️ Yazılım Mühendisliği, Agile/Scrum ve GitHub İngilizcesi Rehberi

[⬅️ Modül Ana Sayfası](./README.md) | [🏠 Repo Ana Sayfası](../README.md) | [➡️ Global İş Bulma, CV ve Mülakat Rehberi](./Global-Is-Bulma-CV-Mulakat-Rehberi.md)

> **Bu Rehberin Amacı:** Bir yazılım mühendisinin günlük mesaisinde en çok ihtiyaç duyduğu **Git commit mesajları, GitHub Issue & Pull Request (PR) şablonları, yapıcı Code Review kalıpları, Agile/Scrum toplantı (Daily Stand-up, Planning, Retro) ifadeleri, Pair Programming diyalogları, System Design (Mimari Tasarım) tartışma cümleleri** ve **Teknik Terimler Sözlüğünü** kopyala-yapıştır (copy-paste) kalitesinde sunmak.

---

## 📑 İçindekiler

1. [📝 Git Commit Mesajları ve "Conventional Commits" İngilizcesi](#-git-commit-mesajları-ve-conventional-commits-ingilizcesi)
2. [🐛 GitHub Issue Açma Şablonları (Bug Report & Feature Request)](#-github-issue-açma-şablonları-bug-report--feature-request)
3. [🚀 Pull Request (PR) Açma Şablonları ve Açıklama Kalıpları](#-pull-request-pr-açma-şablonları-ve-açıklama-kalıpları)
4. [🔍 Code Review (Kod İnceleme) Yapma ve Yanıtlama Kalıpları](#-code-review-kod-inceleme-yapma-ve-yanıtlama-kalıpları)
5. [🏃‍♂️ Agile & Scrum Toplantı Kalıpları (Daily Stand-up, Planning, Retro)](#️-agile--scrum-toplantı-kalıpları-daily-stand-up-planning-retro)
6. [👥 Pair Programming ve Canlı Debugging İfadeleri](#-pair-programming-ve-canlı-debugging-ifadeleri)
7. [🏗️ System Design (Sistem Mimarisi) Tartışma ve Trade-off Kalıpları](#️-system-design-sistem-mimarisi-tartışma-ve-trade-off-kalıpları)
8. [📖 Yazılımcılar İçin Kapsamlı Teknik Terimler, Deyimler ve Kısaltmalar Sözlüğü](#-yazılımcılar-için-kapsamlı-teknik-terimler-deyimler-ve-kısaltmalar-sözlüğü)

---

## 📝 Git Commit Mesajları ve "Conventional Commits" İngilizcesi

Global ekiplerde ve açık kaynak projelerde Git commit mesajları **Emir Kipi (Imperative Mood)** ile yazılır.

> 💡 **Altın Test:** Yazdığınız commit mesajı şu cümlenin boşluğunu gramer olarak doğru tamamlamalıdır:
> ***"If applied, this commit will _____________"***
> * ✅ *"If applied, this commit will **fix race condition in payment worker**"* (`fix`, `fixed` veya `fixes` değil!)
> * ✅ *"If applied, this commit will **add rate limiting to login endpoint**"* (`add`, `added` veya `adding` değil!)

### 1. En Sık Kullanılan Commit Fiilleri ve Örnekleri

| Commit Tipi | Emir Kipi Fiiller | Doğru Commit Mesajı Örnekleri (✅) | Yanlış Örnekler (❌) |
| :--- | :--- | :--- | :--- |
| **`feat:`** (Yeni Özellik) | `add`, `implement`, `introduce`, `support`, `enable` | `feat(auth): implement OAuth2 Google login flow` | `added google login` |
| **`fix:`** (Hata Çözümü) | `fix`, `resolve`, `prevent`, `handle`, `patch` | `fix(cart): prevent negative quantity on item update` | `fixed bug in cart` |
| **`refactor:`** (Kod İyileştirme) | `refactor`, `extract`, `simplify`, `decouple`, `rename` | `refactor(billing): extract tax calculation into helper` | `refactoring code` |
| **`perf:`** (Performans) | `optimize`, `cache`, `memoize`, `speed up`, `reduce` | `perf(db): add composite index to speed up user lookup` | `faster queries` |
| **`docs:`** (Dokümantasyon) | `document`, `update`, `clarify`, `fix typo in` | `docs(readme): clarify local Docker setup instructions` | `updated readme` |
| **`test:`** (Test Ekleme) | `add unit tests for`, `mock`, `cover`, `fix flaky test` | `test(checkout): add edge-case tests for expired coupons` | `more tests` |
| **`chore:` / `ci:`** (Altyapı) | `bump`, `upgrade`, `configure`, `remove unused` | `chore(deps): bump axios from 1.6.0 to 1.7.2` | `package updates` |

### 2. Detaylı (Multi-line) Commit Mesajı Şablonu
Büyük bir değişiklik yaptığınızda sadece başlık yetmez; gövde (*body*) kısmında **"Ne değiştiğinden ziyade NEDEN değiştiğini"** açıklamalısınız:

```text
fix(orders): prevent duplicate order creation on double-click

Previously, clicking the "Place Order" button rapidly over a high-latency
connection sent multiple POST requests before the UI disabled the button.

This commit introduces an idempotency key header (`X-Idempotency-Key`)
stored in Redis with a 5-minute TTL so subsequent identical requests
return the cached response instead of creating duplicate database records.

Fixes #418
```

---

## 🐛 GitHub Issue Açma Şablonları (Bug Report & Feature Request)

Açık kaynak bir projede veya şirket içi Jira/Linear/GitHub'da "çalışmıyor" demek yerine mühendislik standartlarında Issue açmak sizi anında profesyonel gösterir.

### Şablon 1: Kusursuz Hata Raporu (Bug Report)

```markdown
### Describe the Bug
When a user with a non-ASCII character in their display name (e.g., `ğ`, `ş`, `ü`) exports their invoice as a PDF, the generation service crashes with an unhandled `UnicodeEncodeError`.

### Steps to Reproduce
1. Go to **Account Settings -> Profile**.
2. Update the **Full Name** field to `"Çağrı Öztürk"` and click **Save**.
3. Navigate to **Billing -> Invoices** and click **Download PDF** on any invoice.
4. Observe the HTTP 500 Internal Server Error in the network tab.

### Expected Behavior
The PDF invoice should render UTF-8 characters properly and download without throwing a server error.

### Actual Behavior / Stack Trace
The server responds with status `500` and logs the following exception:
```text
UnicodeEncodeError: 'latin-1' codec can't encode character '\u011f' in position 14
```

### Environment
* **Service Version:** `v3.4.1`
* **OS / Browser:** macOS 14.5 / Chrome 128
* **Region:** `eu-central-1`

### Possible Fix (Optional)
It appears the PDF generator defaults to the `Helvetica` standard font, which only supports `latin-1`. Embedding a UTF-8 TrueType font (such as `Inter` or `DejaVuSans`) should resolve the issue.
```

### Şablon 2: Özellik Talebi (Feature Request / Enhancement)

```markdown
### Problem Statement / Motivation
Currently, webhook failures fail silently after the initial attempt. If a customer's endpoint experiences a brief network blip, they permanently miss critical `payment.succeeded` events and have to reconcile data manually via the API.

### Proposed Solution
Implement an automated retry mechanism with exponential backoff (e.g., retry at 1m, 5m, 30m, 2h, and 12h) for any webhook delivery that returns a `5xx` status code or times out.

### Alternatives Considered
* Providing a manual "Replay Webhook" button in the dashboard (useful, but still requires manual intervention from the customer).

### Acceptance Criteria
- [ ] Failed webhooks (`5xx` or network timeout) are automatically queued for up to 5 retries.
- [ ] `4xx` client errors (except `429 Too Many Requests`) are NOT retried.
- [ ] Customers can view the delivery history and retry attempts in the Developer Dashboard.
```

---

## 🚀 Pull Request (PR) Açma Şablonları ve Açıklama Kalıpları

İnceleyen kişinin (Reviewer) işini kolaylaştıran bir PR açıklaması, kodunuzun çok daha hızlı onaylanmasını (`Approved & Merged`) sağlar.

### Profesyonel PR Açıklama Şablonu

```markdown
## 📌 Summary (What & Why)
This PR introduces rate limiting to the `/api/v1/auth/login` and `/api/v1/auth/reset-password` endpoints to mitigate brute-force credential stuffing attacks. Related to security audit ticket **SEC-109**.

## 🛠️ Key Changes
* Added a Redis-backed sliding-window rate limiter middleware (`src/middleware/rateLimiter.ts`).
* Configured a limit of **5 attempts per 15 minutes** per IP + email combination.
* Standardized the `429 Too Many Requests` response payload to include the `Retry-After` header.
* Added unit and integration tests covering allowed, throttled, and Redis-fallback scenarios.

## 🔍 Reviewer Notes (Where to Look)
* Look closely at `src/middleware/rateLimiter.ts` (lines 42–68): I opted for a **fail-open** strategy so that if Redis is temporarily unreachable, login requests are still allowed through while triggering a high-priority Datadog alert. Let me know if you prefer **fail-closed** here.

## 🧪 How to Test Locally
1. Run `docker compose up -d redis` to start the local Redis instance.
2. Execute `npm run test:integration -- rateLimiter.spec.ts`.
3. Alternatively, send 6 consecutive POST requests to `/api/v1/auth/login` and verify that the 6th returns `HTTP 429`.

## ✅ Checklist
- [x] Self-reviewed my own code
- [x] Added/updated unit & integration tests
- [x] Updated API documentation (`openapi.yaml`)
- [x] No breaking changes introduced
```

### PR Açarken ve Güncellerken Kullanılan Hazır Cümleler

* **Taslak PR Açarken (Draft PR):**
  * *"Opening this as a draft PR to get early feedback on the overall architecture before I write the remaining unit tests."* (Kalan birim testlerini yazmadan önce genel mimari hakkında erken geri bildirim almak için bunu taslak PR olarak açıyorum.)
* **İnceleme İsterken:**
  * *"This PR is ready for review! @sarah @mehmet could you take a look when you have some bandwidth?"* (Bu PR incelemeye hazır! Müsaitliğiniz olduğunda göz atabilir misiniz?)
* **Geri Bildirimleri Düzelttikten Sonra:**
  * *"Thanks for the thorough review! I've addressed all the comments and pushed the updates in `a4f92c1`. Ready for another pass (PTAL)."* (Detaylı inceleme için teşekkürler! Tüm yorumları ele aldım ve güncellemeleri gönderdim. Tekrar bakabilirsiniz.)

---

## 🔍 Code Review (Kod İnceleme) Yapma ve Yanıtlama Kalıpları

Global ekiplerde Code Review bir "ego savaşı" değil, **kod kalitesini birlikte yükseltme** sürecidir. Yorumlarınızın **önem derecesini (severity)** belirtmek için şu önekleri (*prefixes*) kullanın:

### 1. Code Review Etiketleri (Conventional Comments)

| Etiket | Anlamı (PR'ı Bloklar mı?) | Kullanım Amacı |
| :--- | :---: | :--- |
| **`[blocking]` / `issue:`** | **Evet (Değişmeli)** | Güvenlik açığı, bug, veri kaybı veya ciddi performans sorunu var. |
| **`suggestion:`** | Opsiyonel / Tavsiye | Daha temiz, okunabilir veya idiomatik bir alternatif önerisi. |
| **`question:` / `clarification:`** | Hayır | Kodun neden öyle yazıldığını anlamak için sorulan samimi soru. |
| **`nit:` (Nitpick)** | **Hayır (Bloklamaz)** | Çok ufak detay (boşluk, değişken ismi, yazım hatası). Düzeltilmese de PR onaylanır. |
| **`praise:`** | Hayır | Çok şık çözülmüş bir kodu takdir etmek için (ekip motivasyonunu artırır!). |

---

### 2. Code Review Yorumu Yazma Kalıpları (Reviewer İçin)

#### 🔴 Hata veya Kritik Sorun Belirtme (`Blocking`)
* *"I think there might be a race condition here if two requests arrive simultaneously. What if we wrap this block in a database transaction?"*
* *"If `user.profile` is `undefined`, line 48 will throw a `TypeError`. Could we use optional chaining (`user?.profile?.avatarUrl`) or add a guard clause?"*
* *"This query runs inside a `for` loop, which introduces an **N+1 query problem** when fetching large lists. We should probably batch-fetch these IDs using an `IN` clause instead."*
* *"Heads-up: It looks like an API key / secret was accidentally committed in `.env.example`. Let's remove it and rotate the key before merging."*

#### 🟡 İyileştirme ve Refactoring Önerme (`Suggestion`)
* *"Suggestion: We could extract this validation logic into a separate helper function to keep the controller lean and easier to unit-test."*
* *"Instead of mutating the array in place, what do you think about using `.map()` or `.filter()` here to keep it immutable?"*
* *"To improve readability, we could use an **early return** (guard clause) at the top of the function to avoid deep `if/else` nesting."*

#### 🟢 Ufak Detaylar (`Nitpick`) ve Övgü (`Praise`)
* *"Nit: Typo in the variable name (`recieveResponse` -> `receiveResponse`). Non-blocking!"*
* *"Nit: Could we rename `d` to `expirationDays` so the unit of time is immediately obvious to future readers?"*
* *"Praise: This recursive parser is super clean and well-tested—great job simplifying the legacy logic!"*
* *"LGTM! 🚀 Just left two minor non-blocking nits, approving in advance so you're not blocked."* (`LGTM` = *Looks Good To Me*)

---

### 3. Code Review Yorumlarına Cevap Verme Kalıpları (Author İçin)

| Durum | Profesyonel Yanıt Kalıbı |
| :--- | :--- |
| **Haklı Bir Hatayı Kabul Etme** | *"Great catch! I completely missed that edge case. Fixed in `c81b3e2`."* (Harika yakaladın! O uç durumu tamamen gözden kaçırmışım. Düzeltildi.) |
| **Öneriyi Uygulama** | *"Good call—extracting that into a custom hook makes it much cleaner. Updated!"* (Güzel fikir; bunu özel bir hook'a çıkarmak kodu çok daha temiz yaptı. Güncellendi!) |
| **Kibarca Karşı Çıkma / Açıklama** | *"I considered that approach initially, but since this function is called on every scroll event, creating a new object each time caused noticeable GC pressure in profiling. Happy to add a code comment explaining why!"* |
| **Başka Bir PR'a Erteleme (Scope Creep)** | *"Totally agree we should refactor that legacy module! Since this PR is already getting quite large, would you mind if I create a follow-up ticket to tackle that separately?"* |

---

## 🏃‍♂️ Agile & Scrum Toplantı Kalıpları (Daily Stand-up, Planning, Retro)

### 1. Daily Stand-up (Günlük 90 Saniyelik Güncelleme)
Daily Stand-up'ta destan anlatılmaz; **Dün ne bitti, bugün ne yapılacak ve önünüzde bir engel (blocker) var mı** net şekilde söylenir.

#### 🗣️ Hazır Stand-up Konuşma Şablonu (Kopyala & Uyarla)
> *"Morning everyone! **Yesterday**, I wrapped up the pagination logic for the orders API and opened PR #214—it's currently awaiting review. **Today**, I'm picking up JIRA-508 to integrate the new SendGrid email templates. **No blockers** on my end, though I might ping @alex later today to double-check one of the webhook payload fields. That's it from me!"*

#### 📋 Duruma Göre Stand-up Cümle Havuzu

| Aşama | Doğal Mühendislik İfadeleri |
| :--- | :--- |
| **Dün Ne Yaptım?** | • *"Yesterday, I **wrapped up / finished up** the unit tests for..."*<br>• *"I spent most of yesterday **debugging / investigating** a memory leak in staging."*<br>• *"I **paired with** @cem on the database migration script and we got it working."*<br>• *"I **addressed the review comments** on PR #88 and merged it into `main`."* |
| **Bugün Ne Yapacağım?** | • *"Today, my main focus is **implementing** the file upload endpoint."*<br>• *"I'm going to **continue working on** JIRA-302; it's about 70% done."*<br>• *"Once my PR is merged, I'll **pick up** the next ticket from the top of the sprint backlog."* |
| **Engel (Blocker) Bildirme** | • *"I'm currently **blocked on** the staging API credentials—@devops could you help me out after stand-up?"*<br>• *"Not a hard blocker yet, but I'm **waiting on** the final Figma specs for the error modal."*<br>• *"No blockers on my end, everything is **on track**."* |

---

### 2. Sprint Planning & Backlog Refinement (Planlama ve Puanlama)
* **Kapsamı Netleştirme (Scope Clarification):**
  * *"Before we estimate this ticket, could we clarify the acceptance criteria around offline mode?"* (Bu işi puanlamadan önce çevrimdışı modla ilgili kabul kriterlerini netleştirebilir miyiz?)
  * *"Does this ticket include the backend API changes as well, or is that tracked separately?"* (Bu iş backend API değişikliklerini de kapsıyor mu, yoksa o ayrı mı takip ediliyor?)
* **Zorluk ve Puan (Story Points) Tartışma:**
  * *"On the surface this looks like a 2-pointer, but since it touches the legacy billing code which has zero test coverage, I'd lean towards a **5** to account for testing and regression risk."*
  * *"This story feels too big to complete within a single sprint. Should we **break it down** into smaller vertical slices?"*
* **Kapasite ve Taahhüt (Capacity & Commitment):**
  * *"Keep in mind that we have a public holiday on Thursday and I'm on call this week, so our team velocity might be slightly lower than usual."*

---

### 3. Sprint Retrospective (Sprint Değerlendirme Toplantısı)
* **İyi Gidenler (What Went Well / Shout-outs):**
  * *"Huge **shout-out** to @elena and @burak for jumping on that production incident on Tuesday and resolving it in under 20 minutes."*
  * *"Breaking down our large epics into smaller PRs really improved our review turnaround time this sprint."*
* **Geliştirilmesi Gerekenler (What Could Be Improved):**
  * *"We had quite a bit of **scope creep** mid-sprint on the dashboard feature, which pushed our original deliverables to the last day."*
  * *"Several PRs sat in the review queue for over 48 hours. Maybe we can set up a Slack reminder or a dedicated daily review slot?"*
* **Aksiyon Alma (Action Items):**
  * *"As a concrete action item for next sprint, let's make sure every bug ticket includes clear reproduction steps before it enters the sprint."*

---

## 👥 Pair Programming ve Canlı Debugging İfadeleri

Başka bir mühendisle ekran paylaşıp canlı kod yazarken (*Driver / Navigator*) sessiz kalmamak ve sesli düşünmek (*thinking out loud*) çok önemlidir:

| Durum | Doğal Konuşma Kalıbı |
| :--- | :--- |
| **Ekran Paylaşımı Kontrolü** | • *"Let me share my screen—can you see my IDE clearly, or should I bump up the font size?"* (Fontu büyüteyim mi?) |
| **Sürücü / Gözlemci Rolü** | • *"Do you want to **drive** first while I **navigate**, and then we can switch after 30 minutes?"* |
| **Sesli Düşünme** | • *"Let me think out loud for a second: we receive the raw array here, so first we need to group it by `tenantId`..."* |
| **Bir Satıra Yönlendirme** | • *"Could you scroll up to line 64 for a second? I want to check the return type of that function."* |
| **Nazikçe Hata Gösterme** | • *"Hold on—I think `userId` on line 32 might be a string from the URL params, so `===` against a number will evaluate to `false`."* |
| **Hipotez Test Etme** | • *"Just to sanity-check our assumption, let's put a breakpoint / `console.log` right before the `try/catch` block and see what the payload actually looks like."* |
| **Takılıp Kalınca** | • *"We've been going down this rabbit hole for 20 minutes. Let's take a step back and check the official docs."* |

---

## 🏗️ System Design (Sistem Mimarisi) Tartışma ve Trade-off Kalıpları

Kıdemli mühendisler mimari toplantılarda ve System Design mülakatlarında hiçbir zaman *"X en iyisidir"* demezler; her zaman **Trade-off (Ödünleşim / Artı-Eksi Dengesi)** üzerinden konuşurlar.

### 1. Gereksinimleri Toplama (Clarifying Functional & Non-Functional Requirements)
* *"Before diving into the high-level architecture, I'd like to clarify our **read-to-write ratio** and expected **QPS (Queries Per Second)** at peak."*
* *"What are our **SLA / availability** targets here? Are we aiming for **four nines (99.99%)**, and can the system tolerate **eventual consistency**, or do we strictly need **strong consistency**?"*
* *"What does our latency budget look like for the **p95 and p99** percentiles?"*

### 2. Mimari Ödünleşimleri (Trade-offs) İfade Etme
* *"There's a classic **trade-off** here between **consistency and latency**. If we replicate synchronously across regions, we guarantee zero data loss, but we take a ~60ms cross-region network penalty on every write."*
* *"While a **microservices architecture** gives teams independent deployment velocity, at our current team size a **modular monolith** avoids distributed systems overhead and network serialization costs."*
* *"Using a **message queue (like Kafka or RabbitMQ)** allows us to **decouple** the ingestion API from the heavy image-processing workers and **smooth out traffic spikes** (load leveling)."*

### 3. Darboğazları ve Tek Hata Noktalarını (Bottlenecks & SPOF) Konuşma
* *"In this diagram, the primary relational database becomes a **Single Point of Failure (SPOF)** and a **write bottleneck** once we exceed ~10k concurrent writes per second."*
* *"To alleviate read pressure on the primary DB, we can introduce **read replicas** combined with a **write-through / read-aside Redis cache** in front of the service."*
* *"What happens if the third-party payment gateway goes down? We should wrap that call in a **Circuit Breaker** with a graceful fallback so it doesn't cause **cascading failures** across our upstream services."*

---

## 📖 Yazılımcılar İçin Kapsamlı Teknik Terimler, Deyimler ve Kısaltmalar Sözlüğü

Gerçek mühendislik toplantılarında her gün duyacağınız ama standart sözlüklerde bulamayacağınız **35 Kritik Mühendislik Deyimi (Engineering Idioms & Jargon)**:

| Terim / Deyim | Telaffuz / Okunuş İpucu | Gerçek Mühendislik Anlamı | Örnek Cümle |
| :--- | :--- | :--- | :--- |
| **Tech Debt (Technical Debt)** | *tek det* (`b` okunmaz!) | Hızlı çıkmak için yapılan geçici çözümlerin ileride yarattığı bakım maliyeti (Teknik Borç). | *"We need to allocate 20% of next sprint to paying down tech debt."* |
| **Yak Shaving** | *yak şeyving* | Asıl işi yapmak için gereken başka bir sorunu, onun için de başka bir sorunu çözerken ilk hedefle alakasız bir yerde kaybolmak. | *"I just wanted to fix a CSS button, and three hours of yak shaving later I'm upgrading our Docker base image."* |
| **Bikeshedding** | *bayk-şeding* | Zor ve kritik mimari konuları bırakıp herkesin fikri olduğu önemsiz detayları (örn. değişken adı, buton rengi) saatlerce tartışmak. | *"Let's not bikeshed on the linter formatting rules—just pick the default and move on."* |
| **Rubber Ducking** | *rabır daking* | Sorunu bir başkasına (veya plastik bir ördeğe) baştan sona sesli anlatırken cevabı kendi kendine bulmak. | *"Thanks for listening—just rubber ducking this with you helped me spot the bug!"* |
| **Footgun** | *fut-gan* | Kullanıcının veya yazılımcının yanlışlıkla kendi ayağına sıkmasına çok müsait olan tehlikeli özellik/API. | *"Allowing raw SQL strings from the frontend is a massive security footgun."* |
| **Boilerplate** | *boylır-pleyt* | İş mantığı içermeyen, sadece yapı kurmak için tekrar tekrar yazılan standart kalıp kod. | *"We switched to this library because it eliminates 80% of the Redux boilerplate."* |
| **Happy Path** | *hepi peth* | Hiçbir hatanın çıkmadığı, tüm girdilerin kusursuz olduğu ideal senaryo. | *"The happy path works fine, but we still need to test network timeouts and invalid payloads."* |
| **Edge Case / Corner Case** | *ec keys* | Sınır değerlerde veya nadir koşullarda ortaya çıkan uç durum (örn. 29 Şubat, boş dizi, 0'a bölme). | *"Passing an empty array is an edge case we didn't handle in the sorting algorithm."* |
| **Race Condition** | *reys kındişın* | İki işlemin aynı kaynağa eşzamanlı erişirken çalışma sırasına bağlı olarak hatalı sonuç üretmesi. | *"There's a race condition when two users try to claim the last ticket at the exact same millisecond."* |
| **Idempotency** | *ay-dem-pı-tın-si* | Bir isteğin 1 kez yapılmasıyla 10 kez yapılmasının sistemde aynı durumu yaratması. | *"Payment endpoints must be idempotent so network retries never charge the customer twice."* |
| **Bottleneck** | *batıl-nek* | Tüm sistemin hızını sınırlayan en yavaş halka (Darboğaz). | *"CPU isn't the issue; disk I/O is our main bottleneck right now."* |
| **Single Point of Failure (SPOF)** | *es-pi-o-ef* | Çöktüğünde bütün sistemi beraberinde çökerten yedeksiz bileşen. | *"Running a single load balancer instance without failover is a Single Point of Failure."* |
| **Graceful Degradation** | *greysfıl degrıdeyşın* | Sistemin bir parçası çöktüğünde tamamen kapanmak yerine kısıtlı özelliklerle çalışmaya devam etmesi. | *"If the recommendation engine fails, we gracefully degrade by showing top-selling items instead of an error page."* |
| **Blast Radius** | *blest reydiyıs* | Bir hatanın veya kesintinin etkilediği kullanıcı/servis çapı (Patlama yarıçapı). | *"We deploy to 1% of traffic first (canary release) to minimize the blast radius of potential bugs."* |
| **Smoke Test / Sanity Check** | *smok test* | Büyük bir dağıtımdan sonra sistemin temel işlevlerinin çöküp çökmediğini kontrol eden hızlı ilk test. | *"Deployment to staging is done—running a quick smoke test before notifying QA."* |
| **Flaky Test** | *fleyki test* | Kod hiç değişmediği halde bazen geçen bazen kalan güvenilmez test. | *"That end-to-end test is super flaky due to hardcoded `sleep(1000)` timers."* |
| **Scope Creep** | *skop kriip* | İş başladıktan sonra kapsamın sürekli küçük eklemelerle şişmesi ve bitiş tarihinin sarkması. | *"Let's guard against scope creep and keep the v1 release strictly focused on core features."* |
| **Bus Factor** | *bas fektır* | Projeyi bilen kaç kişi ekipten ayrılırsa (veya "otobüs çarparsa") projenin tamamen duracağı sayısı. | *"Right now only Cem knows how the legacy deployment script works—our bus factor on that service is 1."* |
| **Dogfooding** | *dog-fuding* | Şirketin geliştirdiği ürünü kendi iç işlerinde bizzat kullanması (*eating your own dog food*). | *"We've been dogfooding the new analytics dashboard internally for two weeks before the public beta."* |
| **Greenfield vs Brownfield** | *grin-fild / braun-fild* | **Greenfield:** Sıfırdan, eski kod bağımlılığı olmadan kurulan yeni proje. **Brownfield:** Mevcut/eski (legacy) sistemin üzerine inşa edilen proje. | *"Building a greenfield microservice is easy; migrating a 10-year-old brownfield monolith is where the real engineering happens."* |

---

### 🔊 Türk Yazılımcıların En Sık Yanlış Telaffuz Ettiği 15 Teknik Kelime

Canlı toplantılarda ve mülakatlarda anında fark yaratan doğru telaffuzlar:

| Kelime | ❌ Yaygın Yanlış Telaffuz | ✅ Doğru Telaffuz (Okunuş) | Açıklama |
| :--- | :--- | :--- | :--- |
| **`Cache`** | *keş-e* / *kaşe* | **keş** (`/kæʃ/`) | Nakit para olan *cash* ile birebir aynı okunur! |
| **`Queue`** | *ku-e-u-e* / *kuyu* | **kyu** (`/kjuː/`) | Sadece `Q` harfini okuyormuşsunuz gibi; sondaki `ueue` tamamen sessizdir. |
| **`Deprecated`** | *deprikeytıd* (bazen *depreciated* ile karışır) | **dep-rı-key-tıd** | Vurgu ilk hecededir (`DEP`). Finans terimi olan *depreciate* (değer kaybetmek) ile karıştırmayın. |
| **`Async` / `Await`** | *asink* | **ey-sink** (`/eɪˈsɪŋk/`) | Baştaki `A` harfi "ey" diye okunur. |
| **`Idempotent`** | *idempotent* | **ay-dem-pı-tınt** | Baştaki `I` "ay" diye okunur. |
| **`Daemon`** | *daymon* | **di-mın** (`/ˈdiːmən/`) | Arka plan servisi; *demon* ile aynı okunur. |
| **`Tuple`** | *tupıl* | **ta-pıl** veya **tu-pıl** | Amerikan İngilizcesinde çoğunlukla *ta-pıl* (`/ˈtʌpəl/`) denir. |
| **`Regex`** | *receks* / *regeks* | **rec-eks** (`/ˈrɛdʒɛks/`) | *Regular Expression*'dan geldiği için `g` harfi yumuşak `c` gibi okunur. |
| **`GUI`** | *g-u-i* | **gu-i** (`/ˈɡuːi/`) | Harf harf değil, tek kelime olarak "gui" diye okunur. |
| **`SQL`** | *es-kü-el* | **es-kyu-el** veya **si-kuıl** | Her ikisi de doğrudur; ABD'de *sequel* (`/ˈsiːkwəl/`) kullanımı çok yaygındır. |
| **`Nginx`** | *en-cin-iks* | **en-cın-eks** (*Engine-X*) | Kelimenin kökeni *Engine X*'tir. |
| **`Kubernetes`** | *kubernetis* | **ku-bır-ne-tiz** | Kısaca yazılışındaki `k8s` ise **"keyts"** (`/keɪts/`) veya *"kubernetes"* diye okunur. |
| **`Hierarchy`** | *hiyerarşi* | **hay-rar-ki** (`/ˈhaɪərɑːrki/`) | Sondaki `ch` "ş" değil **"k"** sesidir! |
| **`Archive`** | *arşiv* | **ar-kayv** (`/ˈɑːrkaɪv/`) | `ch` harfleri "ş" değil **"k"** sesidir! |
| **`Width` / `Height`** | *widt* / *heyt* | **widθ** / **hayt** | *Height* kelimesi "heyt" değil, *high* gibi **"hayt"** (`/haɪt/`) diye biter! |

---

👉 **Şimdi bu teknik iletişimi global bir işe ve yüksek maaşlı bir kontrata dönüştürmek için [Global İş Bulma, CV ve Mülakat Rehberi](./Global-Is-Bulma-CV-Mulakat-Rehberi.md) dosyasına geçin!**
