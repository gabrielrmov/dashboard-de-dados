# Dashboard de Dados

Ferramenta interativa de análise estatística: escolha uma pergunta, o tipo de gráfico (barras, colunas, pizza, linha, pontos, ogiva, boxplot) e veja tabela de frequência, medidas de posição e quartis — com ou sem intervalo de classe. Vem com os dados de exemplo da pesquisa "Uso das redes sociais e da internet no dia a dia" (n = 16) e permite importar qualquer outro CSV.

Site estático de uma página só (`index.html`).

## Publicado no Cloudflare Pages

O site está publicado em **https://dashboard-de-dados.pages.dev** (projeto `dashboard-de-dados` na conta Cloudflare do usuário, via upload direto / Wrangler — sem repositório Git conectado).

Para atualizar o site publicado depois de editar `index.html`:

1. No painel da Cloudflare (**Trabalhadores e Páginas → dashboard-de-dados**), use **Create deployment** e arraste o novo `index.html`, ou
2. Rode `npx wrangler@latest pages deploy .` dentro da pasta do projeto, com a variável `CLOUDFLARE_API_TOKEN` definida (token com permissão **Conta → Cloudflare Pages → Editar**).

## Conectar um domínio próprio

1. No painel da Cloudflare, abra o projeto **dashboard-de-dados → Custom domains → Set up a custom domain**.
2. Digite o domínio ou subdomínio desejado (ex: `dashboard.seusite.com.br`).
3. Se o domínio já estiver na Cloudflare, o DNS é configurado automaticamente. Caso contrário, a Cloudflare mostra o registro `CNAME` para criar no seu provedor de domínio atual.
4. O certificado HTTPS é emitido automaticamente pela Cloudflare, geralmente em poucos minutos.

## Atualizar o dashboard

O arquivo é `index.html`. Edite localmente e publique de novo pelo painel da Cloudflare ou via Wrangler (veja acima). O histórico de versões também está neste repositório git local.
