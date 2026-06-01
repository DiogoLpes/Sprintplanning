# 📖 Guia: Como Colocar o Sprint Planning no GitHub Pages

Segue este passo a passo para partilhar o teu Kanban board com os amigos no Discord!

---

## **Passo 1: Cria um Repositório no GitHub**

1. Vai para [github.com](https://github.com) e faz login
2. Clica no **botão `+`** no canto superior direito
3. Seleciona **"New repository"**
4. Preenche:
   - **Repository name**: `sprintplanning` (ou outro nome)
   - **Description**: "Sprint Planning Kanban Board - Integra-te Project"
   - **Public** (importante! senão não funciona no Pages)
   - **Initialize with README** (deixa marcado)
5. Clica **"Create repository"**

---

## **Passo 2: Envia o Ficheiro para o Repositório**

### Option A: Pelo GitHub Web (Mais Fácil)

1. No repositório que criaste, clica no botão **"Add file"** → **"Upload files"**
2. Arrasta o ficheiro `sque.html` para a zona de upload
3. Renomeia o ficheiro para **`index.html`** (importante!)
   - Clica no nome do ficheiro
   - Muda de `sque.html` para `index.html`
4. Em baixo, escreve uma mensagem de commit:
   ```
   Initial commit: Add sprint planning board
   ```
5. Clica **"Commit changes"**

### Option B: Pelo Git (Terminal)

Se preferires usar git na linha de comandos:

```powershell
# Navega até à pasta do projeto
cd C:\Users\diogo\Sprintplanning

# Inicializa um repositório Git
git init

# Renomeia o ficheiro
ren sque.html index.html

# Adiciona tudo ao staging
git add .

# Faz commit
git commit -m "Initial commit: Add sprint planning board"

# Adiciona o repositório remoto
git remote add origin https://github.com/SEU_USERNAME/sprintplanning.git

# Envia para o GitHub (branch main)
git branch -M main
git push -u origin main
```

---

## **Passo 3: Ativa GitHub Pages**

1. No repositório no GitHub, vai a **Settings** (engrenagem no topo)
2. No menu esquerdo, seleciona **"Pages"**
3. Em "Build and deployment":
   - **Source**: seleciona `Deploy from a branch`
   - **Branch**: seleciona `main` e pasta `/root` (ou deixa tudo default)
4. Clica **"Save"**
5. Aguarda 1-2 minutos... depois aparece uma mensagem azul:
   ```
   Your site is live at: https://seu_username.github.io/sprintplanning/
   ```

---

## **Passo 4: Partilha no Discord**

Agora podes mandar o link nos amigos! 🎉

Copia o link que apareceu em Pages e manda no Discord:

```
Vejam o nosso sprint planning: https://seu_username.github.io/sprintplanning/
```

**Exemplo real:**
```
https://diogo-silva.github.io/sprintplanning/
```

---

## **Troubleshooting**

### O site não abre
- ✅ Verifica se o ficheiro se chama **`index.html`** (não `sque.html`)
- ✅ Aguarda 2-3 minutos para o Pages fazer o build
- ✅ Faz refresh ao browser (Ctrl+Shift+R)

### Mudanças não aparecem no site
- ✅ Garante que fizeste push do código
- ✅ Vai a **Actions** no repositório e verifica se o build passou (deve ter um ✅ verde)
- ✅ Aguarda 30-60 segundos e faz refresh

### Repository é privato?
- ✅ Vai a **Settings** → **General**
- ✅ Desce até "Danger Zone"
- ✅ Clica **"Change repository visibility"** → **"Make public"**

---

## **Próximos Passos (Opcional)**

### Adicionar um domínio customizado
1. Compra um domínio (ex: sprintplanning.pt)
2. Vai em **Settings** → **Pages**
3. Em "Custom domain", escreve o teu domínio
4. Segue as instruções do DNS

### Automatizar atualizações
Se quiseres que as mudanças apareçam automaticamente sem fazeres push manual:
1. Cria um Git Workflow (`.github/workflows/deploy.yml`)
2. Faz commit, push, e fica feito! ✨

---

## **Comandos Git Rápido (Resumo)**

Se quiseres atualizar o board depois:

```powershell
# Faz as mudanças ao ficheiro index.html no VSCode
# Depois, no terminal:

git add .
git commit -m "Update: descrição da mudança"
git push
```

A página atualiza automaticamente em 1-2 minutos! 🚀

---

## **Perguntas Frequentes**

**P: Posso fazer o repositório privado?**
R: Não, GitHub Pages requer repositório público (plano gratuito).

**P: Quantas pessoas podem aceder?**
R: Unlimited! Qualquer pessoa com o link consegue ver (sem precisa dar login).

**P: Os dados ficam guardados no GitHub?**
R: Sim! O repositório é o teu backup. Podes sempre fazer git clone noutro PC.

**P: Posso editar o board online?**
R: Não diretamente. Tens de editar o ficheiro localmente e fazer push.

---

## **Links Úteis**

- 🐙 [GitHub Pages Docs](https://pages.github.com/)
- 📚 [Git Tutorial](https://github.com/git-tips/tips)
- 🚀 [Como fazer um bom README]( https://guides.github.com/activities/hello-world/)

---

**Boa sorte! Se tiveres dúvidas, manda uma mensagem.** 💬
