# Einführung in CSS mit einem einfachen Linktree-Design

CSS (Cascading Style Sheets) ist eine Stylesheet-Sprache, die verwendet wird, um das Design und Layout von HTML-Dokumenten zu gestalten. In diesem Beispiel verwenden wir CSS, um eine schlichte und ansprechende Linktree-Seite zu erstellen.

---

## 1️⃣ **Grundstruktur des HTML-Dokuments**

Das HTML-Gerüst enthält:
- **Einen Container** (`div.container`), der das zentrale Layout der Seite bildet.
- **Ein Profilbild** (`img.avatar`).
- **Einen Titel und eine Beschreibung** (`h2` und `p`).
- **Drei Links**, die als Navigationsbuttons fungieren (`a.link`).

### Beispiel-HTML-Struktur:
```html
<div class="container">
    <img src="avatar.jpg" alt="Profilbild" class="avatar">
    <h2>Mein Name</h2>
    <p>Kurze Beschreibung über mich.</p>
    <a href="#" class="link">Link 1</a>
    <a href="#" class="link">Link 2</a>
    <a href="#" class="link">Link 3</a>
</div>
```

---

## 2️⃣ **Einbindung von CSS**
Es gibt drei Methoden, CSS zu nutzen:
1. **Inline-CSS** (direkt im HTML-Element) → **nicht empfohlen** wegen schlechter Wartbarkeit.
2. **Internes CSS** (im `<style>`-Tag im `<head>`) → geeignet für kleinere Projekte.
3. **Externes CSS** (in einer separaten Datei, z. B. `styles.css`) → **beste Methode** für größere Projekte.

In unserem Beispiel verwenden wir internes CSS.

---

## 3️⃣ **CSS-Regeln in unserem Code erklärt**

### 🔹 **Hintergrund und Schriftart für die gesamte Seite**
```css
body {
    font-family: Arial, sans-serif;
    text-align: center;
    background-color: #f4f4f4;
    padding: 20px;
}
```

### 🔹 **Gestaltung des Hauptcontainers**
```css
.container {
    max-width: 400px;
    margin: auto;
    background: white;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}
```

### 🔹 **Gestaltung des Profilbilds**
```css
.avatar {
    width: 100px;
    height: 100px;
    border-radius: 50%;
    margin-bottom: 10px;
}
```

### 🔹 **Gestaltung der Links**
```css
.link {
    display: block;
    background: #007BFF;
    color: white;
    text-decoration: none;
    padding: 10px;
    margin: 10px 0;
    border-radius: 5px;
}
```

### 🔹 **Hover-Effekt für die Links**
```css
.link:hover {
    background: #0056b3;
}
```

---

## 4️⃣ **Optimierung mit externer CSS-Datei**
Statt das CSS direkt im HTML zu schreiben, sollte man eine **separate CSS-Datei** verwenden, um die Übersichtlichkeit zu erhöhen.

### `styles.css`:
```css
body {
    font-family: Arial, sans-serif;
    text-align: center;
    background-color: #f4f4f4;
    padding: 20px;
}
.container {
    max-width: 400px;
    margin: auto;
    background: white;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}
.avatar {
    width: 100px;
    height: 100px;
    border-radius: 50%;
    margin-bottom: 10px;
}
.link {
    display: block;
    background: #007BFF;
    color: white;
    text-decoration: none;
    padding: 10px;
    margin: 10px 0;
    border-radius: 5px;
}
.link:hover {
    background: #0056b3;
}
```

Dann fügst du in dein HTML-Dokument im `<head>`-Bereich hinzu:
```html
<link rel="stylesheet" href="styles.css">
```

Jetzt ist das CSS **ausgelagert** und leichter zu verwalten.

---

## ✅ **Zusammenfassung**
✔️ CSS steuert das Design von HTML-Seiten.  
✔️ **Internes CSS** ist für kleine Projekte geeignet, aber **externes CSS** ist besser für größere Projekte.  
✔️ **Wichtige CSS-Eigenschaften**: `background`, `color`, `padding`, `margin`, `border-radius`, `box-shadow`, `hover`.  
✔️ **Bester Praxisansatz**: CSS in eine **separate Datei auslagern**.

---

## 📌 **Mögliche Erweiterungen**
🎨 **Farbschema ändern** (z. B. Dunkelmodus).  
🖼 **Hintergrundbild statt Farbe verwenden**.  
🔄 **Animationen oder Hover-Effekte verbessern**.  
📱 **Responsives Design mit `@media`-Queries**.
