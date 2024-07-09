## 10 comandos git

1. **`git clone <url-do-repositório>`**

   Esse comando copia um repositório da nuvem para sua máquina local.

2. **`git add <nome-do-arquivo>`**  
   **`git add .`** (Adiciona todos os arquivos modificados)

   Os comandos acima adicionam um arquivo específico que foi modificado ou todas as modificações de um projeto (o que pode incluir mais de um arquivo) a um "envelope" antes de serem comitados ou "etiquetados". É como se você colocasse suas modificações em um "envelope" mas não o lacrasse ainda.

3. **`git commit -m "Mensagem do commit"`**

   Com esse comando, você salva uma alteração feita (ou várias) "lacrando o envelope" e coloca uma etiqueta nele. Nessa "etiqueta" você coloca uma breve descrição do que foi modificado.

4. **`git status`**

   Indica os arquivos que foram modificados ou estão adicionados ao "envelope", mas ainda não comitados ou "etiquetados".

5. **`git log`**

   Mostra a lista de commits ("envelopes lacrados").

6. **`git pull <nome-remoto> <nome-branch>`**

   Você traz para sua máquina local todos os commits de um repositório remoto.

7. **`git push <nome-remoto> <nome-branch>`**

   Envia os commits ("os envelopes") para o repositório remoto.

8. **`git branch`** (Lista branches)  
   **`git branch <nome>`** (Cria um novo branch)  
   **`git branch -d <nome>`** (Deleta um branch)

   Lista, cria ou exclui branches.

   E vá por mim, você usará muito as branches no seu dia a dia. Elas são ramificações do código principal.

9. **`git stash`**

   Você guarda temporariamente modificações em uma gaveta, por assim dizer. No vídeo, no minuto (), eu mostro um uso prático desse comando.

10. **`git checkout <nome-do-branch>`**

   Usado para caminhar entre as branches.

Existem muitos outros comandos que você aprenderá com o tempo, e o ideal é que você tenha anotado todos os comandos a fim de sempre recorrer a eles quando precisar. No vídeo abaixo, eu mostro como utilizar cada um dos comandos acima :)

Vídeo:
