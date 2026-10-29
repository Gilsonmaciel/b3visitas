# B3 Visitas – v1.0.1

App (PWA) para registrar visitas técnicas em concentradores e medidores de tanque e enviar o relatório em PDF ao cliente pelo WhatsApp. Funciona offline; os dados ficam no próprio celular (IndexedDB).

## Arquivos
- `index.html` – o app completo
- `jspdf.umd.min.js` – gerador de PDF (local, sem depender de internet)
- `sw.js` – service worker (funcionamento offline)
- `manifest.webmanifest`, `icon-192.png`, `icon-512.png` – instalação na tela inicial

## Publicar (precisa de HTTPS para GPS, câmera e instalação)
Opção recomendada – GitHub Pages (grátis):
1. Crie um repositório (ex.: `b3visitas`) e envie estes arquivos para a raiz.
2. Settings → Pages → Source: *Deploy from a branch* → `main` / `root`.
3. Acesse `https://SEU-USUARIO.github.io/b3visitas/` no Chrome do Android.
4. Menu ⋮ → **Instalar app** (ou "Adicionar à tela inicial").

Alternativa: Netlify Drop (arraste a pasta em app.netlify.com/drop).

## Atualizar uma versão
Altere os arquivos e **mude a constante `CACHE` em `sw.js`** (ex.: `b3visitas-v1.0.1`). O celular baixa a versão nova em segundo plano e passa a usá-la na abertura seguinte.

## Primeiro uso
1. Ajustes → dados da empresa, técnico, logo e mensagem padrão do WhatsApp.
2. Clientes → cadastre os postos com WhatsApp do contato e equipamentos (modelo/série).
3. Visitas → **+ Nova visita** ao chegar (registra hora e GPS) → preencha → **Finalizar** → assinatura → **Enviar PDF pelo WhatsApp**.

## Backup
Os dados ficam só no celular. Use Ajustes → Exportar backup (o app avisa após 7 dias sem backup). Limpar dados do Chrome apaga as visitas.
