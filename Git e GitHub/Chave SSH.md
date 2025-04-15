# 🔐 Configurando Chaves SSH no GitHub

Este guia ensina como configurar chaves SSH no GitHub para clonar, enviar (push) e puxar (pull) repositórios com mais segurança e praticidade.

---

## ✅ O que será feito:

1. Verificar se já existe uma chave SSH
2. Gerar uma nova chave SSH (caso necessário)
3. Adicionar a chave ao agente SSH
4. Adicionar a chave ao GitHub
5. Testar a conexão

---

## 🧰 Pré-requisitos

- Git instalado na máquina
- Conta no GitHub
- Terminal ou Git Bash

---

## 1️⃣ Verificar se já existe uma chave SSH

```bash
ls -al ~/.ssh
```

Se aparecer arquivos como `id_rsa` ou `id_ed25519`, você já possui uma chave.

---

## 2️⃣ Gerar uma nova chave SSH

```bash
ssh-keygen -t ed25519 -C "seu-email@example.com"
```

> Caso seu sistema não suporte ed25519:
> 
> ```bash
> ssh-keygen -t rsa -b 4096 -C "seu-email@example.com"
> ```

Pressione **Enter** para aceitar o caminho padrão e depois **Enter** novamente para senha (pode deixar em branco se preferir).

---

## 3️⃣ Adicionar a chave ao agente SSH

Inicie o ssh-agent:

```bash
eval "$(ssh-agent -s)"
```

Adicione a chave ao agente:

```bash
ssh-add ~/.ssh/id_ed25519
```

> Substitua `id_ed25519` pelo nome da sua chave, se for diferente.

---

## 4️⃣ Adicionar a chave pública ao GitHub

Copie a chave pública:

```bash
cat ~/.ssh/id_ed25519.pub
```

1. Acesse: [https://github.com](https://github.com)
2. Vá em **Settings > SSH and GPG keys**
3. Clique em **New SSH key**
4. Cole a chave no campo “Key” e adicione um título
5. Clique em **Add SSH key**

---

## 5️⃣ Testar a conexão com o GitHub

```bash
ssh -T git@github.com
```

Se tudo estiver certo, verá a mensagem:

```
Hi seu-usuario! You've successfully authenticated, but GitHub does not provide shell access.
```

---

## 🚀 Usar SSH nos repositórios

Ao clonar um repositório, use o link SSH (e não o HTTPS):

```bash
git clone git@github.com:seu-usuario/seu-repositorio.git
```

---

Feito com 💻 para quem quer facilitar a vida no GitHub.
