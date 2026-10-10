# Horizon Write

Horizon Write is a writing app for texts that must get the law and the rules right: opinions, memos, articles, course notes. You write on a page, and an AI checks every sentence against the law, rules and sources you choose, starting with Belgian VAT. Each finding shows the passage it rests on, and the app checks every answer of the AI before it shows it. Around the check is a full writing app: the page, your files, versions, import from Word and export to Word and PDF. It belongs to the Horizon suite, next to [Horizon](https://github.com/BartJanCoppens/Horizon) for presentations and [Horizon Calc](https://github.com/BartJanCoppens/Horizon-Calc-Releases) for spreadsheets.

It works on **Mac**, **Windows** and **Linux**. It's free and needs no account.

**[⬇ Download the latest version](https://github.com/BartJanCoppens/Horizon-Write-Releases/releases/latest)**

---

## 1. Download

Open the [latest release](https://github.com/BartJanCoppens/Horizon-Write-Releases/releases/latest), scroll down to **Assets** and click the file for your computer:

| Your computer | File to download |
|---|---|
| Mac with an Apple chip (M1, M2, M3, M4…) | `Horizon-Write-<version>-arm64.dmg` |
| Mac with an Intel processor | `Horizon-Write-<version>-x64.dmg` |
| Windows 10 or 11 | `Horizon-Write-Setup-<version>-x64.exe` |
| Linux (most distributions) | `Horizon-Write-<version>-x86_64.AppImage` |
| Linux (Ubuntu, Debian and similar, as a package) | `Horizon-Write-<version>-amd64.deb` |

Not sure which Mac you have? Click the Apple menu  › **About This Mac**. If it says **Chip: Apple M…**, take the Apple chip file; if it says **Processor: Intel**, take the Intel file.

You can ignore the other files (`.zip`, `.blockmap`, `.yml`): the app uses them for its updates.

## 2. Install

Horizon Write is made by one person for friends and family, so it isn't registered with Apple or Microsoft. Your computer will therefore warn you the first time you open it. That's expected; the steps below show how to get past the warning once.

### Mac

1. Open the `.dmg` file you downloaded.
2. Drag **Horizon Write** onto the **Applications** folder in the window that appears.
3. Open **Horizon Write** from your Applications folder (or with Spotlight).
4. macOS says it can't check Horizon Write for malicious software and won't open it. Click **Done** (or **OK**).
5. Open **System Settings** › **Privacy & Security**, scroll down to the message about Horizon Write and click **Open Anyway**. Confirm with your password or Touch ID, then click **Open Anyway** once more.

From then on Horizon Write opens normally. Needs macOS 12 (Monterey) or later.

### Windows

1. Double-click `Horizon-Write-Setup-<version>-x64.exe`.
2. If Windows shows **Windows protected your PC**, click **More info**, then **Run anyway**.
3. Horizon Write installs by itself (no administrator rights needed) and opens. You'll find it in the Start menu afterwards.

Needs Windows 10 or 11, 64-bit.

### Linux

**AppImage** (works on most distributions):

```sh
chmod +x Horizon-Write-*-x86_64.AppImage
./Horizon-Write-*-x86_64.AppImage
```

Or right-click the file › **Properties** › **Permissions**, tick **Allow executing file as program**, then double-click it. On Ubuntu 22.04 or later, if it doesn't start, install FUSE first: `sudo apt install libfuse2` (on Ubuntu 24.04: `sudo apt install libfuse2t64`).

**Debian package:**

```sh
sudo apt install ./Horizon-Write-*-amd64.deb
```

Horizon Write then appears in your applications menu.

## 3. Getting started

Horizon Write opens on an empty page: start typing. Along the top is a menu bar: **File**, **Edit**, **Format**, **Knowledge**, **Check**, **View** and **Help**. **Format** has headings, bold and italic, bulleted and numbered lists, and quotes, and the usual keys work (`⌘B`, `⌘I` and so on; on Windows and Linux, Ctrl instead of ⌘). Select some text and a small bar with the same formats appears just above it. The first heading is the document's title. **Edit › Find…** (`⌘F`) finds words in the text.

**Help › Open the example** opens a short sample tax opinion with a mistake of each kind, the quickest way to see the check at work.

- **Your files**: **File › Save** (`⌘S`) saves the document as a `.hwrite` file wherever you choose; double-click one to open it again. Horizon Write also keeps a draft of each document as you type, so closing the app or a crash loses nothing; **File › Unsaved drafts** opens the others.
- **Versions**: **File › Save a version…** (`⇧⌘S`) keeps the text as it is now under a name, and **File › Versions…** brings an earlier one back. Versions travel inside the saved file.
- **Word, Markdown and text**: **File › Import…** turns a Word (`.docx`), Markdown or text file into a new document, keeping headings, lists, bold, italic and quotes.
- **Sharing**: **File › Export to Word…** saves a `.docx`, and **File › Export to PDF…** a PDF of the page. **File › Export findings report** saves the check's findings as a web page or a spreadsheet.
- **Knowledge**: the **Knowledge** menu and the Knowledge panel (**View › Knowledge panel**) keep everything the check uses, each with a switch:
  - knowledge packs: **Add pack…**, with the Belgian VAT pack built in;
  - your own sources: PDF, Word or text documents read on your computer, web pages with passages you quote, and pasted passages;
  - the facts of your case (assumptions) and your own rules;
  - a vocabulary of allowed values, such as the VAT rates;
  - your definitions.

  All of it travels inside the saved file.
- **The check**: **Check › Check document** checks every sentence against the knowledge switched on, and **Check paragraph** the paragraph you're in. Each flagged sentence is underlined by what was found: contradicted, holds only if something is true, needs a definition, not backed yet, and more. **View › Findings panel** lists them, and `F8` goes to the next one. Right-click an underline to see the evidence and the rules it rests on, and to **Assume this**, **Accept anyway**, or let the AI suggest a better wording, add a missing condition or define a term. A safety point is saved before every change the AI makes, and **Edit › Undo AI update** takes it back.

**Help › Horizon Write Help** (`F1`) explains everything, with a page of keyboard shortcuts.

Your documents stay on your computer. Only the text you check goes to the AI you chose, with the knowledge switched on; with Ollama or LM Studio, nothing leaves your computer at all.

## 4. Connect an AI

The check needs an AI; without one, only the vocabulary of allowed values is checked. Connect one in **File › Models & keys…**: Claude, OpenAI, Gemini, OpenRouter, Mistral, Groq, DeepSeek, or models you run yourself with Ollama or LM Studio (no key; on this computer, nothing leaves it). **Get a key** opens the provider's page, **Add key…** stores it, and **Test** checks it. Keys are stored encrypted by your computer's keychain and only ever sent to their own provider.

## Updates

- **Windows** and **Linux AppImage**: new versions download in the background and install the next time you restart Horizon Write.
- **Mac** and **Linux .deb**: Horizon Write tells you when a new version is ready, with a **Download** button. Install it the same way as the first time.

## Uninstall

- **Mac**: drag **Horizon Write** from Applications to the Bin.
- **Windows**: **Settings › Apps › Installed apps**, find Horizon Write › **Uninstall**.
- **Linux**: delete the AppImage, or run `sudo apt remove horizon-write`.

## Questions or problems

Contact Bart Jan directly, or [open an issue](https://github.com/BartJanCoppens/Horizon-Write-Releases/issues) here.
