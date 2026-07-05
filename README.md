# Portable Emacs Configuration

My personal Emacs configuration starting point. Designed to be clean, modular, and portable across machines.

## Features & Package Integrations
*   **Git Interface:** Integrated via [Magit](https://magit.vc/) (`C-x g` to open status).
*   **Version Manager:** Integrated via `asdf-vm` to automatically load local runtime toolpaths.
*   **LSP Client:** Powered by the built-in `eglot` client.
*   **Completions:** Interactive buffer completions using `Corfu` and minibuffer search using `Vertico`, `Consult`, and `Orderless`.
*   **Syntax Highlighting:** Enhanced syntax parsing via built-in Tree-sitter using `treesit-auto`.

---

## Prerequisites (External Binaries)

For this configuration to work properly on a new machine, ensure the following tools are installed on your host system:

1.  **C Compiler & Toolchain (`gcc` / `make`):** Required by `treesit-auto` to automatically compile language-specific Tree-sitter grammars.
2.  **asdf version manager:** Required by `asdf-vm` to dynamically resolve your runtime shims.
3.  **GNU Coreutils (`gls`):** Required on macOS for clean Dired buffer listings (falls back to native ls if missing).
4.  **Language Servers (for LSP support):**
    *   `gopls` (Go support)
    *   `rust-analyzer` (Rust support)

---

## Installation on a New Machine

1.  **Clone the Repository:**
    Clone this repository directly into your Emacs configuration directory:
    ```bash
    git clone https://github.com/jalvarezsamayoa/emacs-dotfiles.git ~/.emacs.d
    ```

2.  **Launch Emacs:**
    Open Emacs. It will automatically detect missing packages and download/install them via `use-package` on startup.
