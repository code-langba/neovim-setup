# Neovim setup

Process of setting up [Neovim](https://github.com/neovim/neovim) with [NvChad](https://nvchad.com/) on Windows.

## Contents

1. [Prerequisites](#prerequisites)
2. [Installation](#installation)
3. [Post Installation](#post-installation)
4. [Useful bindings](#useful-bindings)

## Prerequisites [🔝](#contents)

Things you'll need:

- chocolatey

```powershell
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```

- Mingw - C compiler

```
choco install mingw -y
```

- make

```
choco install make -y
```

- tree-sitter

```
choco install tree-sitter -y
```

- ripgrep

```
choco install ripgrep -y
```

## Installation

- Install Neovim

```
choco install neovim -y
```

- Setup NvChad

```
git clone https://github.com/code-langba/neovim-setup $ENV:USERPROFILE\AppData\Local\nvim
nvim
```

## <a href="#post-installation">Post installation</a> [🔝](#contents)

- After installing all the plugins, install some lsp servers within neovim for autocompletion.

```
MasonInstall typescript-language-server css-lsp html-lsp lua-language-server tailwindcss-language-server stylua lua-language-server prettier
```

- Now install some treesitter parsers for syntax highlighting

```
TSInstall tsx javascript typescript
```

## Useful bindings [🔝](#contents)

- space + ch for cheatsheet
- space + ff find files within project
- space + fa find
- space + fw grep words

## Additional [🔝](#contents)

🐞 Some solutions if things don't work.

- if lsp servers are not working properly, try

```
npm i -g typescript-language-server typescript vscode-langservers-extracted @tailwindcss/language-server
```
