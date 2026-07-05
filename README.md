# Portable Emacs Configuration

My personal Emacs configuration starting point. Designed to be clean, modular, and portable across machines.

## Features & Package Integrations
*   **Git Interface:** Integrated via [Magit](https://magit.vc/) (`C-x g` to open status).
*   **Version Manager:** Integrated via `asdf-vm` to automatically load local runtime toolpaths.
*   **LSP Client:** Powered by the built-in `eglot` client.
*   **Auto-Formatting:** Powered by `apheleia` for asynchronous format-on-save.
*   **Completions:** Interactive buffer completions using `Corfu` and minibuffer search using `Vertico`, `Consult`, and `Orderless`.
*   **Syntax Highlighting:** Enhanced syntax parsing via built-in Tree-sitter using `treesit-auto`.
*   **Ruby on Rails Environment:** MVC-aware navigation with `projectile-rails`, interactive testing via `rspec-mode`, and REPL support via `inf-ruby`.
*   **JavaScript/TypeScript:** Full IDE capabilities for JS, TS, and React (JSX/TSX) using native Tree-sitter modes.
*   **JSON:** Structural validation and schema-aware completions via `json-ts-mode`.
*   **Search & Replace:** Fast, project-wide fuzzy searching with `consult-ripgrep` and mass-editing via `wgrep`.

---

## Prerequisites (External Binaries)

For this configuration to work properly on a new machine, ensure the following tools are installed on your host system:

1.  **C Compiler & Toolchain (`gcc` / `make`):** Required by `treesit-auto` to automatically compile language-specific Tree-sitter grammars.
2.  **asdf version manager:** Required by `asdf-vm` to dynamically resolve your runtime shims.
3.  **GNU Coreutils (`gls`):** Required on macOS for clean Dired buffer listings (falls back to native ls if missing).
4.  **ripgrep (`rg`):** Required for fast project-wide search via `consult-ripgrep`.
4.  **Formatters (for Apheleia):**
    *   `ruff` or `black` (for Python formatting)
    *   `rubocop` (for Ruby formatting)
    *   `prettier` (for JS/TS/React formatting)
    *   `gofmt` (built-in with Go)
    *   `rustfmt` (built-in with Rust)
5.  **Language Servers (for Eglot LSP support):**
    *   `gopls` (Go support)
    *   `rust-analyzer` (Rust support)
    *   `pyright` or `pylsp` (Python support)
    *   `ruby-lsp` (or `solargraph` for Ruby support)
    *   `yaml-language-server` (YAML support)
    *   `typescript-language-server` (JS/TS/React support)
    *   `vscode-langservers-extracted` (JSON schema and validation support)

---

## Installation on a New Machine

1.  **Clone the Repository:**
    Clone this repository directly into your Emacs configuration directory:
    ```bash
    git clone https://github.com/jalvarezsamayoa/emacs-dotfiles.git ~/.emacs.d
    ```

2.  **Launch Emacs:**
    Open Emacs. It will automatically detect missing packages and download/install them via `use-package` on startup.
