# 📖 Passo a Passo: Publicar MeliFIT no GitHub Pages

## 🎯 Objetivo Final
Ter o site disponível em: **https://elismeli.github.io/melifit/**

---

## ✅ Pré-requisitos

1. Ter uma conta no GitHub (já tem: **ElisMeli**)
2. Ter o Git instalado no Windows

### Verificar se tem Git instalado:
```powershell
git --version
```

Se não tiver, baixe aqui: https://git-scm.com/download/win

---

## 📝 PASSO 1: Criar Repositório no GitHub

1. Acesse: https://github.com/new
2. Preencha:
   - **Repository name**: `melifit`
   - **Description**: `MeliFIT v2.0 - Desafio de saúde e bem-estar`
   - **Public** ✅ (marque Public)
   - **NÃO marque** "Add README" (já temos um)
3. Clique em **"Create repository"**

---

## 💻 PASSO 2: Preparar os Arquivos (PowerShell)

Abra o PowerShell e execute os comandos abaixo:

```powershell
# Navega até a pasta com os arquivos
cd "C:\Users\fernandes\Downloads\MeliFIT-GitHub"

# Verifica se os arquivos estão lá
dir

# Inicializa o repositório Git
git init

# Adiciona todos os arquivos
git add .

# Cria o primeiro commit
git commit -m "MeliFIT v2.0 - Versão inicial com novas funcionalidades"

# Renomeia a branch para main (padrão GitHub)
git branch -M main

# Conecta com o repositório remoto (SUBSTITUA SEU-TOKEN abaixo)
git remote add origin https://github.com/ElisMeli/melifit.git

# Envia os arquivos para o GitHub
git push -u origin main
```

### ⚠️ Atenção no comando `git push`:

**Primeira vez usando Git?** O GitHub vai pedir autenticação:
- **Username**: `ElisMeli`
- **Password**: Use um **Personal Access Token** (não sua senha!)

---

## 🔑 PASSO 2.5: Criar Personal Access Token (se necessário)

Se o GitHub pedir senha ao fazer `git push`:

1. Acesse: https://github.com/settings/tokens
2. Clique em **"Generate new token"** → **"Generate new token (classic)"**
3. Preencha:
   - **Note**: `MeliFIT Deploy`
   - **Expiration**: 90 days (ou no expiration)
   - **Select scopes**: Marque apenas **`repo`** ✅
4. Clique em **"Generate token"**
5. **COPIE O TOKEN** (só aparece 1 vez!)
6. Use esse token como senha no `git push`

---

## 🌐 PASSO 3: Ativar GitHub Pages

1. No repositório GitHub, clique em **Settings** (Configurações)
2. No menu lateral, clique em **Pages**
3. Em **"Source"** (Branch):
   - Selecione: `main`
   - Folder: `/ (root)`
4. Clique em **"Save"**

**Aguarde 1-2 minutos** para o GitHub processar! ⏱️

---

## 🎉 PASSO 4: Testar o Site

Acesse: **https://elismeli.github.io/melifit/**

Se aparecer erro 404, aguarde mais 1 minuto e atualize a página.

---

## 📱 PASSO 5: Compartilhar o Link

Agora é só compartilhar o link com a equipe:

```
https://elismeli.github.io/melifit/
```

---

## 🔄 Como Atualizar o Site Depois

Sempre que quiser atualizar o conteúdo:

```powershell
# Navega até a pasta
cd "C:\Users\fernandes\Downloads\MeliFIT-GitHub"

# Faz as alterações nos arquivos (edite o index.html)

# Adiciona as mudanças
git add .

# Cria novo commit
git commit -m "Descrição do que mudou"

# Envia para o GitHub
git push

# Aguarde 1-2 minutos e o site atualiza automaticamente!
```

---

## ❓ Problemas Comuns

### Erro: "remote origin already exists"
```powershell
git remote remove origin
git remote add origin https://github.com/ElisMeli/melifit.git
```

### Erro: "Authentication failed"
- Use Personal Access Token, não sua senha
- Veja o PASSO 2.5 acima

### Site não carrega / 404
- Aguarde 2-3 minutos após ativar GitHub Pages
- Verifique se o arquivo se chama **index.html** (não outro nome)
- Confirme que o branch é **main**

### Quer mudar o nome do site?
- Renomeie o repositório em Settings → General
- Novo link será: `https://elismeli.github.io/novo-nome/`

---

## 🎯 Comandos Resumidos (Cola)

```powershell
# Setup inicial
cd "C:\Users\fernandes\Downloads\MeliFIT-GitHub"
git init
git add .
git commit -m "MeliFIT v2.0 - Versão inicial"
git branch -M main
git remote add origin https://github.com/ElisMeli/melifit.git
git push -u origin main

# Atualizações futuras
git add .
git commit -m "Atualização do conteúdo"
git push
```

---

## 💡 Dicas Extras

### Link Personalizado
Se quiser um domínio customizado (ex: melifit.com.br):
1. Compre o domínio
2. Em Settings → Pages → Custom domain
3. Configure o DNS

### Analytics
Para ver quantas pessoas acessam:
1. Crie conta no Google Analytics
2. Adicione o código no `<head>` do index.html

### Editar Online
Não quer usar Git? Edite direto no GitHub:
1. Abra o repositório
2. Clique em `index.html`
3. Clique no ícone de lápis (Edit)
4. Faça as mudanças
5. Clique em "Commit changes"

---

## 📞 Precisa de Ajuda?

Se tiver qualquer dúvida durante o processo, me chame! 

---

**Boa sorte com o MeliFIT! 💪🔥**

#TreinamosParaGanhar
