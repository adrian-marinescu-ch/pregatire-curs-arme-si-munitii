# Pregătire curs Arme și Muniții (RO)

[**▶️ DEMO LIVE**](https://adrian-marinescu-ch.github.io/pregatire-curs-arme-si-munitii/) 

---

## Descriere

Acesta este un proiect static (o singură pagină) pentru exersarea grilelor la **cursul de arme și muniții** din România. Alege automat **20 de întrebări aleatorii** dintr-un set mare, **deduplicate după text**, are **cronometru** (implicit 1 oră), **temă auto/dark/light** și **controale de accesibilitate pentru mărimea textului**.
Funcționează pe **GitHub Pages** sau orice hosting static.

---

## Funcționalități cheie

* ✅ **20 întrebări aleatorii** (număr configurabil), **single-answer** cu **3 opțiuni**
* 🔁 **Deduplicare după textul întrebării** (case-insensitive, normalize)
* ⏱️ **Limită de timp** (implicit **1h**), cu **auto-submit** la expirare
* 🖨️ **Export rapid în PDF** (Întrebări + tabel cu răspunsuri) din prima pagină, păstrează selecția și opțiunile de amestecare
* 🔑 **Cod test (optional)**: introduce același cod pentru a genera exact aceleași întrebări/opțiuni pentru toți participanții
* 🎚️ **Accesibilitate**: butoane **A- / A / A+** pentru scalarea textului (persistă în `localStorage`)
* 🌓 **Temă**: **Auto** (urmează sistemul) / **Dark** / **Light** + toggle, persistă la utilizator
* 📱 **Responsive**: toolbar centrat pe desktop, **vertical & non-overlay pe mobil**
* 📊 **Progress bar**, navigare rapidă pe întrebări, **review** după submit
* 🔒 **Fără backend**: totul rulează local în browser (se folosește doar `localStorage` pentru preferințe)

---

## Cum rulezi local

```bash
# 1) Clonează repo-ul
git clone git@github.com:adrian-marinescu-ch/pregatire-curs-arme-si-munitii.git
cd pregatire-curs-arme-si-munitii

# 2) Deschide index.html direct în browser
# (sau servește-l cu un server static simplu)
```

---

### Seturile de întrebări

```js
// Structura datelor
const QUESTION_SETS = {
  capitol1: [
    {
      id: "q-001",                         // opțional (nu se folosește la deduplicare)
      text: "Exemplu de întrebare?",       // textul întrebării
      options: ["A", "B", "C"],            // EXACT 3 opțiuni
      correct: 0                           // index corect (0, 1 sau 2)
    },
    // ...
  ],
  // alte seturi...
};
```

> **Deduplicarea** se face după **`text`** (normalize + case-insensitive). Dacă ai duplicate cu același text în seturi diferite, primul rămâne.

---

## Disclaimer & Credite

> **Disclaimer:** Acest site este dezvoltat **exclusiv în scop educațional**. Nu garantăm acuratețea, actualitatea sau completitudinea informațiilor; utilizarea materialelor se face pe propria răspundere. Pentru informații oficiale, consultați legislația în vigoare și instituțiile competente.

**Dezvoltat de Adrian Marinescu**

---

## Întrebări frecvente

**Se salvează răspunsurile pe server?**
Nu. Aplicația nu are backend; preferințele de temă și mărime text se salvează local (în `localStorage`).

**Cum folosesc codul de test (optional)?**
Pe pagina de configurare există câmpul „Cod test”. Introdu același cod (de ex. `GRUPA-1`) pe toate dispozitivele și pornește testul sau exportul PDF. Generarea devine deterministă: participanții obțin aceleași întrebări și aceleași ordini ale opțiunilor, util pentru simulări coordonate sau pentru a discuta pe aceleași grile.

---

## Contribuții

* Issues și PR-uri sunt binevenite (corecturi, noi seturi de întrebări, îmbunătățiri de accesibilitate).
* Respectă stilul existent (vanilla HTML/CSS/JS, fără dependențe externe).

---

## Licență

[**GNU General Public License v3.0**](https://raw.githubusercontent.com/adrian-marinescu-ch/pregatire-curs-arme-si-munitii/refs/heads/main/LICENSE) 

---

## Compatibilitate

Testat pe ultimele versiuni de Chrome, Edge, Firefox, Safari.

---

### Mulțumiri

Mulțumesc pentru feedback-ul continuu privind UI/UX, accesibilitate și conținut. Spor la învățat și succes!
