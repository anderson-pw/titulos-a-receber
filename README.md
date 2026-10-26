# Títulos a Receber — FT e pendências de baixa

Painel HTML com paleta Grupo Décio. Importa a posição XLSX ou SE1 CSV e o De_para, com processamento no navegador e histórico local. A publicação pública inicia sem registros financeiros.

O valor usa **Saldo líquido** quando a coluna existe. Nas SE1 antigas, usa **Vlr. Título**. Considera somente **DT Baixa sem data**, conforme regra confirmada. A chave inclui filial, prefixo, título, parcela, tipo, cliente e loja; parcelas distintas são preservadas. O valor original não é somado novamente ao saldo líquido.

Somente FT recebe carteira e entra em A Receber e ofensores. RA/NCC/CC ficam em Pendências de baixa. Grupo por Filial Orig (01/02/08/09); carteiras por Nome ou Nome Cliente, preservadas as prioridades de TRR, Urbano e Peças. Exclusões por Cliente + Loja no De_para. Sem SE5 e sem filtro de Conferencia.

Filtros de emissão, vencimento, competência, carteira, grupo, tipo e posição têm seleção múltipla e são independentes por aba. Os gráficos seguem o recorte superior. Ao selecionar várias posições, usa a mais recente entre elas, sem somá-las. Use backup para transportar o histórico entre navegadores.

A posição de 26/10/2026 substitui a atual e mantém as anteriores. A referência de Thalita foi usada para comparação, sem alterar os valores operacionais para igualar totais. O relatório de conciliação acompanha os arquivos entregues.

Verificação: `node validate-position.mjs` e `node build.mjs`. Gerar a aplicação pública com `node build-public.mjs`; esse arquivo contém somente cabeçalhos e a aplicação.
