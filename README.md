# 🏷️ Doména na prodej - Landing Page Template

Moderní, responzivní landing page pro zobrazení domény na prodej. Jednoduchý, elegantní a plně funkční template, který automaticky detekuje název domény a zobrazí ji na krásné stránce s kontaktním formulářem.

## 📋 Obsah

- [O projektu](#o-projektu)
- [Funkce](#funkce)
- [Ukázka](#ukázka)
- [Instalace](#instalace)
- [Použití](#použití)
- [Přizpůsobení](#přizpůsobení)
- [Technologie](#technologie)
- [Příspěvky](#příspěvky)
- [Licence](#licence)

## 🎯 O projektu

Tento projekt je open-source template pro vytvoření profesionální landing page pro domény na prodej. Je navržen tak, aby byl jednoduchý na použití, plně responzivní a automaticky zobrazoval název domény, na které běží.

**Perfektní pro:**
- Vlastníky domén, kteří chtějí prodat svou doménu
- Registrátory domén
- Investory do domén
- Kdokoli, kdo potřebuje rychle vytvořit stránku "Doména na prodej"

## ✨ Funkce

- 🎨 **Moderní design** - Elegantní UI s gradient pozadím a animacemi
- 📱 **Plně responzivní** - Funguje perfektně na všech zařízeních (desktop, tablet, mobil)
- 🔄 **Automatická detekce domény** - Automaticky zobrazí název domény z URL
- 💫 **Animace** - Pulzující badge "NA PRODEJ" a hover efekty
- 📧 **Kontaktní tlačítko** - Přímý odkaz na email pro zájemce
- ⚡ **Rychlý a lehký** - Pouze HTML, CSS a minimální JavaScript
- 🎯 **SEO friendly** - Správně strukturovaný HTML
- 🌐 **Bez závislostí** - Žádné frameworky, čistý vanilla JavaScript

## 🖼️ Ukázka

Stránka zobrazuje:
- Velký, výrazný název domény
- Pulzující červený badge "NA PRODEJ"
- Popisný text
- Kontaktní tlačítko s ikonou emailu
- Footer s kontaktními informacemi

## 🚀 Instalace

### Rychlý start

1. **Stáhněte nebo naklonujte projekt:**
   ```bash
   git clone https://github.com/YOUR_USERNAME/prodej-domen.git
   cd prodej_domeny
   ```

2. **Otevřete `index.html` v prohlížeči:**
   - Jednoduše dvojklikněte na soubor `index.html`
   - Nebo použijte lokální server:
     ```bash
     # Python 3
     python -m http.server 8000
     
     # Node.js (s http-server)
     npx http-server
     
     # PHP
     php -S localhost:8000
     ```

3. **Nahrajte na webhosting:**
   - Nahrajte všechny soubory (`index.html`, `styles.css`) na váš webhosting
   - Nastavte doménu tak, aby ukazovala na tyto soubory
   - Hotovo! 🎉

## 📖 Použití

### Základní použití

1. **Nahrajte soubory na vaši doménu** (např. `moje-domena.cz`)
2. **Upravte kontaktní email** v souboru `index.html` (řádek 19 a 28)
3. **Volitelně upravte text** podle vašich potřeb
4. Stránka automaticky zobrazí název domény z URL!

### Pro vývojáře

#### Struktura projektu
```
prodej_domeny/
├── index.html      # Hlavní HTML soubor
├── styles.css      # Styly a design
└── README.md       # Dokumentace
```

#### Jak to funguje

JavaScript automaticky detekuje hostname z `window.location.hostname` a zobrazí ho jako název domény. Pokud běží na `localhost`, zobrazí se výchozí hodnota `example.com`.

```javascript
function updateDomainName() {
    const currentHostname = window.location.hostname;
    
    if (currentHostname !== 'localhost' && currentHostname !== '127.0.0.1') {
        document.getElementById('domain-name').textContent = currentHostname;
        document.title = currentHostname + ' - Doména na prodej';
    }
}
```

## 🎨 Přizpůsobení

### Změna kontaktního emailu

V souboru `index.html` najděte a změňte:
```html
<!-- Řádek 19 - Tlačítko -->
<a href="mailto:your-email@example.com" class="contact-button">

<!-- Řádek 28 - Footer -->
<a href="mailto:your-email@example.com">your-email@example.com</a>
```

### Změna popisného textu

Upravte text na řádku 18:
```html
<p class="description">Tvá doména je k dispozici pro váš projekt</p>
```

### Změna barev

V souboru `styles.css` můžete upravit:
- **Gradient pozadí** (řádek 9): `background: linear-gradient(...)`
- **Barva badge** (řádek 64): `background-color: #ff6b6b`
- **Barva tlačítka** (řádek 103): `background-color: #4c7bf3`

### Změna fontu

Projekt používá Google Fonts (Montserrat). Můžete změnit na řádku 10 v `index.html`:
```html
<link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap" rel="stylesheet">
```

A pak upravit v `styles.css` na řádku 8:
```css
font-family: 'Montserrat', sans-serif;
```

### Vlastní logo nebo obrázek

Můžete přidat logo před nebo za název domény v sekci `.domain-info`:
```html
<img src="logo.png" alt="Logo" class="logo">
<h1 id="domain-name">example.com</h1>
```

## 🛠️ Technologie

- **HTML5** - Sémantický markup
- **CSS3** - Moderní styly s Flexbox, animacemi a gradienty
- **Vanilla JavaScript** - Minimální JS pro automatickou detekci domény
- **Google Fonts** - Montserrat font

## 🤝 Příspěvky

Příspěvky jsou vítány! Pokud máte nápad na vylepšení:

1. Forkněte projekt
2. Vytvořte feature branch (`git checkout -b feature/AmazingFeature`)
3. Commitněte změny (`git commit -m 'Add some AmazingFeature'`)
4. Pushněte do branch (`git push origin feature/AmazingFeature`)
5. Otevřete Pull Request

### Nápady na vylepšení
- 🌍 Přidání více jazyků
- 📊 Analytics integrace
- 💬 Kontaktní formulář místo emailu
- 🎨 Více barevných témat
- 📱 Progressive Web App (PWA) podpora

## 📝 Licence

Tento projekt je licencován pod **MIT License** - viz soubor [LICENSE](LICENSE) pro detaily.

Můžete ho volně používat pro komerční i nekomerční projekty, upravovat a distribuovat.

## 🙏 Poděkování

- [Google Fonts](https://fonts.google.com/) za krásný font Montserrat
- Všem přispěvatelům, kteří pomáhají vylepšovat tento projekt

## 📧 Kontakt

Máte otázky nebo návrhy? Otevřete [Issue](https://github.com/YOUR_USERNAME/prodej-domen/issues) nebo vytvořte Pull Request!

---

⭐ Pokud se vám projekt líbí, dejte mu hvězdičku na GitHubu! ⭐

