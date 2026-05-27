# Adjailton & Rhafaella · Cupido

Pacote completo do casal **Adjailton & Rhafaella** — Dia dos Namorados 2026.
Encomendado pra surpreender a Rhafa.

## O que está pronto aqui

| Arquivo | Descrição |
|---|---|
| `index.html` | Página personalizada que a Rhafa abre via QR code |
| `fotos/` | 10 fotos do casal renomeadas (`01-capa-jardim.jpeg` é a capa) |
| `musica/` | Pasta vazia — receberá o MP3 depois de gerar no Suno |
| `carta.md` | Texto final da carta (passa o checklist do prompt-pai) |
| `musica.md` | Letra + style prompt prontos pra colar no Suno Pro |
| `../molde/carta-manuscrita-adja-rhafaella.html` | Molde A4 com linhas pra escrever à mão + QR no rodapé |

## Briefing do casal

- **Adjailton (Adja)** escreve pra **Rhafaella** (namorada)
- Juntos há **1 ano e 6 meses** — se conheceram pelo **Instagram**
- 3 manias amadas: ela pega no nariz dele, ela canta do nada, ela belisca ele
- Risada dela: quando ele só olha e ela solta uma gargalhada
- Momento marcante: primeiro encontro presencial, primeiro abraço todo sem graça
- Mudança: ela ensinou ele a se vestir melhor e a ser mais organizado
- Apelido só do casal: **neneca**
- **Tom escolhido:** intenso e apaixonado
- **Estilo musical:** sertanejo romântico (referência do cliente: "No céu dos teus braços")

## Checklist do que falta fazer pra entregar

- [ ] **Confirmar a data exata de início do namoro** com o cliente (hoje o contador está em `2024-11-26` como estimativa — 1 ano e 6 meses contados de 2026-05-26). Atualizar `index.html` linha do `const start`.
- [ ] **Gerar a música no Suno Pro** usando o conteúdo de [`musica.md`](musica.md)
  - Colar letra no campo *Lyrics*
  - Colar style prompt no campo *Style of music*
  - Title: `No Céu dos Teus Braços`
  - Gerar 3 versões, escolher melhor, baixar MP3
  - Renomear: `no-ceu-dos-teus-bracos-adja-rhafaella.mp3` → mover pra `musica/`
- [ ] **Hospedar o site** (Vercel ou Netlify Drop)
  - Drag-and-drop da pasta `deploy-adja-rhafaella/` inteira
  - Receber URL final (algo tipo `adja-rhafaella.vercel.app`)
- [ ] **Gerar o QR code** em qr-code-generator.com apontando pra URL do site
  - Salvar como `qr-adja-rhafaella.png`
  - Mover pra `../molde/qr-adja-rhafaella.png`
- [ ] **Atualizar o molde da carta** com QR real
  - Em `../molde/carta-manuscrita-adja-rhafaella.html`, substituir o `<div class="qr-placeholder">` pelo `<img src="qr-adja-rhafaella.png" alt="QR Code">`
  - Atualizar `adja-rhafaella.vercel.app` com a URL real, se diferente
- [ ] **Exportar molde como PDF**
  - Abrir o molde no navegador → `Ctrl+P` → "Salvar como PDF"
  - Renomear: `carta-adja-rhafaella.pdf`
- [ ] **Enviar pro Adjailton:**
  - PDF do molde (ele imprime e escreve à mão)
  - Link do site (pra ele conferir antes)
  - Texto da carta de [`carta.md`](carta.md) pra ele copiar à mão no molde

## Como testar o site localmente

```powershell
# Na raiz do projeto (onde tem package.json)
npx serve deploy-adja-rhafaella
```

Abrir `http://localhost:3000`.

## Decisões visuais tomadas

- **Hero / capa do site:** foto do abraço no jardim de jasmim (`01-capa-jardim.jpeg`) — momento de "primeiro abraço sem graça" citado no briefing
- **Album art (player de música):** `02-rhafaella.jpeg` — ela sozinha de macaquinho verde menta no jardim, foto enviada como capa da música pelo cliente
- **Iniciais usadas no selo e footer:** `A & R`
- **Contador:** desde 26/11/2024 ~20:00 (estimativa — 1 ano e 6 meses contados pra trás de 2026-05-26; confirmar com cliente)
- **Frase de capa:** `"No céu dos teus braços é onde eu sei voltar."` (gancho do refrão da música, também fecha a carta)
- **Eyebrow do hero:** "pra minha neneca" (apelido só deles)
- **Polaroids:** 8 momentos diferentes — parque iluminado, beijo na bochecha, casa à tarde, vermelho no espelho, selfie noturna, cinema, camisa do Mengão, academia
- **Timeline:** 3 marcos — Instagram (te vi na tela primeiro) → primeiro abraço sem graça → hoje (mil e quinhentos dias depois com as manias dela)

---

*Parte do projeto Cupido · 3º caso · 2026-05-26*
