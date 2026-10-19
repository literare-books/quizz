# Quiz de captação — Literare Books

Página única (`index.html`) do quiz de qualificação de leads (Solo + Coautoria).
Sem build, sem dependências — o JS inline fala direto com o webhook do
DataCrazy e redireciona pro WhatsApp no final.

## Deploy no EasyPanel

1. Suba esta pasta pra um repositório Git (GitHub/GitLab) que o EasyPanel
   consiga acessar.
2. No EasyPanel: **+ Create → App** (não "Static", usamos Dockerfile).
3. Em **Source**, aponte pro repositório e branch.
4. Em **Build**, método **Dockerfile** (ele já detecta o `Dockerfile` na raiz).
5. Em **Domains**, adicione o domínio/subdomínio que vai apontar pro quiz.
6. Deploy. A cada push nessa branch, repetir o deploy manualmente ou ligar
   auto-deploy (webhook do GitHub), se o EasyPanel oferecer.

## Atualizar o quiz

O arquivo real vive como Artifact no Claude
(`quiz-solo-coautoria.html` → republicado aqui como `index.html`). Pra
atualizar: substitua `index.html` por uma versão nova e dê um novo deploy —
não precisa mexer no Dockerfile nem no nginx.conf.
