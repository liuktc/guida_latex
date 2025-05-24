# **Guida semplice a LaTeX & Overleaf per la tua tesi 😃**

Ehi, studente di Medicina della Sapienza! Questa guida è fatta apposta per te, anche se è la prima volta che senti parlare di LaTeX 😉  
Ti aiuterà a creare una tesi ordinata, professionale e a prova di relatore!

---

## 📚 **Indice dei contenuti**

1. [Perché scegliere LaTeX](#1-perché-latex)
   - [Differenza tra LaTeX e Word](#11-differenza-fra-latex-e-word)
2. [Overleaf: l’editor online](#2-overleaf-l’editor-online)
   - [Interfaccia Overleaf](#21-interfaccia-overleaf)
3. [Struttura base del progetto](#3-struttura-base-del-progetto)
4. [Il tuo primo file `.tex`](#4-il-tuo-primo-tex-minimale)
5. [Capitoli, sezioni e sottosezioni](#5-capitoli-sezioni-e-sottosezioni)
6. [Inserire figure](#6-inserire-figure-🎨)
7. [Tabelle](#7-tabelle-📊)
8. [Liste puntate e numerate](#8-liste-puntate-e-numerate-📝)
9. [Bibliografia e citazioni](#9-bibliografia-e-citazioni-📚)
10. [Consigli pratici](#10-tips--trucchetti-🔍)

---

## 1. Perché LaTeX?

✅ **Aspetto professionale**  
✅ **Automazione totale** di numeri di pagina, bibliografia, riferimenti  
✅ **Stabilità**: niente formattazioni che “saltano” all’ultimo minuto

Con LaTeX scrivi un file `.tex` (come un file di testo), e lui genera per te un PDF elegantissimo.

### 1.1 Differenza fra LaTeX e Word

| Word                             | LaTeX                                                  |
| -------------------------------- | ------------------------------------------------------ |
| "What You See Is What You Get"   | "What You Mean Is What You Get"                        |
| Impagini a mano                  | Impagini con regole automatiche                        |
| Facile da iniziare               | Più difficile all’inizio, ma potente sul lungo termine |
| Rischio di impaginazione caotica | Layout sempre pulito e professionale                   |

---

## 2. Overleaf: l’editor online

Overleaf ti permette di usare LaTeX senza installare nulla.

### Come iniziare:

1. Vai su [overleaf.com](https://www.overleaf.com)
2. Registrati (puoi usare l'email Sapienza, ma anche una qualsiasi)
3. Clicca su "New Project" > "Blank Project" oppure **usa il template Sapienza** 👉 [INSERISCI LINK AL TEMPLATE]

Nel progetto troverai:

- `main.tex`: il tuo documento principale
- `bibliography.bib`: la tua bibliografia
- `images/`: la cartella per le immagini

> 🧠 Ogni salvataggio ricompila automaticamente il tuo PDF!

### 2.1 Interfaccia Overleaf

![interfaccia overleaf](overleaf.png)

- 📁 **A sinistra**: tutti i file del progetto
- ✏️ **Al centro**: l’editor dove scrivi il tuo `.tex`
- 📄 **A destra**: l’anteprima del tuo PDF

**PRO TIP**: Usa `Ctrl + S` per compilare velocemente!

---

## 3. Il tuo primo file `.tex` minimale

```latex
\documentclass[12pt,a4paper]{report}
\usepackage[utf8]{inputenc}
\usepackage[T1]{fontenc}
\usepackage[italian]{babel}
\usepackage{graphicx}
\usepackage{biblatex}
\addbibresource{bibliography.bib}

\title{Titolo della tua Tesi}
\author{Il tuo Nome}
\date{Mese Anno}

\begin{document}
\maketitle
\tableofcontents

\chapter{Introduzione}
Qui ci va il tuo testo iniziale...

\chapter{Materiali e Metodi}
Descrivi esperimenti, protocolli, ecc.

\printbibliography
\end{document}
```

Spiegazione rapida:

- Tutti i comandi iniziano con `\`, poi il nome del comando e le parentesi graffe `{}` per i parametri. Esempi:
  - `\title{Titolo della tua Tesi}` imposta il titolo.
  - `\documentclass{}` definisce il tipo di documento (qui un report).
  - `\usepackage{}` importa pacchetti utili (come `graphicx` per le immagini).
  - `\maketitle` genera la pagina del titolo.
  - `\tableofcontents` crea l'indice automatico.
  - `\printbibliography` stampa la bibliografia.

## 4. Capitoli, sezioni e sottosezioni

Organizza bene il tuo testo!

```latex
\chapter{Introduzione}
\section{Obiettivi dello studio}
\subsection{Contesto clinico}
```

## 5. Inserire figure 🎨

```latex
\begin{figure}[h]
    \centering
    \includegraphics[width=0.6\textwidth]{images/tuafoto.png}
    \caption{Descrizione della figura}
    \label{fig:esperimento}
\end{figure}
```

📌 Note utili:

- La figura deve essere nella cartella `images/`
- Richiama la figura nel testo con Figura `\ref{fig:esperimento}` (in questo modo se cambi il numero della figura, si aggiorna automaticamente).

## 6. Liste puntate e numerate 📝

### Liste puntate

```latex
\begin{itemize}
    \item Primo punto
    \item Secondo punto
    \item Terzo punto
\end{itemize}
```

### Liste numerate

```latex
\begin{enumerate}
    \item Primo punto numerato
    \item Secondo punto numerato
    \item Terzo punto numerato
\end{enumerate}
```

## 7. Bibliografia e citazioni 📚

1. Crea un file bibliography.bib
2. Aggiungi una fonte in formato BibTeX:

```bibtex
@article{rossi2020,
  author = {Rossi, Mario},
  title  = {Studio del microbiota},
  journal= {Giornale Medico},
  year   = {2020}
}
```

3. Cita nel testo con `\cite{rossi2020}`
4. Alla fine del documento, inserisci `\printbibliography`

## 8. Tips & Trucchetti 🔍

✅ Riferimenti automatici
Usa `\label{}` e `\ref{}` per citare figure, capitoli, sezioni ecc.

✅ Compila spesso
Errori? Overleaf te li segnala in tempo reale!

✅ Struttura i file per capitoli
Mantieni tutto ordinato: ogni capitolo in un file `.tex` diverso.

✅ Git e collaborazione
Overleaf integra Git, utile se lavori in gruppo.

✅ Commenta il codice
Usa `%` per lasciare note a te stesso, es. `% Qui inizia il capitolo 2`

# 🎉 Buon lavoro!

Scrivere una tesi con LaTeX è una sfida, ma ti dà un controllo totale e un risultato elegante.
Buona scrittura e... in bocca al lupo! 🍀
