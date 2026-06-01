# ⚡ Quick Start - GitHub Pages em 5 Minutos

**Guia simples para partilhar o sprint board com a equipa no Discord**

---

## 1️⃣ Cria o Repositório no GitHub

### O quê é um repositório?
Um repositório é como uma pasta na cloud onde guardas o código. Todos conseguem aceder se soubere o link!

### Como fazer:

1. Vai a **[github.com/new](https://github.com/new)**
2. Preenche com:
   - **Repository name**: `sprintplanning` (sem espaços)
   - **Description**: "Sprint Planning Kanban - Integra-te" (opcional)
   - **Tipo**: ✅ Marca **Public** (importante! senão ninguém consegue ver)
   - **Initialize this repository with: README**: ✅ Marca
3. Clica no botão azul **"Create repository"**

### Verificação:
- Deves estar agora numa página que diz "sprintplanning" no topo
- URL deve ser assim: `https://github.com/SEU_USERNAME/sprintplanning`

---

## 2️⃣ Envia o Arquivo para o GitHub

### Primeiro, renomeia o ficheiro:

```powershell
cd C:\Users\diogo\Sprintplanning

# Muda o nome de sque.html para index.html
# (O GitHub Pages só reconhece index.html como página principal)
ren sque.html index.html
```

### Depois, configura o Git e envia tudo:

```powershell
# Inicializa um repositório Git local
# (isto prepara a pasta para funcionar com Git)
git init

# Diz ao Git para rastrear TODOS os ficheiros
git add .

# Guarda uma "snapshot" dos ficheiros
# (é como um ponto de controlo)
git commit -m "Add sprint board"

# Conecta o teu repositório local ao GitHub
# (ATENÇAO: substitui SEU_USERNAME pelo teu user do GitHub)
git remote add origin https://github.com/SEU_USERNAME/sprintplanning.git

# Renomeia o branch para "main" (padrão do GitHub)
git branch -M main

# Envia tudo para o GitHub (guarda online)
# (isto pode levar 5-10 segundos)
git push -u origin main
```

### O que aconteceu?
- O teu ficheiro `index.html` está agora no GitHub
- Todos os arquivos também foram enviados
- O GitHub tem um backup do teu projeto

### Verificação:
- Vai a `https://github.com/SEU_USERNAME/sprintplanning`
- Deves ver o arquivo `index.html` listado lá

---

## 3️⃣ Ativa GitHub Pages

### O que é GitHub Pages?
É um serviço gratuito que transforma uma pasta do repositório numa página web pública.

### Como ativar:

1. No repositório do GitHub, vai ao topo e clica em **Settings** (engrenagem ⚙️)
2. No menu esquerdo, clica em **Pages**
3. Em "Build and deployment":
   - **Source**: Seleciona `Deploy from a branch`
   - **Branch**: Seleciona `main` (deve estar pronto)
   - **Folder**: Deixa `/root` (já está correto)
4. Clica no botão **"Save"**

### O que acontece agora?
- O GitHub faz o "build" da página (leva 1-2 minutos)
- Depois aparece uma mensagem azul no topo que diz:
  ```
  Your site is live at: https://seu_username.github.io/sprintplanning/
  ```

### Verificação:
- Se vires essa mensagem, está pronto! ✅
- Se não vires, aguarda 2-3 minutos e faz F5 para dar refresh

---

## 4️⃣ Partilha no Discord

### Agora tens o link!

Copia este link (e substitui `seu_username` pelo teu username do GitHub):
```
https://seu_username.github.io/sprintplanning/
```

### Exemplo real:
Se o teu username for `diogo-silva`, o link é:
```
https://diogo-silva.github.io/sprintplanning/
```

### Manda no Discord:
```
Pessoal, vejam o nosso sprint planning aqui:
https://seu_username.github.io/sprintplanning/
```

Qualquer pessoa com o link consegue abrir, ver, arrastar cards e criar novas tasks! 🎉

---

## ❌ Se Algo Correr Mal...

### "Error: fatal: 'origin' does not appear to be a git repository"

**Solução**: O Git não foi inicializado. Faz isto:
```powershell
cd C:\Users\diogo\Sprintplanning
git init
```

### "Everything up-to-date"

**Significado**: Tudo já está no GitHub. Isto é BOAS notícias! ✅

### "Permission denied (publickey)"

**Solução**: O Git não consegue aceder ao Getty. Faz isto:
```powershell
# Gera uma chave SSH (só fazer uma vez)
ssh-keygen -t ed25519 -C "seu_email@gmail.com"

# Copia a chave pública
type $PROFILE\..\..\.ssh\id_ed25519.pub | clip

# Vai a https://github.com/settings/keys
# Clica "New SSH key"
# Cola a chave e guarda
```

### "arquivo index.html não aparece no GitHub"

**Solução**: Faz push de novo:
```powershell
git add .
git commit -m "Add index.html"
git push
```

### "O site não abre / mostra erro 404"

**Solução**:
1. Aguarda 3-5 minutos (às vezes leva)
2. Vai a **Settings → Pages** e verifica se o "Build" tem um ✅ verde
3. Faz Refresh do browser (Ctrl+Shift+R)
4. Se ainda não funciona, avalia se o URL está correto

---

## ✅ Checklist Final

Antes de mandares no Discord, verifica:

- ✅ Ficheiro renomeado para `index.html`
- ✅ `git push` funcionou sem erros
- ✅ No GitHub, o repositório é **Public**
- ✅ Pages está ativado em **Settings → Pages**
- ✅ O site abre e consegues arrastar cards
- ✅ Copiar o link correto para partilhar

---

## 🚀 Próximos Passos

### Para atualizar o board depois:

Se fizeres mudanças ao arquivo `index.html` (ex: adicionar tasks), faz isto para enviar para o GitHub:

```powershell
cd C:\Users\diogo\Sprintplanning

# Marca os ficheiros modificados
git add .

# Guarda as mudanças
git commit -m "Update: descreve o que mudaste"

# Envia para o GitHub
git push
```

**A página atualiza automaticamente em 1-2 minutos!**

---

**Boa sorte! Se tiveres dúvidas, manda uma mensagem.** 💬
