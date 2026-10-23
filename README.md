# Títulos a Receber — FT e pendências de baixa

Painel HTML com a paleta do Grupo Décio. A SE1 é separada em dois conjuntos: **FT em cobrança** e **RA, NCC e CC pendentes de baixa**. A aplicação pública inicia sem bases financeiras ou De_paras; importe os arquivos no próprio navegador.

## Tipos e carteiras

Somente FT compõe A Receber, as carteiras de cobrança, o detalhamento FT e os ofensores. RA, NCC e CC são classificados como já pagos e aguardando baixa, conforme a regra informada; ficam em uma aba própria com indicadores de valor e quantidade, gráficos por tipo e detalhamento. Não recebem carteira. Nos dois conjuntos, usar DT Baixa sem data, Vlr. Título, as exclusões do De_para e uma ocorrência por chave de título.

Grupo usa o início da Filial Orig: 01 Rodoviário, 02 TRR, 08 Peças e 09 Urbano. Apenas nos FT: Urbano/Peças → Ana Claudia, TRR → Thalita, demais grupos por Nome Cliente (0–E Milena, F–Q Maria Eduarda, R–Z Thalita). Nome ausente ou inicial inválida fica Sem classificação. Não há filtro por Conferencia e não se utiliza SE5.

## Vencimentos e ofensores

Competência e gráficos diários usam Vencto Real. FT possui sua linha de valor a receber; RA/NCC ficam na página Pendências de baixa, com seletores independentes de dia. Cada seleção modifica somente o respectivo gráfico e resumo diário, preservando os indicadores gerais.

Top 5 ofensores usa somente FT sem baixa e com mais de 3 dias corridos de atraso até a data atual de São Paulo. Exatamente 3 dias fica fora; 4 dias entra. Agrupar Cliente + Loja por mês de Vencto Real, somar Vlr. Título e ordenar do maior para o menor; empate pela chave Cliente + Loja. RA, NCC e CC ficam fora do ranking.

## Importação, exclusões e histórico

Em Atualizar bases, importe a SE1 completa da posição. Na primeira carga, inclua o de_para_geral.xlsx. Excluir Cliente + Loja com Status Desconsiderar nas abas cartões e intercompany. A primeira linha sem baixa define valor/vencimento em uma chave repetida; divergências são sinalizadas.

Uma nova SE1 substitui a posição atual e preserva a anterior. As posições não são somadas; reimportar a mesma extração não duplica o histórico. Dados importados e histórico são processados no navegador em IndexedDB. Cada origem, navegador e computador tem dados próprios. Use backup e restauração para transferir posições. Exportar CSV acompanha a página e o recorte.

## Publicação

Aplicação completa em index.html, sem dependências externas. GitHub Pages: branch main, raiz do repositório, com .nojekyll. A publicação pública contém somente aplicação e cabeçalhos.

Desenvolvido por Anderson Prado © 2026.
