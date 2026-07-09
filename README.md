# Projeto teste

### Monta um fluxo de trabalho no GitHub.
### Esse fluxo se chama GitHub Flow.
### E é usado por muitas empresas de software.

- Cria a tela de login
- Cria a tela de cadastro

--
## **  O fluxo de trabalho no dia a dia (passo a passo)**

1. Imagine que você que criar a funcionalidade de esqueci minha senha no projeto:
2. Você entra na branch develop e baixa as ultimas atualizações (git pull):
3. Você cria uma nova branch a partir dela (git checkout -b feature/esqueci-senha):
4. Você escreve o código do PHP, o HTML e a documentação dessa funcionalidade nessa branch:
5. Terminou? Você envia essas alterações para o GitHub e abre um PullRequest(PR) pedindo para juntar (merge) sua feature/esqueci-senha dentro da develop:
6. O código é revisado por outro DEV (ou por você mesmo) e o merge é feito. A branch feature/esqueci-senha é deletada para manter o repositório limpo:

--
**********************************************************************************************

### Passo 1: Garantir que sua branch `develop` está atualizada

Antes de começar qualquer código novo, você deve puxar as últimas alterações que seus colegas de equipe enviaram para o servidor.

```bash
# Vai para a branch de desenvolvimento
git checkout develop

# Baixa as novidades do GitHub para o seu computador
git pull origin develop

```

---

### Passo 2: Criar a branch para a sua funcionalidade (Feature)

Agora que você está atualizado, cria uma branch temporária usando o prefixo `feature/`.

```bash
# Cria e já muda para a nova branch
git checkout -b feature/tela-perfil

```

---

### Passo 3: Trabalhar no código e na documentação

Neste momento, você abre o VS Code (ou seu editor de preferência), altera seus arquivos `.php` e **também atualiza o `README.md**` explicando a nova tela.

Depois de salvar os arquivos, você faz o commit:

```bash
# Verifica quais arquivos foram alterados
git status

# Adiciona todas as alterações (código + documentação) para o "pacote"
git add .

# Registra a alteração com uma mensagem clara
git commit -m "feat: adiciona tela de perfil e atualiza instruções no README"

```

---
### Passo 4: Enviar a branch para o GitHub

Sua branch só existe na sua máquina por enquanto. Você precisa enviá-la para o servidor do GitHub.

```bash
# Envia a branch para o repositório remoto
git push origin feature/tela-perfil

```

---

### Passo 5: O Pull Request (Feito no site do GitHub)

Agora você sai do terminal e vai para a interface web do GitHub:

1. O próprio GitHub mostrará um botão amarelo escrito **"Compare & pull request"**. Clique nele.
2. Certifique-se de que a base do lado esquerdo é **`develop`** e a sua branch à direita é **`feature/tela-perfil`**.
3. Escreva o que foi feito e clique em **"Create pull request"**.

---

### Passo 6: Finalizar e limpar o ambiente (Pós-Merge)

Depois que você (ou seu líder técnico) revisou o código e clicou em **"Merge pull request"** lá no site do GitHub, aquela funcionalidade já faz parte da branch `develop`.

Agora você limpa o seu computador para começar a próxima tarefa:

```bash
# Volta para a develop local
git checkout develop

# Baixa o seu próprio código que acabou de ser fundido lá no GitHub
git pull origin develop

# Deleta a branch local que você usou, já que ela não é mais necessária
git branch -d feature/tela-perfil
