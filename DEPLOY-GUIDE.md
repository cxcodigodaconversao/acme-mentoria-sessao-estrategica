# 🚀 Guia de Deploy - GitHub + Netlify

## 📋 Checklist Antes de Começar

- [ ] Conta no GitHub criada
- [ ] Conta no Netlify criada (pode usar login do GitHub)
- [ ] Logo da empresa salva como `logo.png`
- [ ] Links de CTA definidos

---

## 📁 Estrutura de Arquivos

Certifique-se de ter estes arquivos:

```
📁 sessao-estrategica/
├── 📄 index.html          # Aplicação principal
├── 📄 README.md           # Documentação
├── 📄 netlify.toml        # Configurações Netlify
├── 📄 .gitignore         # Arquivos ignorados
├── 📄 DEPLOY-GUIDE.md    # Este guia
└── 🖼️ logo.png           # Sua logo (adicionar)
```

---

## 🔄 Passo 1: Preparar Arquivos

### 1.1 Adicionar Sua Logo
1. Salve sua logo como `logo.png` na pasta principal
2. No `index.html`, encontre esta linha:
```html
<img src="logo.png" alt="Logo da Empresa" class="logo" style="display: none;">
```
3. Remova `style="display: none;"`:
```html
<img src="logo.png" alt="Logo da Empresa" class="logo">
```

### 1.2 Configurar CTAs
No `index.html`, encontre e substitua:
```html
<!-- Substitua pelos seus links -->
<a href="SUA_PAGINA_DE_VENDAS" class="btn-cta">Quero Conhecer a Mentoria ACME</a>
<a href="SEU_WHATSAPP_OU_CONTATO" class="btn-cta-secondary">Falar com um Especialista</a>
```

**Exemplo:**
```html
<a href="https://mentoriaacme.com.br/inscricao" class="btn-cta">Quero Conhecer a Mentoria ACME</a>
<a href="https://wa.me/5511999999999" class="btn-cta-secondary">Falar com um Especialista</a>
```

---

## 🐙 Passo 2: Subir para GitHub

### 2.1 Criar Repositório
1. Acesse [github.com](https://github.com)
2. Clique em **"New repository"**
3. Nome: `sessao-estrategica` (ou outro nome)
4. Público ou Privado (sua escolha)
5. **NÃO** marque "Add README" (já temos um)
6. Clique **"Create repository"**

### 2.2 Upload dos Arquivos

**Opção A: Interface Web (Mais Fácil)**
1. No novo repositório, clique **"uploading an existing file"**
2. Arraste todos os arquivos para a área
3. Escreva: `Primeira versão da Sessão Estratégica`
4. Clique **"Commit changes"**

**Opção B: Linha de Comando**
```bash
# Na pasta dos arquivos
git init
git add .
git commit -m "Primeira versão da Sessão Estratégica"
git branch -M main
git remote add origin https://github.com/SEU_USUARIO/sessao-estrategica.git
git push -u origin main
```

---

## 🌐 Passo 3: Deploy no Netlify

### 3.1 Conectar GitHub ao Netlify
1. Acesse [netlify.com](https://netlify.com)
2. Clique **"Log in"** → **"GitHub"**
3. Autorize Netlify no GitHub

### 3.2 Criar Site
1. No dashboard, clique **"New site from Git"**
2. Escolha **"GitHub"**
3. Encontre e selecione `sessao-estrategica`
4. Configurações:
   - **Branch:** `main`
   - **Build command:** `echo 'Build complete'`
   - **Publish directory:** `.`
5. Clique **"Deploy site"**

### 3.3 Aguardar Deploy
- ⏱️ Deploy demora ~2 minutos
- ✅ Status mudará para "Published"
- 🔗 URL será gerada automaticamente

---

## 🔧 Passo 4: Configurações Finais

### 4.1 Nome do Site (Opcional)
1. Em **Site settings** → **General**
2. **Site name** → **Change site name**
3. Exemplo: `mentoria-acme-diagnostico`
4. URL ficará: `mentoria-acme-diagnostico.netlify.app`

### 4.2 Domínio Personalizado (Opcional)
1. **Domain settings** → **Add custom domain**
2. Digite: `diagnostico.mentoriaacme.com.br`
3. Configure DNS conforme instruções

### 4.3 Formulários (Opcional)
Se quiser capturar emails, adicione no HTML:
```html
<form name="leads" method="POST" data-netlify="true">
  <input type="email" name="email" placeholder="Seu email" required>
  <button type="submit">Receber Resultado</button>
</form>
```

---

## ✅ Passo 5: Teste Final

### 5.1 Checklist de Teste
- [ ] Site carrega corretamente
- [ ] Logo aparece
- [ ] Quiz funciona (responder algumas perguntas)
- [ ] Gráfico circular é gerado
- [ ] CTAs direcionam corretamente
- [ ] Funciona no mobile

### 5.2 URLs para Testar
- **Principal:** `https://seu-site.netlify.app`
- **Redirects:** 
  - `https://seu-site.netlify.app/diagnostico`
  - `https://seu-site.netlify.app/quiz`

---

## 🔄 Atualizações Futuras

### Como Atualizar o Site
1. **Edite arquivos** no computador
2. **Commit no GitHub:**
   - Interface web: Upload files → Commit
   - Linha de comando: `git add . && git commit -m "Atualização" && git push`
3. **Deploy automático** no Netlify em ~2 minutos

### Monitoramento
- **Analytics:** Netlify Analytics (gratuito básico)
- **Formulários:** Ver submissões em Netlify
- **Erros:** Logs em Deploy settings

---

## 🚨 Solução de Problemas

### Site não carrega
- ✅ Verificar se `index.html` está na raiz
- ✅ Verificar logs de deploy no Netlify
- ✅ Testar localmente (abrir `index.html` no navegador)

### Logo não aparece
- ✅ Arquivo `logo.png` está na pasta?
- ✅ Removeu `style="display: none;"`?
- ✅ Nome do arquivo está correto no HTML?

### Gráfico não funciona
- ✅ Chart.js está carregando? (verificar console F12)
- ✅ JavaScript tem erros? (verificar console F12)

### CTAs não funcionam
- ✅ Links estão corretos no HTML?
- ✅ URLs são válidas e acessíveis?

---

## 📞 Suporte

**Documentação Oficial:**
- Netlify: [docs.netlify.com](https://docs.netlify.com)
- GitHub: [docs.github.com](https://docs.github.com)

**Problemas Técnicos:**
- Abra issue no GitHub do projeto
- Verifique console do navegador (F12)

---

**🎉 Parabéns! Sua Sessão Estratégica está online e pronta para capturar leads qualificados!**
