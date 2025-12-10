# Dixit Therapy - App per Sedute Terapeutiche a Distanza

Web app per utilizzare le carte Dixit durante sedute di terapia online.

## 🎯 Funzionalità

- **Deck Principale**: Scorri 5 carte alla volta da un mazzo mescolato casualmente
- **Deck Personale**: Seleziona fino a 5 carte per la sessione
- **Visualizzazione Finale**: Mostra le carte selezionate con spazio per note
- **Configurazione Admin**: Imposta il numero di carte e l'URL delle immagini

## 📦 Setup su GitHub

### 1. Crea il Repository

```bash
# Crea un nuovo repository su GitHub (es: dixit-therapy)
# Poi clona il repository sul tuo computer
git clone https://github.com/TUO-USERNAME/dixit-therapy.git
cd dixit-therapy
```

### 2. Struttura dei File

Crea questa struttura nel repository:

```
dixit-therapy/
├── index.html          # File principale dell'app
├── cards/              # Cartella con le immagini
│   ├── 1.jpg
│   ├── 2.jpg
│   ├── 3.jpg
│   └── ... (fino a 109.jpg)
└── README.md           # Questo file
```

### 3. Carica le Carte Dixit

1. Scarica tutte le 109 carte dalla cartella Google Drive
2. Assicurati che siano nominate: `1.jpg`, `2.jpg`, ... `109.jpg`
3. Mettile nella cartella `cards/` del repository

```bash
# Aggiungi tutti i file
git add .
git commit -m "Aggiunge app Dixit Therapy e carte"
git push origin main
```

### 4. Attiva GitHub Pages

1. Vai su **Settings** del repository
2. Nella sezione **Pages** (menu laterale sinistro)
3. In **Source** seleziona:
   - Branch: `main`
   - Folder: `/ (root)`
4. Clicca **Save**

Dopo qualche minuto, l'app sarà disponibile su:
```
https://TUO-USERNAME.github.io/dixit-therapy/
```

### 5. Configura l'URL delle Immagini

Quando apri l'app per la prima volta:

1. Clicca **3 volte** velocemente nell'angolo in alto a destra
2. Apparirà il pulsante **Admin**
3. Clicca su **Admin**
4. Imposta l'URL del repository:
   ```
   https://raw.githubusercontent.com/TUO-USERNAME/dixit-therapy/main/cards
   ```
   (Sostituisci `TUO-USERNAME` con il tuo username GitHub)
5. Salva

## 🎮 Come Usare l'App

### Per il Paziente/Utente:

1. **Selezione**: 
   - Scorri le carte con le frecce
   - Clicca su una carta per aggiungerla al tuo deck personale
   - Clicca di nuovo per rimuoverla

2. **Finalizza**:
   - Quando sei soddisfatto, clicca **Fine**
   - Non devi selezionare tutte e 5 le carte

3. **Revisione**:
   - Visualizza le carte scelte
   - Aggiungi note personali
   - Clicca **Nuova Sessione** per ricominciare

### Per l'Amministratore:

1. **Accesso Admin**:
   - Clicca rapidamente 3 volte nell'angolo in alto a destra
   - Apparirà il pulsante "Admin"

2. **Configurazione**:
   - Imposta quante carte usare (1-109)
   - Configura l'URL del repository GitHub
   - Le impostazioni vengono salvate nel browser

## 🔧 Personalizzazione

### Modificare il Numero di Carte nel Deck Personale

Nel file `index.html`, cerca questa riga (circa riga 350):

```javascript
} else if (personalDeck.length < 5) {  // Cambia questo 5
```

E questa (circa riga 480):

```javascript
{[0, 1, 2, 3, 4].map((index) => (  // Modifica questo array
```

### Cambiare i Colori

L'app usa Tailwind CSS. I colori principali sono:

- **Pagina Selezione**: `from-purple-100 via-blue-50 to-indigo-100`
- **Pagina Finale**: `from-green-100 via-blue-50 to-teal-100`
- **Pulsanti**: `bg-blue-600`, `bg-green-600`

## 📱 Compatibilità

- ✅ Desktop (Chrome, Firefox, Safari, Edge)
- ✅ Tablet
- ✅ Mobile (responsive design)

## 🐛 Risoluzione Problemi

### Le immagini non si caricano

1. Verifica che le carte siano nella cartella `cards/`
2. Controlla che siano nominate correttamente (1.png, 2.png, etc.)
3. Assicurati che l'URL nel pannello Admin sia corretto
4. Verifica che il repository sia pubblico

### L'app non si carica su GitHub Pages

1. Controlla che GitHub Pages sia attivato
2. Aspetta 2-3 minuti dopo il primo push
3. Svuota la cache del browser (Ctrl+F5)

### Il pulsante Admin non appare

1. Clicca esattamente 3 volte (non di più) nell'angolo in alto a destra
2. Se non funziona, ricarica la pagina e riprova

## 📄 Licenza

Questo progetto è stato creato per uso terapeutico personale.

⚠️ **Nota sulle Carte Dixit**: Le carte Dixit sono protette da copyright. Assicurati di avere il diritto di utilizzarle nel tuo contesto terapeutico.

## 👤 Autore

Guido - Parsec Cooperativa Sociale

---

## 🆘 Hai bisogno di aiuto?

Se hai problemi con il setup o l'utilizzo dell'app, puoi:

1. Controllare che tutti i passaggi di setup siano stati seguiti
2. Verificare la console del browser per eventuali errori (F12)
3. Assicurati che il repository sia pubblico e GitHub Pages sia attivo
