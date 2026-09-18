# Dashboard de Dados

Ferramenta interativa de análise estatística: escolha uma pergunta, o tipo de gráfico (barras, colunas, pizza, linha, pontos, ogiva, boxplot) e veja tabela de frequência, medidas de posição e quartis — com ou sem intervalo de classe. Vem com os dados de exemplo da pesquisa "Uso das redes sociais e da internet no dia a dia" (n = 16) e permite importar qualquer outro CSV.

Site estático de uma página só (`index.html`).

## Publicado no GitHub Pages

O site está publicado em **https://gabrielrmov.github.io/dashboard-de-dados/**

Repositório: https://github.com/gabrielrmov/dashboard-de-dados (branch `main`, pasta raiz, publicado via GitHub Pages — Settings → Pages).

> Nota: uma tentativa anterior de publicar no Cloudflare Pages foi abandonada porque a plataforma retornava erro 404 para qualquer deploy feito nessa conta (deploys marcados como "sucesso" no painel, mas o site nunca ficava acessível — problema do lado da Cloudflare, não do processo de deploy). O GitHub Pages funcionou de primeira.

Para atualizar o site publicado depois de editar `index.html`:

1. Pela interface do GitHub: abra o repositório, clique em `index.html` → ícone de lápis (editar) → "Commit changes", ou use "Add file → Upload files" para substituir o arquivo.
2. Ou clonando o repositório localmente e usando git normalmente (`git add`, `git commit`, `git push`).

O GitHub Pages republica automaticamente em cerca de 1 minuto após cada push na branch `main`.

## Conectar um domínio próprio

1. No repositório, vá em **Settings → Pages → Custom domain**, digite o domínio e salve. Isso cria um arquivo `CNAME` no repositório.
2. No seu provedor de domínio, crie um registro:
   - **Subdomínio** (ex: `dashboard.seusite.com.br`): um registro `CNAME` apontando para `gabrielrmov.github.io`.
   - **Domínio raiz** (ex: `seusite.com.br`): registros `A` apontando para os IPs do GitHub Pages:
     `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`.
3. Marque **Enforce HTTPS** assim que o certificado ficar disponível (pode levar até 24h).

## Atualizar o dashboard

O arquivo é `index.html`. Edite, publique de novo (veja acima) — o histórico de versões também está neste repositório git local (`/tmp/dashboard/repo`, ainda não sincronizado com o remoto além do primeiro upload).
