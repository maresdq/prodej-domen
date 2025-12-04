# 📚 Příklady použití

Tento dokument obsahuje praktické příklady, jak můžete tento template použít a přizpůsobit.

## 🎯 Základní scénáře

### Scénář 1: Jednoduchá doména na prodej

**Situace:** Máte doménu `moje-domena.cz` a chcete ji prodat.

**Kroky:**
1. Nahrajte soubory na `moje-domena.cz`
2. Změňte email v `index.html` na váš kontaktní email
3. Hotovo! Stránka automaticky zobrazí `moje-domena.cz`

### Scénář 2: Více domén

**Situace:** Máte 10 domén a chcete pro každou samostatnou stránku.

**Řešení:**
- Vytvořte kopii projektu pro každou doménu
- Nebo použijte subdomény: `domena1.vasweb.cz`, `domena2.vasweb.cz`
- Každá subdoména automaticky zobrazí svůj název

### Scénář 3: Branding

**Situace:** Chcete přidat logo vaší společnosti.

**Kód:**
```html
<div class="domain-info">
    <img src="logo.png" alt="Vaše logo" style="max-width: 200px; margin-bottom: 2rem;">
    <h1 id="domain-name">example.com</h1>
    <!-- zbytek kódu -->
</div>
```

## 🎨 Přizpůsobení barev

### Modré téma
```css
.pulse-badge {
    background-color: #3b82f6; /* modrá */
}

.contact-button {
    background-color: #2563eb;
}
```

### Zelené téma
```css
.pulse-badge {
    background-color: #10b981; /* zelená */
}

.contact-button {
    background-color: #059669;
}
```

### Tmavé téma
```css
body {
    background: linear-gradient(135deg, #1a202c 0%, #2d3748 100%);
}

.domain-card {
    background-color: #2d3748;
    color: #e2e8f0;
}
```

## 📧 Různé způsoby kontaktu

### Email s předmětem
```html
<a href="mailto:your-email@example.com?subject=Zájem o doménu" class="contact-button">
```

### Email s předmětem a tělem
```html
<a href="mailto:your-email@example.com?subject=Zájem o doménu&body=Dobrý den,%0D%0A%0D%0AMám zájem o koupi této domény." class="contact-button">
```

### Telefonní číslo
```html
<a href="tel:+420123456789" class="contact-button">
    <span>Zavolejte nám</span>
    <svg>...</svg>
</a>
```

### Kontaktní formulář (pokročilé)
Můžete nahradit email link formulářem:
```html
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST" class="contact-form">
    <input type="email" name="email" placeholder="Váš email" required>
    <textarea name="message" placeholder="Vaše zpráva" required></textarea>
    <button type="submit" class="contact-button">Odeslat</button>
</form>
```

## 🌍 Vícejazyčná verze

### Přidání jazykového přepínače
```html
<div class="language-switcher">
    <a href="?lang=cs" class="lang-link active">Česky</a>
    <a href="?lang=en" class="lang-link">English</a>
</div>
```

### JavaScript pro přepínání jazyků
```javascript
const translations = {
    cs: {
        badge: "NA PRODEJ",
        description: "Tato doména je k dispozici pro váš projekt",
        button: "Mám zájem"
    },
    en: {
        badge: "FOR SALE",
        description: "This domain is available for your project",
        button: "I'm interested"
    }
};

function setLanguage(lang) {
    document.querySelector('.pulse-badge').textContent = translations[lang].badge;
    document.querySelector('.description').textContent = translations[lang].description;
    document.querySelector('.contact-button span').textContent = translations[lang].button;
}
```

## 📊 Přidání Analytics

### Google Analytics
```html
<!-- V <head> sekci -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

### Facebook Pixel
```html
<!-- V <head> sekci -->
<script>
  !function(f,b,e,v,n,t,s)
  {if(f.fbq)return;n=f.fbq=function(){n.callMethod?
  n.callMethod.apply(n,arguments):n.queue.push(arguments)};
  if(!f._fbq)f._fbq=n;n.push=n;n.loaded=!0;n.version='2.0';
  n.queue=[];t=b.createElement(e);t.async=!0;
  t.src=v;s=b.getElementsByTagName(e)[0];
  s.parentNode.insertBefore(t,s)}(window, document,'script',
  'https://connect.facebook.net/en_US/fbevents.js');
  fbq('init', 'YOUR_PIXEL_ID');
  fbq('track', 'PageView');
</script>
```

## 🔒 SEO optimalizace

### Přidání meta tagů
```html
<head>
    <!-- Existující tagy -->
    
    <!-- SEO -->
    <meta name="description" content="Doména [DOMAIN] je na prodej. Kontaktujte nás pro více informací.">
    <meta name="keywords" content="doména na prodej, koupit doménu, [DOMAIN]">
    <meta name="author" content="Vaše jméno">
    
    <!-- Open Graph (pro sociální sítě) -->
    <meta property="og:title" content="[DOMAIN] - Doména na prodej">
    <meta property="og:description" content="Tato doména je k dispozici pro váš projekt">
    <meta property="og:type" content="website">
    <meta property="og:url" content="https://[DOMAIN]">
    
    <!-- Twitter Card -->
    <meta name="twitter:card" content="summary">
    <meta name="twitter:title" content="[DOMAIN] - Doména na prodej">
    <meta name="twitter:description" content="Tato doména je k dispozici pro váš projekt">
</head>
```

## 🚀 Optimalizace výkonu

### Lazy loading obrázků (pokud přidáte obrázky)
```html
<img src="logo.png" alt="Logo" loading="lazy">
```

### Preload fontů
```html
<link rel="preload" href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap" as="style">
```

## 💡 Tipy a triky

1. **Testování lokálně:** Použijte lokální server místo `file://` pro správné fungování
2. **HTTPS:** Ujistěte se, že používáte HTTPS na produkci
3. **Caching:** Přidejte cache headers pro rychlejší načítání
4. **CDN:** Zvažte použití CDN pro statické soubory
5. **Backup:** Pravidelně zálohujte vaše soubory

---

Máte další příklady nebo nápady? Sdílejte je v [Issues](https://github.com/YOUR_USERNAME/prodej-domen/issues)!

