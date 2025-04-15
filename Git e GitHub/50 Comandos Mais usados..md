# 🧠 Comandos Git: Essenciais x Avançados

Este guia é dividido em duas partes:
- ✅ **30 Comandos Essenciais**: Para quem usa Git no dia a dia.
- 🚀 **20 Comandos Avançados/Opcionais**: Para quem quer ir além ou resolver situações específicas.

---

## ✅ 30 Comandos Git Essenciais

### 🔹 Inicialização e Configuração
```bash
git init                     # Cria um repositório Git
git config --global user.name "Seu Nome"
git config --global user.email "seu@email.com"
git config --list            # Lista as configurações atuais
```

### 🔹 Status e Histórico
```bash
git status                   # Verifica o status dos arquivos
git log                      # Mostra o histórico completo de commits
git log --oneline            # Histórico resumido (1 linha por commit)
git show                     # Detalhes do último commit
git diff                     # Diferença entre arquivos e último commit
```

### 🔹 Adicionando e Comitando
```bash
git add arquivo.txt          # Adiciona um arquivo específico
git add .                    # Adiciona todos os arquivos modificados
git commit -m "mensagem"     # Commit com mensagem
git commit -am "msg"         # Add + commit direto (arquivos já versionados)
```

### 🔹 Trabalhando com Repositório Remoto
```bash
git clone url                # Clona repositório remoto
git remote -v                # Mostra os repositórios remotos
git remote add origin url    # Adiciona um repositório remoto
git push -u origin main      # Envia commits para o repositório remoto
git pull                     # Puxa atualizações do remoto
```

### 🔹 Branches
```bash
git branch                   # Lista as branches locais
git branch nova-branch       # Cria uma nova branch
git checkout nome-da-branch  # Troca de branch
git checkout -b nova-branch  # Cria e troca para a nova branch
git merge nome-da-branch     # Mescla uma branch na atual
git branch -d nome-da-branch # Deleta uma branch local
```

### 🔹 Controle Simples de Erros
```bash
git reset arquivo.txt        # Remove da área de stage
git reset --soft HEAD~1      # Volta um commit, mantendo arquivos staged
git reset --hard             # Remove alterações não commitadas
git revert id-do-commit      # Cria um commit que desfaz o commit escolhido
```

---

## 🚀 20 Comandos Avançados / Menos Usados

### 🔹 Histórico e Debug
```bash
git reflog                   # Histórico de tudo (inclusive resets e commits "apagados")
git blame arquivo.txt        # Mostra quem editou cada linha do arquivo
git log --graph --oneline    # Histórico com gráfico de branches
```

### 🔹 Cherry-Pick e Tags
```bash
git cherry-pick id-do-commit # Aplica um commit específico em outra branch
git tag v1.0                 # Cria uma tag
git tag                     # Lista tags
git tag -d v1.0              # Deleta uma tag local
git push origin v1.0         # Envia uma tag para o repositório remoto
```

### 🔹 Stash (Salvar alterações temporárias)
```bash
git stash                    # Guarda alterações não commitadas
git stash list               # Lista os stashes salvos
git stash pop                # Aplica o último stash e remove da lista
git stash apply              # Aplica o stash sem remover
```

### 🔹 Limpeza
```bash
git clean -fd                # Remove arquivos/diretórios não rastreados
git clean -n                 # Simula o clean (mostra o que seria removido)
```

### 🔹 Rebase e Comparações
```bash
git rebase main              # Reescreve histórico colocando a branch atual após a main
git diff nome-da-branch      # Diferença entre a branch atual e outra
git fetch                    # Atualiza dados do remoto sem mesclar
```

### 🔹 Submódulos e Worktrees (avançado mesmo)
```bash
git submodule add url caminho   # Adiciona um repositório como submódulo
git worktree add caminho branch # Usa duas branches em pastas diferentes
```

---

## ✨ Dica final: Crie aliases para acelerar tudo!
```bash
git config --global alias.st status
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.cm "commit -m"
git config --global alias.last "log -1 HEAD"
```

---
