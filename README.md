# Títulos a Receber — Grupo Décio

Painel HTML de títulos em aberto da SE1, com visão executiva, detalhamento e Top 5 ofensores por mês do vencimento. A SE5 não é utilizada. A versão pública do GitHub inicia sem dados financeiros; importe as bases no próprio navegador.

## Importação e histórico

Uma nova SE1 substitui a posição aberta atual inteira e preserva a anterior em Posição da base. Extrações abertas nunca são somadas. Reimportar uma posição idêntica não duplica o histórico. IndexedDB guarda os dados neste navegador; use o backup para preservar e transferir as posições. Cada origem, navegador e computador tem dados próprios.

Abertos são os títulos com DT Baixa vazia ou igual a `//`. Os valores usam Vlr. Titulo, uma vez por chave de título. Não existe filtro por Conferencia. O De_para geral exclui Cliente + Loja com Status Desconsiderar nas abas cartões e intercompany. Duplicatas conflitantes são sinalizadas e mantêm a primeira linha aberta observada.

## Grupo e carteira

Grupo usa o início de Filial Orig: 01 Rodoviário, 02 TRR, 08 Peças e 09 Urbano. Carteira prioriza Urbano e Peças para Ana Claudia e TRR para Thalita. Nos demais grupos usa Nome Cliente, sem acentos: 0–E Milena, F–Q Maria Eduarda, R–Z Thalita. Nome vazio fica em Sem classificação.

## Gráficos diários

Competência e linhas diárias RA/NCC usam Vencto Real. Cada gráfico tem seu próprio filtro de dia, seleção pelo ponto e botão Mostrar todos os dias. Selecionar um dia muda apenas a linha, o valor e a quantidade do respectivo gráfico; preserva os indicadores gerais e o outro gráfico. Limpar filtros restaura as duas séries.

RA, NCC e CC mostram reais e quantidade de títulos únicos. Cartão Frota e Nota Prazo aguardam os tipos aprovados.

## Top 5 ofensores

Entram apenas títulos ainda em aberto com data de análise − Vencto Real > 3 dias corridos. Exatamente 3 dias não entra; 4 dias entra. Títulos pagos, futuros ou sem vencimento válido ficam fora. A data de análise é o dia atual no fuso de São Paulo e aparece no painel.

Cada mês usa Vencto Real e classifica Cliente + Loja pelo total aberto de Vlr. Titulo em atraso acima de 3 dias, do maior para o menor. Desempate por chave Cliente + Loja. A classificação não depende do histórico de pagamentos do cliente. Os filtros de competência, carteira, grupo, ilha e busca recalculam até cinco clientes por mês. A posição selecionada limita o conjunto de títulos; outras posições não são somadas.

O ranking mostra valor em aberto, títulos únicos vencidos, atraso médio, maior atraso e vencimento mais antigo. Exportar CSV na página do ranking exporta o Top 5 mensal do recorte.

## Publicação e privacidade

A publicação contém somente a aplicação e os cabeçalhos, sem bases financeiras ou De_paras. As bases importadas são processadas no navegador. A publicação usa GitHub Pages, branch main, raiz do repositório, com .nojekyll. A aplicação não depende de serviços externos para os cálculos.

Desenvolvido por Anderson Prado © 2026.
