# 🛠️ Configurando

Este tutorial tem como objetivo ajudar você a deixar sua máquina pronta para programar, desde a instalação do Git até a criação de aliases úteis no terminal. Ideal para quem está iniciando em uma nova empresa ou projeto! 🚀

---

## ✅ 1. Instalando o Git (caso não esteja instalado)

### 🔹 Windows

1. Acesse: [https://git-scm.com](https://git-scm.com) [https://git-scm.com]([https://git-scm.com](https://git-scm.com/downloads/win)) 
2. Baixe o instalador e siga os passos padrão da instalação.
3. Após instalar, abra o terminal (CMD ou PowerShell) e digite:

```bash
git --version
```

Se aparecer a versão do Git, está tudo certo!

---

## ✅ 2. Configurando o Git pela primeira vez

Abra o terminal e configure seu nome e e-mail (serão usados nos commits):

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seuemail@exemplo.com"
```

Para verificar todas as configurações do Git:

```bash
git config --list
```

---

## ✅ 3. Criando Aliases (apelidos) para comandos do Git

Isso vai economizar tempo com comandos repetitivos. Veja alguns exemplos de aliases úteis:

```bash
git config --global alias.st status
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.cm "commit -m"
git config --global alias.last "log -1 HEAD"
```

Depois disso, você poderá usar comandos como:

```bash
git st
git co nome-da-branch
git cm "mensagem do commit"
```

---

## ✅ 4. Criando Aliases do Terminal

Se estiver usando **Git Bash**, **PowerShell** ou **WSL**, é possível criar aliases para facilitar o uso diário do terminal.

---

### 🔹 Para Git Bash ou WSL (Linux)

1. Abra o terminal
2. Edite o arquivo `.bashrc` (ou `.zshrc` se estiver usando o zsh):

```bash
nano ~/.bashrc
```

3. Adicione os aliases desejados:

```bash
alias gs='git status'
alias gc='git commit -m'
alias gp='git push'
alias c='clear'
```

4. Salve o arquivo e atualize o terminal com:

```bash
source ~/.bashrc
```

---

### 🔹 Para PowerShell (Windows)

1. Crie ou edite o seu arquivo de perfil com o comando:

```powershell
notepad $PROFILE
```

2. Adicione os seguintes aliases:

```powershell
Set-Alias gs git status
Set-Alias gc git commit
Set-Alias gp git push
Function cls {Clear-Host}
```

---

Pronto! Agora sua máquina está configurada com Git e atalhos no terminal para facilitar seu dia a dia como dev! ✨


# 🐧Linux


---

## ✅ 1. Instalando o Git

Abra o terminal e execute:

### 🔹 Debian, Ubuntu e derivados:

```bash
sudo apt update
sudo apt install git -y
```

### 🔹 Fedora:

```bash
sudo dnf install git -y
```

### 🔹 Arch Linux:

```bash
sudo pacman -S git
```

Verifique a instalação:

```bash
git --version
```

---

## ✅ 2. Configurando o Git pela primeira vez

Defina o nome e o e-mail que serão usados nos commits:

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seuemail@exemplo.com"
```

Para verificar todas as configurações:

```bash
git config --list
```

---

## ✅ 3. Criando Aliases (apelidos) para comandos do Git

Economize tempo com comandos personalizados:

```bash
git config --global alias.st status
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.cm "commit -m"
git config --global alias.last "log -1 HEAD"
```

Uso rápido:

```bash
git st
git co nome-da-branch
git cm "mensagem do commit"
```

---

## ✅ 4. Criando Aliases do Terminal

### 🔹 Para Bash

1. Edite o arquivo `.bashrc`:

```bash
nano ~/.bashrc
```

2. Adicione ao final do arquivo:

```bash
alias gs='git status'
alias gc='git commit -m'
alias gp='git push'
alias c='clear'
```

3. Salve com `Ctrl + O`, depois `Enter` e saia com `Ctrl + X`.

4. Recarregue o terminal:

```bash
source ~/.bashrc
```

---

### 🔹 Para Zsh

Se estiver usando o Zsh (Oh My Zsh, por exemplo), edite o `.zshrc`:

```bash
nano ~/.zshrc
```

Adicione os mesmos aliases:

```bash
alias gs='git status'
alias gc='git commit -m'
alias gp='git push'
alias c='clear'
```

Salve e recarregue:

```bash
source ~/.zshrc
```

---
