# Convite — Anos da Andreia 🎂☀️

Página de convite + confirmação (RSVP) para o aniversário da **Andreia Morris Mendes**
(Domingo, 12 de julho de 2026, em Paredes).

Projeto **100% autónomo**: um único `index.html` + o vídeo. Sem dependências de
qualquer outro projeto. As confirmações são enviadas por email através do
serviço gratuito **FormSubmit** (nada de servidores próprios).

## Ficheiros
| Ficheiro | O que é |
|----------|---------|
| `index.html` | A página toda (HTML + CSS + JS, tudo embutido) |
| `convite-andreia.mp4` | O vídeo-convite |
| `.nojekyll` | Faz o GitHub Pages servir os ficheiros tal e qual |

## Como as confirmações chegam ao email
O formulário envia para o email da Andreia (definido no `index.html`) via **FormSubmit** (endpoint AJAX).

⚠️ **Passo único de ativação:** na **primeira** confirmação enviada, o FormSubmit
manda um email à Andreia com o assunto *"Confirm your email"* — basta ela clicar
em **"Activate Form"** uma vez. A partir daí, todas as confirmações chegam
automaticamente à caixa de entrada, com nome, presença, nº de pessoas e mensagem.

> Dica de privacidade: depois de ativar, o FormSubmit dá um endereço "alias"
> (ex.: `https://formsubmit.co/xxxxxxxx`) que se pode usar em vez do email, para
> não deixar o email à vista no código. É opcional.

## Publicar no GitHub Pages
1. Criar um repositório novo no GitHub (ex.: `convite-andreia`).
2. Enviar o conteúdo **desta pasta** (`site/`) para o repositório:
   ```bash
   cd site
   git init
   git add .
   git commit -m "Convite anos da Andreia"
   git branch -M main
   git remote add origin git@github.com:UTILIZADOR/convite-andreia.git
   git push -u origin main
   ```
3. No GitHub: **Settings → Pages → Build and deployment → Source: Deploy from a branch**,
   branch `main` / `/ (root)`. Guardar.
4. Ao fim de ~1 min fica em `https://UTILIZADOR.github.io/convite-andreia/`.
5. Abrir a página, fazer uma confirmação de teste e **ativar o FormSubmit** (ver acima).

## Alterar depois
- **Data / hora / morada:** procurar `12 de julho` e `2026-07-12T15:00:00+01:00` no `index.html`.
- **Texto do convite:** bloco `<p class="quote">`.
- **Email de destino:** variável `_u` no `<script>` do `index.html`.
- **Trocar o vídeo:** substituir `convite-andreia.mp4` (manter o nome).
