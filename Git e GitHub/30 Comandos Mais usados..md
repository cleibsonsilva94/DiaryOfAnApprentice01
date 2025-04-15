# 🧠 Comandos Git Essenciais para o Dia a Dia

Este guia traz os principais comandos do Git usados no dia a dia de desenvolvimento, organizados por categorias para facilitar a consulta. Ideal para iniciantes e também para quem quer relembrar comandos importantes! 🚀

---

## 📦 Inicialização e Configuração

```bash
git init
```
Cria um repositório Git vazio na pasta atual.

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seuemail@exemplo.com"
```
Configura seu nome e e-mail (usados nos commits).

```bash
git config --list
```
Mostra todas as configurações ativas do Git.

---

## 🔍 Status e Informações

```bash
git status
```
Mostra o status atual dos arquivos (modificados, não versionados etc.).

```bash
git log
```
Exibe o histórico de commits.

```bash
git log --oneline
```
Mostra o histórico de forma resumida (1 linha por commit).

```bash
git show
```
Mostra os detalhes de um commit (último por padrão).

```bash
git diff
```
Mostra as diferenças entre arquivos modificados e o último commit.

---

## 📥 Trabalhando com Repositórios Remotos

```bash
git clone url-do-repositorio
```
Clona um repositório remoto para sua máquina.

```bash
git remote -v
```
Lista os repositórios remotos conectados.

```bash
git remote add origin url
```
Conecta seu repositório local a um repositório remoto.

```bash
git push -u origin main
```
Envia seus commits para a branch `main` no repositório remoto e cria um vínculo.

```bash
git pull
```
Atualiza seu repositório local com mudanças do remoto.

---

## ✅ Adicionando e Comitando

```bash
git add arquivo.txt
```
Adiciona um arquivo específico para a área de stage.

```bash
git add .
```
Adiciona todos os arquivos modificados para o stage.

```bash
git commit -m "Mensagem do commit"
```
Registra as mudanças com uma mensagem.

```bash
git commit -am "Mensagem"
```
Adiciona e comita arquivos modificados já versionados (sem precisar de `git add`).

---

## 🌱 Branches

```bash
git branch
```
Lista todas as branches locais.

```bash
git branch nome-da-branch
```
Cria uma nova branch.

```bash
git checkout nome-da-branch
```
Troca para a branch indicada.

```bash
git checkout -b nome-da-branch
```
Cria e já troca para a nova branch.

```bash
git merge nome-da-branch
```
Une a branch especificada com a branch atual.

```bash
git branch -d nome-da-branch
```
Exclui a branch localmente (se já foi mesclada).

---

## 🧽 Reset, Revert e Reflog

```bash
git reset arquivo.txt
```
Remove o arquivo da área de stage.

```bash
git reset --hard
```
Descarta todas as alterações e volta ao último commit.

```bash
git reset --soft HEAD~1
```
Remove o último commit, mas mantém os arquivos no stage.

```bash
git revert id-do-commit
```
Cria um novo commit desfazendo as alterações de um commit específico.

```bash
git reflog
```
Lista todo o histórico de movimentações (inclusive commits "apagados").

---

## 🛠️ Outros Comandos Úteis

```bash
git stash
```
Salva temporariamente suas alterações e limpa o diretório.

```bash
git stash pop
```
Restaura as alterações salvas com `stash`.

```bash
git tag nome-da-tag
```
Cria uma tag no commit atual.

```bash
git clean -fd
```
Remove arquivos não rastreados do diretório (atenção: é irreversível!).

```bash
git cherry-pick id-do-commit
```
Aplica um commit específico de outra branch na branch atual.

```bash
git blame arquivo.txt
```
Mostra linha por linha quem alterou o quê em um arquivo.

---

## ✨ Dica Extra: Histórico Resumido e Visual

```bash
git log --oneline --graph --all
```
Exibe o histórico completo com ramificações em formato de gráfico.

---

Com esses comandos, você tem uma base sólida para trabalhar com Git no dia a dia! 💻
