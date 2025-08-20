# 🎯 Sessão Estratégica - Diagnóstico para Consultórios

Uma aplicação web interativa para avaliar o nível atual de gestão de consultórios e clínicas odontológicas, identificando oportunidades de melhoria através da **Mentoria ACME**.

## ✨ Funcionalidades

- ✅ **Quiz Interativo** - 20 perguntas estratégicas organizadas em 4 pilares
- ✅ **Navegação Fluida** - Uma pergunta por vez com transições suaves
- ✅ **Gráfico Radar Circular** - Visualização clara dos gaps de competência
- ✅ **Análise Detalhada** - Feedback personalizado por área
- ✅ **Design Responsivo** - Otimizado para desktop e mobile
- ✅ **CTA Integrado** - Direcionamento para página de vendas

## 🎨 Design

### Paleta de Cores
- **#000000** - Preto (principal)
- **#333333** - Cinza escuro (secundário)
- **#ffffff** - Branco (contraste)

### Tipografia
- **Playfair Display** - Títulos
- **Inter Bold** - Textos em destaque
- **Inter Regular** - Textos padrão

## 📊 Pilares Avaliados

1. **Finanças** (5 perguntas)
   - Reserva de emergência
   - Separação contas pessoais/profissionais
   - Margem de lucro por procedimento
   - Divisão com parceiros
   - Previsibilidade de faturamento

2. **Equipe** (5 perguntas)
   - Rotinas estruturadas
   - Delegação e supervisão
   - Motivação e comprometimento
   - Proatividade da equipe
   - Autonomia operacional

3. **Processos e Fidelização** (5 perguntas)
   - Documentação de processos
   - Autonomia para ausências
   - Recuperação de pacientes
   - Programas de fidelização
   - Campanhas internas

4. **Marketing e Vendas** (5 perguntas)
   - Consistência nas redes sociais
   - Habilidades de posicionamento
   - Captação de novos pacientes
   - Técnicas de vendas e objeções
   - Planejamento estratégico

## 🚀 Como Usar

### Pré-requisitos
- Nenhum! É um site estático HTML puro
- Funciona em qualquer navegador moderno

### Deploy no Netlify (Recomendado)

#### Método 1: GitHub + Netlify (Automático)

1. **Clone/Fork este repositório:**
   ```bash
   git clone https://github.com/seu-usuario/sessao-estrategica.git
   cd sessao-estrategica
   ```

2. **Conecte ao Netlify:**
   - Acesse [netlify.com](https://netlify.com)
   - Login com GitHub
   - "New site from Git" → GitHub
   - Selecione o repositório
   - Deploy automático!

#### Método 2: Drag & Drop

1. **Baixe os arquivos:**
   - `index.html`
   - `logo.png` (sua logo)

2. **Upload no Netlify:**
   - Acesse [netlify.com](https://netlify.com)
   - Arraste os arquivos para área de deploy
   - Site online em segundos!

### Deploy em Outros Serviços

#### Vercel
```bash
npm i -g vercel
vercel --prod
```

#### GitHub Pages
1. Suba para GitHub
2. Settings → Pages
3. Source: Deploy from branch
4. Branch: main

## 📱 Como Adicionar Sua Logo

### Método 1: Logo Local
1. Salve sua logo como `logo.png` na pasta do projeto
2. No `index.html`, encontre:
```html
<img src="logo.png" alt="Logo da Empresa" class="logo" style="display: none;">
```
3. Remova `style="display: none;"`:
```html
<img src="logo.png" alt="Logo da Empresa" class="logo">
```

### Método 2: Logo Online
Use o link direto da sua logo:
```html
<img src="https://seusite.com/logo.png" alt="Logo da Empresa" class="logo">
```

## 🔧 Personalização

### Alterar Links CTA
No final do `index.html`, substitua:
```html
<a href="SUA_PAGINA_DE_VENDAS" class="btn-cta">Quero Conhecer a Mentoria ACME</a>
<a href="SEU_CONTATO" class="btn-cta-secondary">Falar com um Especialista</a>
```

### Alterar Nome da Empresa
Substitua "Mentoria ACME" pelo nome da sua empresa em:
- Título da página
- CTAs finais
- Mensagens de resultado

### Ajustar Cores (Opcional)
Para tons mais suaves, substitua no CSS:
```css
#000000 → #2c2c2c  /* Cinza escuro */
#333333 → #4a4a4a  /* Cinza médio */
```

## 📊 Como Funciona

1. **Quiz Interativo:** 20 perguntas divididas em 4 pilares
2. **Escala 0-10:** Cada pergunta avaliada de 0 a 10
3. **Cálculo Automático:** Média por pilar e geral
4. **Gráfico Circular:** Visualização dos resultados vs ideal
5. **Feedback Personalizado:** Mensagens específicas por área
6. **CTA Direcionado:** Convite para a mentoria

## 🎯 Níveis de Resultado

- **80-100%:** Consultório Estruturado
- **60-79%:** Consultório em Desenvolvimento  
- **40-59%:** Consultório Iniciante
- **0-39%:** Consultório Crítico

## 📈 Analytics (Opcional)

Para adicionar Google Analytics, insira antes do `</head>`:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

## 🔒 Recursos de Segurança

- Headers de segurança configurados
- Proteção XSS
- HTTPS automático (Netlify)
- Sem dependências externas vulneráveis

## 📞 Suporte

Para dúvidas técnicas:
- Abra uma issue no GitHub
- Consulte [docs.netlify.com](https://docs.netlify.com)

## 📄 Licença

Este projeto é propriedade da **Mentoria ACME** e destinado exclusivamente para uso na captação de leads qualificados.

---

**Desenvolvido para transformar a gestão de consultórios odontológicos** 🦷✨
