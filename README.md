# PULSE · Felipe Ramos Advogados

> Dashboard de Business Intelligence operacional do escritório.
> Dados atualizados em tempo real via Google Sheets.

🟢 **Acesso ao vivo:** depois de habilitar GitHub Pages, fica em `https://SEU_USUARIO.github.io/NOME_DO_REPO/`

---

## 📋 Estrutura

```
├── index.html          ← dashboard (single-file)
├── fr-monogram.png     ← logo (referenciado pelo HTML)
├── README.md           ← este arquivo
└── INSTRUCOES_DEPLOY.md ← guia passo-a-passo
```

## 🎯 Funcionalidades

- **Vista dupla** Master / Equipe (toggle no rodapé do sidebar)
- **7 painéis:** Visão Executiva · Prazos · Produtividade · Equipe · Colaborador · Agenda · Tarefas Paradas
- **Modo TV** (canto superior direito) — fullscreen + auto-rotação entre abas + auto-refresh
- **Dados ao vivo** do Google Sheets (sem servidor)
- **Filtros interativos:** cards clicáveis, donuts com drill-down
- **Identidade FR** — paleta dourada, Montserrat, monograma

## 🔧 Configuração de dados

A planilha Google Sheets é a fonte de verdade. O ID está hardcoded no `index.html` (procure por `const SHEETS_ID =`).

Abas esperadas: `prazos`, `audiencias`, `publicacoes`, `workmonitor`, `paradas`, `ranking`.

Pra atualizar dados: edita a planilha → equipe recarrega o dashboard (F5).

---

Construído com HTML/CSS/JS puro + Chart.js + Tailwind CDN. Zero build, zero servidor.
