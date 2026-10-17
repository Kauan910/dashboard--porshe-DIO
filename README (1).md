# Porsche Sales Dashboard

Dashboard interativa em HTML, CSS e JavaScript criada a partir da aba `Sanitized` da planilha de vendas Porsche disponibilizada no desafio da DIO.

## Perguntas de negócio
1. **Quais modelos vendem mais?** O gráfico compara a quantidade de registros por modelo.
2. **Quais modelos geram mais receita?** O gráfico soma os preços sanitizados por modelo.
3. **Como as vendas evoluem ao longo do tempo?** O gráfico mostra a quantidade de vendas por ano da data da venda.

Essas perguntas permitem observar volume, faturamento e distribuição temporal sem depender de uma coleção excessiva de gráficos.

## Indicadores e filtros
- Indicadores: quantidade de vendas no recorte, receita total e preço médio.
- Filtros: modelo, cidade, ano do veículo e método de pagamento.
- Os gráficos e indicadores são recalculados quando os filtros mudam.
- O botão **Limpar filtros** restaura a visão completa.

## Tratamento dos dados
Foram utilizadas somente as colunas sanitizadas necessárias:
- `PorscheModelSanitized`
- `ModelYearSanitized`
- `SalesPriceSanitized`
- `PayMethodSanitized`
- `CitySanitized`
- `StateSanitized` (mantido na preparação, embora não seja um filtro nesta versão)
- `SaleDateSanitized`

Os valores de ano e preço foram convertidos para números. As datas com valor `INVALID` não são usadas no gráfico temporal, mas os registros continuam participando dos indicadores e dos gráficos de modelo quando possuem os demais dados. A dashboard não inclui nome de cliente, vendedor ou identificador de venda. Os preços são exibidos em USD, moeda usada pela planilha de origem.

## Prompt utilizado
> Crie uma dashboard interativa de vendas da Porsche em um único arquivo HTML, usando HTML, CSS e JavaScript. Responda: quais modelos vendem mais, quais modelos geram mais receita e como as vendas evoluem por ano da data de venda. Inclua indicadores de quantidade de vendas, receita total e preço médio; filtros por modelo, cidade, ano do veículo e método de pagamento; e um botão para limpar os filtros. Use visual premium inspirado na Porsche, com fundo escuro e detalhes vermelhos. Incorpore os dados sanitizados no HTML, não invente resultados e exclua datas inválidas apenas do gráfico temporal. Garanta que todos os filtros atualizem os indicadores e gráficos.

## Ferramenta e implementação
Esta versão foi montada como arquivo HTML único, com CSS e JavaScript incorporados. Os gráficos são desenhados com elementos HTML/CSS, sem bibliotecas externas. A base sanitizada está incorporada no próprio arquivo para que a dashboard funcione ao abrir `index.html` localmente, sem servidor.

## Como testar localmente
1. Baixe `index.html`.
2. Abra o arquivo no navegador.
3. Altere os filtros e confira se os três indicadores e os gráficos são atualizados.
4. Clique em **Limpar filtros** para voltar à visão completa.

## Como publicar no GitHub Pages
1. Crie um repositório público chamado `porsche-sales-dashboard`.
2. Envie `index.html` e este `README.md` para a raiz do repositório.
3. No GitHub, entre em **Settings → Pages**.
4. Em **Build and deployment**, selecione **Deploy from a branch**, escolha `main` e a pasta `/ (root)`, e salve.
5. Aguarde a publicação e abra o endereço indicado pelo GitHub Pages. Normalmente, o formato é `https://SEU-USUARIO.github.io/porsche-sales-dashboard/`.
6. Coloque o endereço real publicado neste README depois que o GitHub gerar o link.

## Evidências sugeridas
Inclua no repositório uma captura de tela da dashboard e outra com um filtro aplicado. Atualize esta seção com o nome dos arquivos de imagem que você adicionar.
