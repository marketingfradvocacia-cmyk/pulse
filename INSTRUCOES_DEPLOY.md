# Como hospedar o PULSE no GitHub Pages

> Guia passo-a-passo. Tempo total: **~10 minutos**. Custo: **R$ 0,00**.

---

## ✅ Pré-requisitos

- Uma conta no GitHub (cria grátis em https://github.com/signup)
- Os 2 arquivos prontos nesta pasta:
  - `index.html`
  - `fr-monogram.png`

---

## 🚀 Passo 1 — Criar o repositório

1. Entra em https://github.com → faz login
2. Canto superior direito: clica no **`+`** → **New repository**
3. Preenche:
   - **Repository name:** `pulse` (ou outro nome curto)
   - **Description:** `Dashboard PULSE - Felipe Ramos Advogados`
   - Visibilidade: **Public** (necessário pra Pages funcionar grátis)
   - ✅ Marca **"Add a README file"**
4. Clica **Create repository**

→ Você cai numa página do tipo `https://github.com/SEU_USUARIO/pulse`

---

## 📤 Passo 2 — Subir os arquivos

### Caminho A — Drag-and-drop (mais fácil)

1. Na página do repo, clica em **"Add file"** → **"Upload files"**
2. **Arrasta os arquivos** `index.html` e `fr-monogram.png` da pasta `C:\PULSE\GitHubDeploy\` pra dentro da área de upload
3. Em "Commit changes" embaixo:
   - Mensagem: `subir dashboard inicial`
   - Clica **"Commit changes"**

### Caminho B — Editor web (alternativa)

1. Repo → **"Add file"** → **"Create new file"**
2. Nome do arquivo: `index.html`
3. Cola o conteúdo do `index.html` local
4. **"Commit new file"**
5. Repete pro `fr-monogram.png` (mas drag-and-drop é melhor pra binários)

---

## 🌐 Passo 3 — Ativar GitHub Pages

1. No repo, clica em **"Settings"** (ícone de engrenagem, barra superior)
2. Menu lateral esquerdo: **Pages**
3. Em **"Source"** seleciona **"Deploy from a branch"**
4. Em **"Branch"** escolhe **`main`** e a pasta **`/ (root)`**
5. **Save**

→ GitHub mostra uma mensagem amarela: *"Your site is live at https://SEU_USUARIO.github.io/pulse/"*

⏱ **Demora 1-3 minutos** pra ficar acessível na primeira vez.

---

## 🎯 Passo 4 — Acessar e compartilhar

Abre no navegador:

```
https://SEU_USUARIO.github.io/pulse/
```

(Substitua `SEU_USUARIO` pelo seu usuário GitHub e `pulse` pelo nome do repo)

**Pra equipe acessar:** copia essa URL e compartilha. Funciona em qualquer dispositivo (PC, celular, tablet) com internet.

---

## 🔄 Como atualizar o dashboard

Sempre que mudar o `index.html`:

1. Repo no GitHub → clica em `index.html` na lista de arquivos
2. Ícone de **lápis ✏** (canto superior direito do código)
3. Edita o que precisa OU clica em **"..."** → **"Replace this file"** pra subir uma versão nova
4. **"Commit changes"**

→ O site atualiza em **30 segundos**.

---

## 🆘 Troubleshooting

**"Page not found" ao abrir a URL**
→ Esperar mais alguns minutos (pode demorar 5min na primeira vez)
→ Confirmar que o arquivo está com nome exato `index.html` (case-sensitive)

**Logo não aparece**
→ Confirma que `fr-monogram.png` foi enviado e tem esse nome exato

**Dados não atualizam (badge "Modo demo")**
→ A planilha Google Sheets continua sendo a fonte. Veja `INSTRUCOES_GOOGLE_SHEETS.md` no projeto local

**Modo TV não vira fullscreen**
→ Alguns browsers bloqueiam fullscreen sem interação. Aceita o popup quando aparecer

---

## 🎁 Bônus: domínio personalizado

Se você tem um domínio (ex: `pulse.feliperamosadv.com.br`):

1. Em **Settings → Pages → Custom domain** digita o domínio
2. No painel do seu domínio, adiciona registro CNAME:
   ```
   pulse.feliperamosadv.com.br → SEU_USUARIO.github.io
   ```
3. GitHub provisiona HTTPS automaticamente

---

✅ **Tudo pronto.** Equipe acessa via navegador, sem instalar nada.

⚠ **Lembrete de segurança:** o HTML é público (qualquer um com o link vê os dados). Pro PULSE, isso é aceitável porque a planilha Sheets também tá compartilhada como "Qualquer um com link · Leitor". Se precisar restringir, use Cloudflare Access ou hospede num servidor privado.
