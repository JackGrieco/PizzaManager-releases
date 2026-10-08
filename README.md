# PizzaManager — download

Gestore di sessioni di terminale in schede: shell, [Claude Code](https://claude.com/claude-code),
[Codex](https://developers.openai.com/codex/cli/), [OpenCode](https://opencode.ai).
Ogni sessione è un terminale vero, e su macOS e Linux sopravvive alla chiusura
dell'app.

**Qui ci sono solo i pacchetti scaricabili.** Il codice è in un repository
privato: questo repo esiste perché i link di download funzionino per chiunque.

## Scarica

| | | |
|---|---|---|
| **macOS** | [Apple Silicon (.dmg)](../../releases/latest/download/PizzaManager-mac-arm64.dmg) · [Intel (.dmg)](../../releases/latest/download/PizzaManager-mac-x64.dmg) | Trascina l'app in *Applicazioni* |
| **Linux** | [AppImage](../../releases/latest/download/PizzaManager-linux-x86_64.AppImage) · [.deb](../../releases/latest/download/PizzaManager-linux-amd64.deb) | `chmod +x` l'AppImage, o `sudo dpkg -i` il .deb |
| **Windows** | [Installer (.exe)](../../releases/latest/download/PizzaManager-win-x64-setup.exe) | Installer classico |

Tutte le versioni, con le note di ogni rilascio: [Releases](../../releases).

## Alla prima apertura

- **macOS**: niente da fare. Il `.dmg` è firmato con un Developer ID e
  notarizzato da Apple, quindi si apre come qualsiasi app scaricata.
- **Linux**: niente da fare.
- **Windows**: il pacchetto non è firmato e compare l'avviso SmartScreen —
  *Ulteriori informazioni → Esegui comunque*.

## Cosa serve

Le CLI degli assistenti (`claude`, `codex`, `opencode`) si installano a parte:
l'app lancia quelle che trova nel `PATH`.

Su macOS e Linux, con [`tmux`](https://github.com/tmux/tmux) installato le
sessioni vivono fuori dall'app: chiudere la finestra è uno stacco, e alla
riapertura le schede tornano dov'erano. Senza `tmux` — e su Windows, dove non
esiste — i processi si chiudono con l'app.
