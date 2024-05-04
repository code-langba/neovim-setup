# Neovim setup

Process of setting up [Neovim](https://github.com/neovim/neovim) with [NvChad](https://nvchad.com/) on Windows.

## Contents

1. [Prerequisites](#prerequisites)
2. [Installation](#installation)
3. [Post Installation](#post-installation)
4. [Useful bindings](#useful-bindings)
5. [Additional](#additional)

## <div id="prerequisites">Prerequisites [🔝](#contents)</div>

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

## <div id="installation">Installation [🔝](#contents)</div>

- Install Neovim

```
choco install neovim -y
```

- Setup NvChad

```
git clone https://github.com/code-langba/neovim-setup $ENV:USERPROFILE\AppData\Local\nvim
nvim
```

## <div id="post-installation">Post installation [🔝](#contents)</div>

- After installing all the plugins, install some lsp servers within neovim for autocompletion.

```
MasonInstall typescript-language-server css-lsp html-lsp lua-language-server tailwindcss-language-server stylua lua-language-server prettier
```

- Now install some treesitter parsers for syntax highlighting

```
TSInstall tsx javascript typescript
```

## <div id="useful-bindings">Useful bindings [🔝](#contents)</div>

- space + ch for cheatsheet
- space + ff find files within project
- space + fa find
- space + fw grep words

## <div id="additional">Additional [🔝](#contents)</div>

🐞 Some solutions if things don't work.

- if lsp servers are not working properly, try

```
npm i -g typescript-language-server typescript vscode-langservers-extracted @tailwindcss/language-server
```
