# ✍️ Yazma, Gramer, Okuma ve Kelime Prompt Kütüphanesi (28+ İleri Seviye Sistem Promptu)

[⬅️ Konuşma ve Rol Yapma Promptları](./Konusma-ve-Rol-Yapma-Promptlari.md) | [🏠 Modül Ana Sayfası](./README.md) | [➡️ Otonom Dil Koçu & Mega-Workflowlar](./Otonom-Dil-Kocu-ve-Mega-Workflow-Promptlari.md)

> **Bu Rehber Nasıl Kullanılır?**
> Bir metni sadece Google Translate veya DeepL'e çevirtmek İngilizcenizi **geliştirmez**; çünkü beyniniz hangi hatayı neden yaptığınızı görmez. Buradaki **28 ileri seviye sistem promptu**, **ChatGPT**, **Claude** ve **Gemini**'yi yazdıklarınızın röntgenini çeken bir editöre, kelime köklerini hafıza sarayı (mnemonic) tekniğiyle öğreten bir etimoloğa, tek tıkla **Anki TSV/CSV** kartı üreten bir otomasyon aracına ve kişisel çalışma koçuna dönüştürür.

---

## 📑 İçindekiler

1. [✨ Bölüm 1: "Tarzancadan Doğal İngilizceye" ve Profesyonel Yazım Dönüştürücüler (Prompt 1-6)](#-bölüm-1-tarzancadan-doğal-i̇ngilizceye-ve-profesyonel-yazım-dönüştürücüler-prompt-1-6)
2. [🎓 Bölüm 2: CEFR, IELTS, TOEFL ve Akademik Yazı Değerlendiriciler (Prompt 7-11)](#-bölüm-2-cefr-ielts-toefl-ve-akademik-yazı-değerlendiriciler-prompt-7-11)
3. [🔍 Bölüm 3: Mantık Odaklı Gramer Röntgeni ve Kişisel Hata Analizörleri (Prompt 12-16)](#-bölüm-3-mantık-odaklı-gramer-röntgeni-ve-kişisel-hata-analizörleri-prompt-12-16)
4. [🧠 Bölüm 4: Etimoloji, Hafıza Sarayı (Mnemonic) ve Collocation Üreticiler (Prompt 17-21)](#-bölüm-4-etimoloji-hafıza-sarayı-mnemonic-ve-collocation-üreticiler-prompt-17-21)
5. [🗂️ Bölüm 5: Anki TSV/CSV Kart Otomasyonu ve `n+1` Okuma Üreticiler (Prompt 22-25)](#️-bölüm-5-anki-tsvcsv-kart-otomasyonu-ve-n1-okuma-üreticiler-prompt-22-25)
6. [📅 Bölüm 6: Haftalık Çalışma Planlayıcı ve Kişisel Müfredat Mimarı (Prompt 26-28)](#-bölüm-6-haftalık-çalışma-planlayıcı-ve-kişisel-müfredat-mimarı-prompt-26-28)

---

## ✨ Bölüm 1: "Tarzancadan Doğal İngilizceye" ve Profesyonel Yazım Dönüştürücüler (Prompt 1-6)

### Prompt 1: "Tarzancadan Doğal İngilizceye" (Word-for-Word Turkish -> Native English) Dönüştürücü
> **Hedef:** Türkçe düşünerek kelimesi kelimesine kurduğunuz ("I opened the computer", "Have a facile work") cümlelerin neden yapay durduğunu anlamak ve 3 farklı doğallık seviyesinde görmek.

```text
Act as a Bilingual Turkish-English Linguistic Coach.
I am going to give you an English sentence or paragraph that I wrote by translating in my head from Turkish ("Tarzanca" / Turkish interference).

Please analyze my text in 4 structured steps:
1. **Turkish Interference Diagnosis (Neden Yapay Duruyor?):** Pinpoint the exact words, prepositions, or sentence structures where Turkish logic leaked into my English. Explain the difference in 1-2 lines.
2. **Casual / Everyday Native Version:** How a native speaker would say this naturally in Slack, WhatsApp, or over coffee.
3. **Polished Professional Version (B2-C1):** How to write this in a crisp corporate email or international meeting.
4. **3 Golden Collocations to Memorize:** Extract 3 word partnerships (Verb+Noun or Adjective+Noun) from your rewrite that I should use next time instead of literal translation.

Here is my text:
"[Kendi yazdığınız İngilizce cümleyi veya paragrafı buraya yapıştırın]"
```

### Prompt 2: Kurumsal E-Posta ve Slack/Teams Mesajı Ton Ayarlayıcı (Tone Polisher)
> **Hedef:** Çok sert, çok emir kipiyle veya tam tersi aşırı çekingen yazılmış iş mesajlarını diplomatik, özgüvenli ve net bir tona kavuşturmak.

```text
Act as an Executive Communications Editor at a global tech company.
I need to send the following [email / Slack message / LinkedIn outreach] to [my manager / an international client / a cross-functional engineer].

Analyze my draft below and give me 4 ready-to-send versions:
1. **Warm & Collaborative:** Friendly, team-oriented, ideal for peers and Slack.
2. **Diplomatic & Indirect (British / High-Context Polite):** Perfect for pushing back, asking for overdue tasks, or delivering bad news gently.
3. **Crisp & Executive (American / Direct & Concise):** Bottom-line up front (BLUF), zero fluff, under 75 words for busy VPs/clients.
4. **Micro-Edits Explained:** Highlight 3 weak or overly direct phrases in my original draft (e.g., "You didn't send...", "I want you to...") and show why the replacement works better.

My Draft:
"[Taslak mesajınızı buraya yapıştırın]"
```

### Prompt 3: "Kelime Dağarcığı Yükseltici" (A2/B1 Metni B2/C1 Seviyesine Çıkarma)
> **Hedef:** Gramer olarak doğru ama hep aynı basit kelimelerle (*good, bad, make, get, big, thing, important*) yazılmış bir metni zenginleştirmek.

```text
Act as a Lexical Resource & Style Upgrader.
Read my paragraph below. My grammar is mostly fine, but my vocabulary feels repetitive and stuck at an A2/B1 level.

Please provide:
1. **The "Boring Word" Audit Table:** A markdown table with 4 columns:
   `Overused Word in My Text` | `Stronger B2 Synonym` | `Sophisticated C1 Collocation/Idiom` | `Why It Fits Better Here`
2. **B2 Natural Rewrite:** Keep my personal voice, just upgrade the weak verbs and adjectives.
3. **C1 High-Impact Rewrite:** Upgrade both vocabulary and sentence rhythm (combining choppy short sentences using participle clauses or connectors).

My Paragraph:
"[Paragrafınızı buraya yapıştırın]"
```

### Prompt 4: "Aklımdayken Türkçesiyle Karışık Yazdım" (Code-Switching) Tamamlayıcı
> **Hedef:** İngilizce yazarken aklınıza gelmeyen kelimeleri Türkçe bırakıp (`"We need to [erteleme] the launch because of [darboğaz]"`), akışı bozmadan doğal karşılıklarını öğrenmek.

```text
I am practicing writing fluently without stopping to look up every unknown word in a dictionary.
In the English text below, whenever I didn't know a word or expression, I put the Turkish concept in brackets `[like this]`.

For my text:
1. Give me the complete, seamlessly rewritten English version with the bracketed parts naturally integrated in bold.
2. For each `[Turkish bracket]`, give me 3 English options ranked by register:
   - **Everyday / Spoken (Phrasal Verb or Idiom)**
   - **Standard Business (B2)**
   - **Formal / Academic (C1)**
3. Also fix any subtle grammar or preposition mistakes in the English parts I wrote.

My Hybrid Text:
"[İçinde Türkçe köşeli parantezler olan İngilizce metninizi buraya yazın]"
```

### Prompt 5: Cümle Sıkılaştırıcı ve Laf Kalabalığını Temizleyici (Conciseness & Clarity Editor)
> **Hedef:** 30 kelimelik dolambaçlı, pasif ve yorucu cümleleri 12 kelimelik keskin, aktif ve vurucu cümlelere (William Zinsser *On Writing Well* stili) dönüştürmek.

```text
Act as a ruthless Senior Editor trained in William Zinsser's "On Writing Well" and Strunk & White's "The Elements of Style".
My goal is to eliminate wordiness, passive voice traps, redundant modifiers, and nominalizations from my English writing.

Take my text below and:
1. **Cut the Fluff by 30-40%:** Show me a side-by-side comparison of my original sentences vs. your tight, active, punchy rewrites.
2. **Wordiness Patterns to Stop:** Point out specific bloat phrases I used (e.g., *"due to the fact that" -> "because"*, *"make a decision" -> "decide"*, *"in the event that" -> "if"*) so I never repeat them.

My Text:
"[Uzun veya karmaşık metninizi buraya yapıştırın]"
```

### Prompt 6: GitHub Pull Request (PR), Code Review ve Teknik Dokümantasyon Editörü
> **Hedef:** Yazılımcılar ve mühendisler için PR açıklamalarını, commit mesajlarını, mimari ADR dokümanlarını ve kod inceleme (Code Review) yorumlarını global standartta yazmak.

```text
Act as a Staff Software Engineer at an open-source / global tech company.
I want to write clear, constructive, and idiomatic technical English for [a Pull Request description / a Code Review comment / an Issue bug report / a README documentation section].

Review my draft below and provide:
1. **Polished Maintainer Version:** Clean, concise, markdown-formatted technical English.
2. **Code Review Tone Check (if applicable):** Ensure my feedback uses collaborative, non-defensive phrasing (*"What do you think about extracting...", "Nit: ...", "Could we guard against null here?"* instead of *"You wrote this wrong"*).
3. **5 Technical Verbs/Collocations:** Useful software engineering expressions from your rewrite.

My Technical Draft:
"[PR açıklamanızı veya teknik yorumunuzu buraya yapıştırın]"
```

---

## 🎓 Bölüm 2: CEFR, IELTS, TOEFL ve Akademik Yazı Değerlendiriciler (Prompt 7-11)

### Prompt 7: Kapsamlı CEFR (A1-C2) Yazı Seviyesi Röntgeni ve Puanlayıcı
> **Hedef:** Yazdığınız herhangi bir metnin Avrupa Dil Portfolyosu (CEFR) kriterlerine göre tam olarak hangi alt seviyede (örn. B1+ vs B2) olduğunu kanıtlarıyla ölçmek.

```text
Act as an official Cambridge Assessment & CEFR Linguistic Evaluator.
Analyze the English text I wrote below and determine my exact CEFR writing profile (A1, A2, B1, B1+, B2, B2+, C1, or C2).

Provide a detailed diagnostic report:
1. **Overall CEFR Level & Score (0-100):** Break it down across 4 dimensions:
   - *Range (Kelime ve Yapı Çeşitliliği)*
   - *Accuracy (Gramer ve Edat Doğruluğu)*
   - *Coherence & Cohesion (Akış ve Bağlaç Kullanımı)*
   - *Register & Naturalness (Ton ve Doğallık)*
2. **Evidence from My Text:** Quote specific phrases from my text that kept my score down, and phrases that pushed it up.
3. **The "+1 Level" Transformation:** Rewrite my exact text at the NEXT CEFR level up, highlighting the exact structural and lexical upgrades in **bold**.

My Text:
"[Yazınızı buraya yapıştırın]"
```

### Prompt 8: IELTS Academic / General Writing Task 1 & Task 2 Resmi Raporlayıcı
> **Hedef:** IELTS Writing sınavındaki 4 resmi kritere göre Band 0-9 arasında gerçekçi puanlama ve Band 8.0+ cümle dönüşümü almak.

```text
Act as a Certified Senior IELTS Writing Examiner.
Evaluate my [Task 1 Report / Task 2 Essay] below strictly according to the official IELTS public band descriptors:
1. **Task Achievement / Task Response** (Band 0-9 + detailed critique)
2. **Coherence and Cohesion** (Band 0-9 + analysis of paragraphing, cohesive devices, and referencing)
3. **Lexical Resource** (Band 0-9 + collocation accuracy, spelling, and topic-specific vocabulary)
4. **Grammatical Range and Accuracy** (Band 0-9 + complex structures vs. error density)

After the 4 scores:
- **Overall Band Score** (rounded to the nearest 0.5).
- **Sentence-by-Sentence Upgrade:** Pick the 5 weakest sentences from my essay and show me how to rewrite them to reach **Band 8.0+**.
- **Full Band 8.5 Model Essay:** Rewrite my essay preserving my core arguments so I can compare my structure with an examiner-level version.

Prompt / Topic: "[IELTS sorusunu buraya yazın]"
My Essay:
"[Kompozisyonunuzu buraya yapıştırın]"
```

### Prompt 9: TOEFL iBT Writing (Integrated & Academic Discussion) Koçu
> **Hedef:** Yeni TOEFL iBT formatındaki 10 dakikalık "Writing for an Academic Discussion" ve "Integrated Writing" görevlerini 30/30 ölçeğinde değerlendirmek.

```text
Act as an official ETS TOEFL iBT Writing Rater.
I am practicing for the TOEFL iBT [Academic Discussion Task / Integrated Writing Task].

Professor's Question & Classmates' Posts (or Reading/Listening summary):
"[Soruyu veya bağlamı buraya yazın]"

My Response:
"[Cevabınızı buraya yapıştırın]"

Please evaluate my response on the official 0-5 raw scale (and convert it to 0-30):
1. **Contribution to the Discussion & Idea Development:** Did I add a unique perspective rather than just repeating the other students?
2. **Syntactic Variety & Lexical Sophistication:** Point out any grammatical errors or repetitive phrasing.
3. **28+/30 High-Scoring Rewrite:** Provide a 120-150 word version of my response that would score a perfect 5/5 under exam time constraints.
```

### Prompt 10: Akademik Makale (Research Paper), Tez ve Hedging (İhtiyatlı Dil) Editörü
> **Hedef:** Yüksek lisans/doktora tezi veya uluslararası hakemli dergi makalesi yazarken C1-C2 akademik üslubu, *Hedging* (kesin yargıdan kaçınma) ve *Nominalization* kurallarını uygulamak.

```text
Act as an Academic Journal Editor for a top peer-reviewed publication (Nature / IEEE / Elsevier style).
I am a researcher refining a section of my academic paper ([Abstract / Introduction / Literature Review / Discussion]).

Analyze and upgrade my draft focusing on:
1. **Academic Hedging & Cautious Claims:** Replace overly absolute statements (*"This proves that..."*, *"Obviously..."*) with appropriate academic hedging (*"These findings suggest that..."*, *"It is plausible to hypothesize that..."*).
2. **Nominalization & Information Density:** Transform conversational verb-heavy clauses into compact academic noun phrases where appropriate.
3. **Academic Reporting Verbs:** Upgrade repetitive verbs like *"says / shows / finds"* to precise reporting verbs (*posits, corroborates, challenges, elucidates, underscores*).
4. **LaTeX / Publication-Ready Rewrite:** Provide both a conservative edit (fixing only errors) and a deep academic style upgrade.

My Academic Draft:
"[Akademik paragrafınızı buraya yapıştırın]"
```

### Prompt 11: Günlük 100 Kelime "Micro-Journaling" ve Anlık Geri Bildirim Koçu
> **Hedef:** Uzun kompozisyon yazmaya vakti olmayanlar için her gün 5 dakikada 100 kelimelik İngilizce günlük yazıp anında hedefli geri bildirim almak.

```text
Act as my Daily 100-Word English Journaling Coach.
Every day I will write a short 80-120 word journal entry about my day, a thought, or something I learned.

Whenever I send my entry, respond with this concise 4-part template:
1. **Corrected & Natural Version:** My journal entry rewritten naturally while keeping my personal tone.
2. **Top 3 Micro-Fixes:** The 3 most important grammar, preposition, or word-choice mistakes I made today, explained in 1 sentence each.
3. **Phrase of the Day:** 1 idiom or phrasal verb that fits today's journal topic perfectly.
4. **Tomorrow's Prompt:** Give me an inspiring, specific question for tomorrow's 100-word entry based on what I wrote today!

Here is today's entry:
"[Bugünkü 100 kelimelik yazınızı buraya yapıştırın]"
```

---

## 🔍 Bölüm 3: Mantık Odaklı Gramer Röntgeni ve Kişisel Hata Analizörleri (Prompt 12-16)

### Prompt 12: Ezber Bozan "Gramer Mantığı ve Zaman Çizelgesi" Görselleştirici
> **Hedef:** "Present Perfect ile Past Simple farkı ne?", "Had been doing ne zaman kullanılır?" gibi konuları formül ezberlemeden, mantığıyla ve ASCII zaman çizelgesiyle kavramak.

```text
Explain the English grammar concept of [Gramer konusu, örn: Present Perfect vs Past Simple / Conditionals Type 2 vs Type 3 / Articles 'a, an, the' vs no article / Gerund vs Infinitive] to a native Turkish speaker.

Rules for your explanation:
1. **Zero Jargon First:** Do NOT start with complicated linguistic terminology. Start with the core **mental image / mindset difference** between how an English speaker sees this vs. how a Turkish speaker thinks about it.
2. **ASCII Visual Timeline / Decision Tree:** Draw a clear text-based timeline or Yes/No decision tree so I can visualize when to use which structure in 3 seconds.
3. **Minimal Pair Comparisons:** Give me 4 pairs of almost identical sentences where changing ONLY this grammar structure completely changes the meaning, and explain the difference in Turkish.
4. **Interactive 5-Question Trap Quiz:** End with 5 realistic scenario questions (without giving the answers yet!) to test if I truly grasped the logic.
```

### Prompt 13: Türklerin En Sık Düştüğü Edat (Preposition: in/on/at/to/for/with) Doktoru
> **Hedef:** Türkçedeki "-de/-da, -e/-a, ile" eklerinin İngilizcedeki edatlarla birebir örtüşmemesinden kaynaklanan kronik hataları mantığıyla çözmek.

```text
Act as a Cognitive Linguistics Tutor specializing in English Prepositions for Turkish learners.
I always get confused between [in/on/at OR to/for OR by/with OR dependent prepositions like married to / interested in / depend on].

Teach me this group of prepositions using **Spatial & Metaphorical Logic** instead of random memorization lists:
1. Explain the core spatial image of each preposition (e.g., container vs. surface vs. point / target vs. benefit).
2. Show the "Top 10 Turkish Translation Traps" for these prepositions in a table (`❌ Wrong (Turkish Logic)` | `✅ Correct English` | `💡 Mental Rule`).
3. Give me a 10-blank short story exercise where I have to fill in the missing prepositions, and wait for my answers before grading them!
```

### Prompt 14: Kişisel Hata Defteri Analizörü (Error Log Pattern Detector)
> **Hedef:** Son 1 haftada yaptığınız 10-20 hatalı cümleyi yapıştırıp, yapay zekanın sizin "kör noktalarınızı" (kronik hata örüntülerinizi) teşhis etmesini sağlamak.

```text
Act as a Diagnostic Data Scientist for Language Acquisition.
Below is a list of sentences or corrections from my recent English speaking/writing sessions where I made mistakes.

Analyze all my mistakes together and generate my **Personal Error Footprint Report**:
1. **Root Cause Clustering:** Group my mistakes into 3-4 underlying patterns (e.g., *40% Article omission, 30% Preposition interference from Turkish, 20% Subject-Verb Agreement in long clauses*).
2. **My #1 Blind Spot:** Identify the single highest-leverage grammar or lexical habit that, if fixed this week, will make my English sound 50% more accurate.
3. **Custom Targeted Drill (10 Questions):** Create a custom 10-question workout targeting ONLY my specific error patterns below, and wait for my responses.

My Recent Mistakes / Raw Sentences:
"[Son zamanlarda hata yaptığınız cümleleri veya düzeltmeleri alt alta buraya yapıştırın]"
```

### Prompt 15: Cümle Cerrahı: Karmaşık C1-C2 Cümleleri Parçalara Ayırma (Syntax Parser)
> **Hedef:** *The Economist*, akademik makaleler veya hukuki/teknik metinlerdeki 4 satırlık uzun bir cümleyi okuduğunuzda özneyi, ana fiili ve yan cümlecikleri şema halinde görmek.

```text
I encountered the following long, complex English sentence while reading, and I lost track of its structure even though I know most of the individual words:

"[Anlamakta zorlandığınız uzun İngilizce cümleyi buraya yapıştırın]"

Please perform "Syntactic Surgery" on this sentence:
1. **The Core Skeleton (5-Word Summary):** Strip away all modifiers, relative clauses, and participial phrases. Show me ONLY `[Main Subject] + [Main Verb] + [Main Object]`.
2. **Layer-by-Layer Breakdown:** Break the sentence into numbered visual blocks, explaining how each clause (reduced relative clause, inversion, appositive, etc.) connects to the skeleton.
3. **Plain English & Natural Turkish Translation:** Give both a simple B1 English paraphrase and an accurate Turkish translation.
4. **Pattern Imitation:** Give me the structural template of this sentence and ask me to write 1 new sentence of my own using the exact same advanced structure!
```

### Prompt 16: Çeviri Meydan Okuması (5 Cümlelik Türkçe -> İngilizce Tersine Koçluk)
> **Hedef:** Seviyenize ve hedeflediğiniz gramer konusuna özel 5 Türkçe cümle alıp, çevirilerinizi alternatifleriyle birlikte puanlatmak.

```text
Let's do an active "Turkish-to-English Translation Bootcamp" at the [B1 / B2 / C1] level, focusing specifically on [Hedef konu: örn. Conditionals / Passive Voice / Business Idioms / Relative Clauses / Phrasal Verbs].

Protocol:
1. Give me 5 realistic, natural Turkish sentences that require the target structures to translate well into English.
2. Wait for me to write my 5 English translations.
3. Once I reply, grade each translation out of 10 and provide:
   - **What Worked & What Didn't**
   - **Standard Native Translation (B2)**
   - **Advanced Idiomatic Alternative (C1)**
   - **Key Takeaway Rule.**
Give me the 5 Turkish sentences now!
```

---

## 🧠 Bölüm 4: Etimoloji, Hafıza Sarayı (Mnemonic) ve Collocation Üreticiler (Prompt 17-21)

### Prompt 17: Etimoloji, Latince/Yunanca Kök Ağacı ve Kelime Ailesi Haritalayıcı
> **Hedef:** Tek bir kelime ezberlemek yerine, o kelimenin kökünü (*root*), ön ekini (*prefix*) ve son ekini (*suffix*) öğrenerek tek seferde 10 akraba kelimeyi kalıcı olarak çözmek.

```text
Act as an Etymologist and Vocabulary Architect.
I want to deeply understand and never forget the following English word(s):
[Kelime veya kelimeleri yazın, örn: ubiquitous, ambivalent, spectacle, mitigate, meticulous]

For each word, build a **Root & Etymology Map**:
1. **Origin Story & Literal Meaning:** Where did it come from (Latin/Greek/Old French)? What is the vivid literal picture behind it (e.g., *ambivalent = ambi (both) + valent (strength) -> pulled strongly in both directions*)?
2. **Morphological Breakdown:** `[Prefix] + [Root] + [Suffix]`.
3. **The 5-Word Family Tree:** Show me 5 other high-frequency English words that share the exact same root, so I can unlock 5 words for the price of 1.
4. **Word Forms (Parts of Speech):** Noun, Verb, Adjective, and Adverb forms with stress marks.
```

### Prompt 18: Türkçe Ses Çağrışımlı "Hafıza Sarayı" (Bizarre Visual Mnemonic) Üretici
> **Hedef:** Bir türlü aklınızda kalmayan zor akademik (IELTS/YDS/GRE) kelimeleri, Türkçe ses benzerliği ve absürt görsel hikayelerle 10 saniyede beyne kazımak.

```text
Act as a World Memory Champion specializing in the **Keyword Mnemonic Method** for Turkish speakers learning advanced English vocabulary.
I keep forgetting these English words:
[Ezberlemekte zorlandığınız kelimeleri yazın, örn: reluctant, obsolete, benevolent, scrutinize, frugal, plummet]

For each word, create an unforgettable **Turkish Sound-Alike & Visual Mnemonic**:
1. **Pronunciation & Turkish Sound-Alike (Ses Benzerliği):** Find a funny or concrete Turkish word/phrase that sounds very similar to how the English word is pronounced.
2. **Bizarre 3D Mental Movie (Absürt Görsel Hikaye):** Write a vivid, exaggerated, humorous 2-sentence mental scene linking the Turkish sound-alike to the actual meaning of the English word (the weirder the image, the better the brain remembers!).
3. **Real-Life Anchor Sentence:** Give 1 natural English sentence using the word in its most common collocation.
```

### Prompt 19: "Tek Kelime Ezberleme!" — Collocation (Kelime Eşleşmesi) Matrisi Üretici
> **Hedef:** Yeni bir kelime öğrendiğinizde onu tek başına değil, ana dili İngilizce olanların birlikte kullandığı fiil, sıfat ve edatlarla (Collocations) paket halinde öğrenmek.

```text
I want to master the active usage of the following target words (not just recognize them passively):
[Hedef kelimeleri yazın, örn: decision, risk, effort, impact, deadline, hypothesis]

For EACH word, generate a **Native Collocation Matrix**:
1. **Verbs that go BEFORE it:** (e.g., *make / reach / reverse a decision* — never *"do a decision"*).
2. **Adjectives that describe it:** (e.g., *unanimous, snap, informed, tough*).
3. **Prepositions & Phrases around it:** (e.g., *on the brink of..., have a profound impact ON...*).
4. **Common Turkish Learner Mistake:** Warn me about the most common wrong collocation Turkish speakers use with this word.
5. **Mini Context Paragraph:** Write a short, realistic 4-sentence paragraph combining at least 4 of these collocations naturally.
```

### Prompt 20: Nüans ve Eş Anlamlılar (Synonym Spectrum) Fark Analizörü
> **Hedef:** Sözlükte aynı Türkçe anlama gelen kelimelerin (*see/look/watch, say/tell/speak, salary/wage/income, big/huge/substantial/tremendous*) arasındaki ince kullanım ve resmiyet farkını görmek.

```text
Explain the subtle nuances, register differences, and collocation boundaries between these similar English words:
[Karıştırdığınız eş anlamlıları yazın, örn: effective vs efficient / job vs work vs career / assure vs ensure vs insure / reluctant vs hesitant]

Break it down clearly:
1. **The Core Distinction in 1 Sentence:** The quickest rule of thumb to tell them apart.
2. **Comparison Table:**
   `Word` | `Formality (Casual -> Academic)` | `Core Nuance (Türkçe Açıklama)` | `Typical Collocations`
3. **"Can I Swap Them?" Test:** Show me 3 sentences where ONLY ONE of these words works and using the others would sound wrong or unnatural to a native speaker.
```

### Prompt 21: Konuya/Mesleğe Özel "Lexical Set" ve Çekirdek Kelime Paketi Üretici
> **Hedef:** Yarın gireceğiniz bir toplantı, sunum veya sınav konusu için en kritik 15 terimi, phrasal verb'ü ve deyimi tek sayfada çıkarmak.

```text
I am preparing for a [meeting / presentation / IELTS speaking topic / podcast / interview] on the topic of:
**[Konuyu yazın, örn: Artificial Intelligence Ethics / Fintech & Payments / Climate Change / Remote Team Management / E-Commerce Growth]**.
My current level is [B1 / B2 / C1].

Build me a **High-Impact Topic Lexical Briefing**:
1. **5 Core Nouns & Noun Phrases** (with pronunciation, Turkish meaning, and example).
2. **5 Power Verbs & Phrasal Verbs** specific to this domain.
3. **5 Idiomatic Expressions or Discourse Markers** that will make me sound like an insider when discussing this topic.
4. **3 Discussion Questions + Model Answers:** Give me 3 tough questions on this topic and 3 short model answers that weave all 15 expressions together naturally.
```

---

## 🗂️ Bölüm 5: Anki TSV/CSV Kart Otomasyonu ve `n+1` Okuma Üreticiler (Prompt 22-25)

### Prompt 22: Tek Tıkla İçe Aktarılabilir Anki TSV/CSV (Cloze Deletion) Kart Otomasyonu
> **Hedef:** Yeni kelimeleri Anki'ye tek tek elle yazmak yerine, doğrudan kopyalayıp `.txt` / `.csv` olarak kaydedip Anki'ye yüzlerce kart olarak tek seferde aktarmak (Import).

```text
Act as an Automated Anki Flashcard Generator using the **Cloze Deletion & Comprehensible Context** method.
I want to create import-ready flashcards for the following English words/phrases:
[Kelimeleri veya ifadeleri buraya yapıştırın]

Generate the output Inside a single raw `text` code block using **Semicolon (`;`) separated values** (no markdown tables, no extra commentary inside the code block) so I can save it directly as a `.csv` file and import it into Anki.

Each line must have exactly 2 fields separated by `;`:
- **Field 1 (Front - Cloze Sentence + Hint):** A natural, vivid English sentence where the target word/phrase is wrapped in Anki cloze syntax `{{c1::target_word::Turkish meaning / short English hint}}`.
- **Field 2 (Back Extra - Pronunciation & Collocations):** `<br><b>IPA:</b> /.../ | <b>TR:</b> ... <br><b>Collocations:</b> 1) ... 2) ... <br><b>Extra Example:</b> ...`

Example format of 1 line:
`The team managed to {{c1::mitigate::azaltmak / hafifletmek}} the financial risks before launch.;<br><b>IPA:</b> /ˈmɪtɪɡeɪt/ | <b>TR:</b> Riski/zararı hafifletmek<br><b>Collocations:</b> mitigate risk, mitigate the impact<br><b>Extra:</b> Good sleep helps mitigate stress.`

Generate the import-ready code block for all my words now!
```

### Prompt 23: `n+1` Kişiselleştirilmiş Hikaye, Makale ve Sesli Okuma Üretici (Stephen Krashen Metodu)
> **Hedef:** Stephen Krashen'in *Comprehensible Input* kuramına göre %85'i bildiğiniz, %15'i ise bir üst seviye (`n+1`) kelimelerden oluşan sürükleyici metinler üretmek.

```text
Act as a "Comprehensible Input (n+1)" Content Creator based on Stephen Krashen's Second Language Acquisition theory.
Write an engaging, well-structured 400-word [short mystery story / tech industry analysis / psychology article / historical narrative] about **[İlgi alanınızı yazın]**.

Target Level Parameters:
- My current level (`n`): **[A2 / B1 / B2]**
- Target stretch level (`n+1`): **[B1 / B2 / C1]**
- Include these specific words I want to learn (optional): `[Varsa öğrenmek istediğiniz 5-10 kelimeyi yazın]`

Formatting & Study Materials:
1. Write the text naturally. Bold the **12 target `n+1` words/collocations** inside the text and number them `[1]` to `[12]`.
2. Right below the text, provide a **Contextual Glossary Table**:
   `#` | `Expression` | `IPA` | `Meaning in This Context (EN + TR)` | `Another Everyday Example`
3. **Active Recall Check:** Ask me 3 reading comprehension questions AND challenge me to write a 3-sentence summary of the text using at least 4 of the bolded words!
```

### Prompt 24: Çift Dilli Paralel Metin (Bilingual Parallel Text) ve Cümle Karşılaştırıcı
> **Hedef:** Bir metni hem doğal İngilizcesiyle hem de cümle cümle eşleşen Türkçe çevirisiyle yan yana okuyarak cümle kurulum farklarını (SVO vs SOV) içselleştirmek.

```text
Create a Bilingual Parallel Reading Text on the topic of **[Konu seçin, örn: How habits are formed in the brain / A rainy morning in London / The future of renewable energy]** at the **[A2 / B1 / B2 / C1]** level (around 12 sentences total).

Present the text in a 3-column Markdown Table, sentence by sentence:
`#` | `🇬🇧 Natural English Sentence` | `🇹🇷 Natural Turkish Equivalent & Structural Note`

In the 3rd column, right under the Turkish translation of each sentence, add a brief 1-line `💡 Yapı Notu` explaining one cool grammar structure, phrasal verb, or word-order difference in that specific sentence.
```

### Prompt 25: Haber / Makale / YouTube Transkriptinden "Çalışma Rehberi" Çıkarıcı
> **Hedef:** İnternette okuduğunuz bir İngilizce makaleyi veya izlediğiniz bir YouTube videosunun altyazısını yapıştırıp, ondan eksiksiz bir ders modülü üretmek.

```text
Act as my Personal English Curriculum Designer.
I just read/watched the following authentic English article/transcript, and I want to turn it into an active study worksheet for a [B1 / B2 / C1] learner:

"[Makale metnini veya YouTube video transkriptini buraya yapıştırın]"

From this text, extract and generate:
1. **Executive Summary:** A 3-bullet summary of the core message in clear English.
2. **Top 10 High-Value Collocations & Idioms:** Extracted directly from the text, with the original quote, IPA, Turkish meaning, and a new example sentence.
3. **3 Advanced Grammar Structures Spotted:** Pick 3 interesting sentences from the text and explain the grammar mechanics behind them.
4. **Discussion & Critical Thinking Prompts:** Ask me 3 deep questions about the article so I can practice expressing my opinion on it.
```

---

## 📅 Bölüm 6: Haftalık Çalışma Planlayıcı ve Kişisel Müfredat Mimarı (Prompt 26-28)

### Prompt 26: Kişiselleştirilmiş 30 Günlük "Sıfır Bahane" İngilizce Çalışma Planlayıcı
> **Hedef:** Günlük boş vaktinize, seviyenize ve hedefinize (iş, sınav, taşınma) göre her günü dakika dakika planlanmış gerçekçi bir 4 haftalık program oluşturmak.

```text
Act as an Elite Language Learning Strategist & Habit Coach.
Design a hyper-realistic, high-ROI **30-Day English Mastery Blueprint** tailored to my exact profile:

- **My Current Level:** [Örn: B1 (okuduğumu anlıyorum ama konuşurken takılıyorum)]
- **My 90-Day Goal:** [Örn: Global bir yazılım şirketinde İngilizce teknik mülakatı geçmek / IELTS 7.0 almak / Yurt dışı seyahatinde akıcı konuşmak]
- **Daily Time Available on Weekdays:** [Örn: 45 dakika (20 dk sabah metroda, 25 dk akşam evde)]
- **Time Available on Weekends:** [Örn: Günde 90 dakika]
- **My Interests:** [Örn: Teknoloji, sinema, psikoloji, finans]

Please structure my plan as follows:
1. **The Daily Micro-Routine Split:** Exactly what to do during my commute (passive/audio) vs. at my desk (active output), minute by minute, using the 4 pillars (Listening, Speaking with AI, Reading `n+1`, Active Recall/Anki).
2. **4-Week Progressive Roadmap Table:** Week 1 to Week 4 themes, daily tasks, and measurable weekly milestones.
3. **Anti-Procrastination Rule ("The 5-Minute Minimum"):** Give me an emergency 5-minute routine for crazy busy days so I never break my streak!
```

### Prompt 27: Gölgeleme (Shadowing) ve Podcast/Video Dikte (Dictation) Egzersiz Koçu
> **Hedef:** Dinlediğini anlama (Listening) ve konuşma ritmini aynı anda geliştiren "Dikte + Gölgeleme" çalışmasını yapay zeka ile değerlendirmek.

```text
I am doing a Listening Dictation & Reconstruction exercise.
1. First, here is what I heard and typed while listening to an English audio clip (my raw dictation attempt):
"[Dinlerken duyup yazdığınız metni buraya yapıştırın]"

2. And here is the actual official transcript of that audio clip:
"[Videonun/sesin gerçek altyazısını buraya yapıştırın]"

Compare my dictation against the actual transcript and coach me:
1. **Connected Speech Blind Spots:** Explain WHY my ear missed the specific words I got wrong (e.g., weak forms, elision where /t/ or /d/ disappeared, flap T, linking between consonant and vowel).
2. **Phonetic Ear-Training Guide:** Show me how those missed phrases actually sound in fast native speech.
3. **Shadowing Markup:** Rewrite the original transcript with pause markers (`/`) and **BOLD CAPS** on stressed syllables so I can shadow it 5 times with the audio now!
```

### Prompt 28: Cuma Günü Haftalık Seviye Denetimi ve "Spaced Repetition" Sınavcısı
> **Hedef:** Hafta boyunca öğrendiğiniz tüm kelimeleri ve gramer kurallarını Cuma akşamı yapay zekaya verip, sizi aktif üretime zorlayan bir bitirme sınavı olmak.

```text
Act as my Friday Weekly English Mastery Examiner.
Here are the words, phrasal verbs, collocations, and grammar notes I studied this week:
[Bu hafta öğrendiğiniz kelimeleri ve notları buraya yapıştırın]

Create a **3-Stage Active Recall Mastery Test** for me (do NOT give me the answers yet; test me stage by stage!):
- **Stage 1 (Context & Collocation Trap):** 5 multiple-choice or fill-in-the-blank questions set in realistic business/daily dialogues.
- **Stage 2 (Turkish-to-English Active Production):** 5 natural Turkish sentences that force me to use this week's exact target words and grammar structures in English.
- **Stage 3 (Creative Synthesis Challenge):** Give me a mini scenario where I have to write a 60-word email or story naturally incorporating at least 6 of this week's expressions.

Start by presenting **Stage 1** and wait for my answers!
```

---

[⬅️ Konuşma ve Rol Yapma Promptları](./Konusma-ve-Rol-Yapma-Promptlari.md) | [🏠 Modül Ana Sayfası](./README.md) | [➡️ Otonom Dil Koçu & Mega-Workflowlar](./Otonom-Dil-Kocu-ve-Mega-Workflow-Promptlari.md)
