# Strukturierte Daten für Lax Republic

## Übersicht

Strukturierte Daten (JSON-LD Schema.org) wurden für beide Versionen der Website hinzugefügt:

1. **Hauptseite (www.lax-republic.de)** - in `index.html`
2. **Spreadshop (lax-republic.myspreadshop.de)** - in `spreadshop-custom-header.html`

---

## ✅ Was wurde in der index.html hinzugefügt?

### 1. **ClothingStore Schema** (statt einfacher Organization)
- Definiert Lax Republic als Online-Bekleidungsgeschäft
- Enthält Details zu:
  - Produktkatalog (T-Shirts, Hoodies, Accessoires)
  - Kategorien für Männer, Frauen und Accessoires
  - Zahlungsmethoden (Kreditkarte, PayPal, SEPA)
  - Währung (EUR)
  - Zielmarkt (Deutschland)

### 2. **WebSite Schema**
- Definiert die Website mit Suchfunktion
- Ermöglicht Google, eine Suchbox in den Suchergebnissen anzuzeigen

### 3. **FAQPage Schema**
- Markiert alle FAQ-Fragen und Antworten
- Google kann diese direkt in den Suchergebnissen anzeigen
- Enthält alle 6 FAQ-Fragen von der Seite

### 4. **BreadcrumbList Schema**
- Zeigt die Navigationsstruktur
- Hilft Google, die Seitenhierarchie zu verstehen
- Kann in Suchergebnissen als Breadcrumb-Navigation erscheinen

---

## ✅ Was ist im Spreadshop Custom Header?

### 1. **ItemList Schema**
- Listet die Produktgruppen auf (T-Shirts, Hoodies, Accessoires, Nachhaltige Produkte)
- Zeigt die Vielfalt des Sortiments
- **KEIN Duplikat** der Hauptseite!

### 2. **Brand Schema**
- Definiert "Lax Republic" als Marke
- Wird auf Produktseiten referenziert
- Verlinkt zurück zur Hauptseite

### 3. **Product Template** (als Kommentar)
- Vorlage für einzelne Produktseiten
- Falls du später einzelne Produkte optimieren möchtest

---

## 🚀 Wie füge ich den Code bei Spreadshop ein?

1. Gehe zu deinem Spreadshop Backend
2. Navigiere zu **Design/Einstellungen** > **Custom HTML**
3. Füge den Inhalt von `spreadshop-custom-header.html` in das Feld **"Custom Shop Header HTML"** ein
4. Speichern

---

## 🔍 Strukturierte Daten testen

### Rich Results Test (Google)
1. Gehe zu: https://search.google.com/test/rich-results
2. Füge deine URL ein: `https://www.lax-republic.de/`
3. Klicke auf "URL testen"
4. Google zeigt, welche Rich Results möglich sind

### Schema Markup Validator
1. Gehe zu: https://validator.schema.org/
2. Füge deine URL oder den HTML-Code ein
3. Prüfe auf Fehler oder Warnungen

---

## 📊 Was bringen strukturierte Daten?

### Für Suchmaschinen:
- ✅ Besseres Verständnis des Inhalts
- ✅ Mögliche Rich Snippets in Google (FAQ, Breadcrumbs, Produktinfos)
- ✅ Höhere Klickraten durch erweiterte Suchergebnisse
- ✅ Bessere Kategorisierung als E-Commerce-Website

### Für deine Website:
- ✅ Google versteht, dass es ein Lacrosse-Shop ist
- ✅ FAQ können direkt in Suchergebnissen erscheinen
- ✅ Produktkategorien werden erkannt
- ✅ Marke "Lax Republic" wird etabliert

---

## 🎯 Keine Duplikate!

**Warum keine Duplikate zwischen Hauptseite und Spreadshop?**

- **Hauptseite (www.lax-republic.de)**: 
  - ClothingStore, WebSite, FAQPage, BreadcrumbList
  - Fokus auf allgemeine Shop-Informationen
  
- **Spreadshop (lax-republic.myspreadshop.de)**:
  - ItemList, Brand, Product-Template
  - Fokus auf Produktkatalog und Marke
  - **KEINE** WebSite/ClothingStore/FAQPage (da andere Domain)

Dies vermeidet Verwirrung bei Suchmaschinen und jede Domain hat ihre eigenen, relevanten strukturierten Daten.

---

## 📝 Anpassungen für die Zukunft

### Falls du später erweitern möchtest:

1. **Social Media Profile hinzufügen**
   - Im ClothingStore Schema das `sameAs` Array füllen:
   ```json
   "sameAs": [
     "https://www.facebook.com/laxrepublic",
     "https://www.instagram.com/laxrepublic"
   ]
   ```

2. **Kontaktinformationen**
   - `contactPoint` hinzufügen für Kundenservice

3. **Bewertungen** (falls verfügbar)
   - `aggregateRating` hinzufügen

4. **Öffnungszeiten** (falls relevant)
   - `openingHoursSpecification` hinzufügen

---

## ✅ Checkliste nach Deployment

- [ ] index.html auf Vercel deployen
- [ ] Spreadshop Custom Header HTML einfügen
- [ ] Mit Google Rich Results Test testen
- [ ] Mit Schema.org Validator prüfen
- [ ] Google Search Console überprüfen (nach 1-2 Wochen)
- [ ] Prüfen ob FAQ in Google-Suchergebnissen erscheinen

---

## 🆘 Support

Falls Google Fehler oder Warnungen anzeigt:
- Prüfe, ob alle URLs korrekt sind
- Stelle sicher, dass die Bilder erreichbar sind
- Kontrolliere die JSON-Syntax (keine fehlenden Kommas etc.)

Bei Fragen zur Schema.org Dokumentation:
https://schema.org/docs/schemas.html

