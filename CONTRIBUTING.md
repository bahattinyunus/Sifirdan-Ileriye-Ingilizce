# 🤝 Katkıda Bulunma Rehberi (Contributing Guide)

**Sıfırdan İleriye İngilizce** projesine katkıda bulunmak istediğiniz için teşekkür ederiz! Bu proje, Türkiye'de İngilizce öğrenmek isteyen herkesin ücretsiz, reklamsız ve doğru metodolojiyle kaliteli kaynaklara ulaşabilmesi için topluluk tarafından geliştirilmektedir.

---

## 🌟 Nasıl Katkıda Bulunabilirsiniz?

Aşağıdaki alanlardan herhangi birinde katkı sağlayabilirsiniz:

1. **Yeni Kaynak Ekleme:** Faydasını gördüğünüz YouTube kanalları, podcastler, web siteleri, kitaplar veya uygulamalar.
2. **İçerik Geliştirme:** Mevcut seviye rehberlerine (A1-A2, B1-B2, C1-C2) yeni diyaloglar, cümle kalıpları, deyimler veya çalışma ipuçları ekleme.
3. **Yapay Zeka Promptları:** Dil öğreniminde test ettiğiniz ve verimli sonuç aldığınız yeni AI prompt şablonları paylaşma.
4. **Düzeltmeler:** Yazım hatalarını, kırık linkleri veya eksik açıklamaları düzeltme.

---

## 📏 Kaynak Ekleme Kuralları (Kalite Standartlarımız)

Repodaki bilgi kirliliğini önlemek için eklenen kaynakların aşağıdaki kriterleri sağlaması gerekmektedir:

- **Ücretsiz veya Erişilebilir Olmalı:** Tamamen ücretli kursların veya korsan (telif hakkı ihlali içeren) materyallerin linkleri kabul edilmez.
- **Seviyesi Belirtilmeli:** Eklediğiniz kaynağın hangi seviyeye (`A1-A2`, `B1-B2` veya `C1-C2`) hitap ettiğini mutlaka belirtin.
- **Neden Faydalı Olduğu Açıklanmalı:** Sadece link bırakmak yerine, kaynağın nasıl kullanılması gerektiğini 1-2 cümleyle açıklayın.
- **Bağlam Odaklı Olmalı:** Tek başına kelime ezberleten listeler yerine, kelimeleri **örnek cümle ve bağlam içinde** sunan içerikler önceliklidir.

---

## 🛠️ Adım Adım Pull Request (PR) Gönderme Süreci

GitHub üzerinden katkıda bulunmak oldukça basittir:

1. **Fork'layın:** Bu reponun sağ üst köşesindeki **Fork** butonuna tıklayarak kendi hesabınıza bir kopyasını alın.
2. **Klonlayın:** Kendi hesabınızdaki repoyu bilgisayarınıza indirin:
   ```bash
   git clone https://github.com/<kullanici-adiniz>/Sifirdan-Ileriye-Ingilizce.git
   cd Sifirdan-Ileriye-Ingilizce
   ```
3. **Yeni Bir Dal (Branch) Oluşturun:** Yapacağınız değişiklik için anlamlı bir dal açın:
   ```bash
   git checkout -b ekle/b1-podcast-onerisi
   ```
4. **Değişikliklerinizi Yapın:** İlgili Markdown (`.md`) dosyasını düzenleyin ve formatın mevcut tablolarla/listelerle uyumlu olduğundan emin olun.
5. **Commit'leyin:** Değişikliklerinizi açıklayıcı bir mesajla kaydedin:
   ```bash
   git add .
   git commit -m "feat(B1-B2): yeni podcast ve shadowing kaynağı eklendi"
   ```
6. **Push'layın ve PR Açın:**
   ```bash
   git push origin ekle/b1-podcast-onerisi
   ```
   Ardından GitHub üzerinden **Pull Request** oluşturun.

---

## 📝 Örnek Kaynak Ekleme Formatı

Bir YouTube kanalı veya podcast eklerken şu şablonu kullanabilirsiniz:

```markdown
- **[Kaynak Adı](https://ornek-link.com)** (`Seviye: B1-B2`): Kısa açıklama ve bu kaynağın nasıl verimli kullanılacağına dair 1 cümlelik tavsiye.
```

---

## 💬 İletişim ve Öneriler

Kod veya Markdown bilmiyorsanız bile **Issues** sekmesinden yeni bir başlık açarak kaynak önerilerinizi veya geri bildirimlerinizi bizimle paylaşabilirsiniz!
