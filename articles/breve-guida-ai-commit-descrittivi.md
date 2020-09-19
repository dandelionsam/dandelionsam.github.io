# Breve guida ai commit descrittivi
💻 `git commit`, invio.

Ed è qui che il **terrore** ed il **panico** cominciano ad instradarsi nella nostra mente, dopo aver digitato questi caratteri sul nostro scuro terminale.

Quante volte la difficoltà di scrivere quello snippet di codice e di averlo fatto funzionare come si deve, viene **sormontata** dalla complessità di *indicare per iscritto* quello che abbiamo appena realizzato?

Per fortuna, nel vasto e *comprensivo* mondo degli sviluppatori, qualcuno ha pensato bene di architettare una **convenzione** che cerchi di risolvere questo annoso problema: [**Conventional Commits**](https://www.conventionalcommits.org/en/v1.0.0/).

Nel loro sito possiamo leggere: 

> La specifica Conventional Commits è una convenzione riguardante i
> messaggi di commit usati dai VCS che fornisce una serie di semplici
> regole per creare una storia dei commit esplicita, che ne facilita la
> prima lettura e la creazione di strumenti automatici per la loro
> gestione.

E continuando, sotto:

> La convenzione, si sposa con [SemVer](http://semver.org/) nel
> descrivere le feature, i fix e i cambiamenti effettuati attraverso i
> messaggi di commit.

## 🔧 Come funziona?

Conventional Commits prevede la creazione di messaggi di commit, composti seguendo le **regole** e le **strutture** che ci vengono messe a disposizione. Il messaggio standard è composto così: `<type>[optional scope]: <description>`. 

I messaggi inoltre possono essere seguiti, **opzionalmente**, da un `[body]` e da un `[footer]`.

### In dettaglio

Se andiamo a sbirciare su [@angular/angular](https://github.com/angular/angular/blob/master/.pullapprove.yml), possiamo vedere qualche esempio concreto. Oltre a ciò, [questo documento 📄](https://docs.google.com/document/d/1QrDFcIiPjSLDn3EL15IJygNPiHORgU1_OOAqWjiDU5Y/edit#) descrive come sono cambiati nel tempo i loro commit e come il team di Angular si sia conformato ad una **specifica comune**. 

Se ho appena risolto un bug che non mi permetteva di visualizzare correttamente un input, potrei scrivere: `fix(ui): input in MainView`.

## 📕 Type di base: le regole, quelle semplici

La convenzione prevede tre `type` principali che sono: 

 - `feat`, usato per descrivere l'aggiunta di nuove funzionalità
 - `fix`, usato per comunicare il fix di bug o di errori
 - `BREAKING CHANGE`, usato per avvertire che sono stati effettuati cambiamenti che potrebbero causare incompatibilità con versioni precedenti

Oltre questi tre, ci vengono indicati **altri** `type` come descritto su [@commitlint/config-conventional](https://github.com/conventional-changelog/commitlint/tree/master/%40commitlint/config-conventional).

## 📘 Millemila altri type: quando_il_gioco_si_fa_duro...
Su @commitlint/config-conventional, oltre ai tre principali descritti sopra, possiamo trovare i seguenti tipi: `build`, `ci`, `chore`, `docs`, `perf`, `refactor`, `revert`,  `style` e `test`.

Di questi però, nonostante alcuni siano **autoesplicativi**, non viene fornita *nessuna descrizione specifica* sul sito di Conventional Commits. Con l'aiuto di un browser e armati di pazienza, possiamo andarle a recuperare tutte qui e lì in giro per il web.

## 📖 Esplicitazioni: ...{ i_duri_cominciano_a_giocare }
Ecco quindi la descrizione di ogni singolo type:


-   `build`: cambiamenti effettuati sui sistemi di build o sulle dipendenze esterne (ad esempio: **gulp**, **broccoli**, **npm**)
- `chore*`: cambiamenti alle task di **Grunt**
-   `ci`: cambiamenti effettuati sulle configurazioni o sugli script di *continuous integration* (ad esempio: **Circle**, **BrowserStack**, **SauceLabs**)
- `docs`: cambiamenti effettuati sulla documentazione
- `feat`: aggiunta di nuove feature
- `fix`: bug fix
- `perf`: cambiamenti per il miglioramento delle performance;
- `refactor`: cambiamenti al codice che non rientrano in `fix` o `feat`
- `revert`: ripristino di uno stato precedente del commit
- `style*`: cambiamenti che non influenzano il significato del codice (spazi bianchi, formattazione, punti e virgola)
- `test*`: aggiunta di test o correzione di quelli già esistenti

Le voci che presentano un asterisco prevedono che **non** vengano effettuati cambiamenti *esecutivi* al codice sorgente o al suo significato.

Chiaramente, se il progetto su cui si sta lavorando non è particolarmente complesso e/o non si attiene ad alcuni di questi parametri, possiamo anche non utilizzarli tutti.

## ❓ Perchè dovremmo usarli: semplificazione
Giunti a questo punto, la domanda sorge quasi spontaneamente: **perchè devo complicare ancora di più la mia vita?**. 

Fondamentalmente è vero: questo modo di scrivere i commit aggiunge un mini layer di **astrazione** in più rispetto ad essere liberi di scrivere quello che ci pare.

Dobbiamo attenerci a delle regole, e per attenerci alle regole dobbiamo prima conoscerle.

✅ È vero altresì che, superato questo piccolo scoglio iniziale, i vantaggi di questo sistema sono pressochè **insostituibili**: guadagneremo un **incredibile chiarezza** nei nostri messaggi, avremo la possibilità di **automazione** e sicuramente **perderemo meno tempo** e ci spremeremo meno le meningi nello scrivere i messaggi stessi.

## 🔎 Referenze
[Conventional Commits](https://www.conventionalcommits.org/)

[Semantic Commit Messages](https://seesparkbox.com/foundry/semantic_commit_messages)

[Karma Git Commit Msg](http://karma-runner.github.io/1.0/dev/git-commit-msg.html)


