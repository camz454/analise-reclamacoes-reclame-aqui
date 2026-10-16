# Análise de Reclamações com Python: Uma Visão sobre a Contabilizei no Reclame Aqui

Projeto acadêmico desenvolvido na disciplina **EAC0582 – Tópicos de Tecnologia nos Negócios**, da **FEA-USP**, no primeiro semestre de 2025.

## Sobre o projeto

Este projeto analisa reclamações relacionadas à **Contabilizei**, publicadas na plataforma **Reclame Aqui**, com o objetivo de explorar padrões de insatisfação, a distribuição dos status das reclamações e os assuntos mais recorrentes. A análise combina visualizações, processamento de linguagem natural (NLP) e técnicas de aprendizado de máquina em **Python**, utilizando o **Google Colab**.

O conjunto de dados utilizado no trabalho possui **450 reclamações**. A coleta foi realizada com o **Instant Data Scraper** e os dados foram organizados em uma planilha Excel para análise.

## Objetivos

- Visualizar a distribuição das reclamações por status.
- Investigar a variável temporal disponível na base, agrupada por status.
- Classificar automaticamente os sentimentos expressos nos **títulos** das reclamações.
- Identificar grupos de reclamações com temas semelhantes por meio de *clustering*.
- Explorar palavras recorrentes nos títulos e discutir oportunidades de melhoria do atendimento e dos serviços.

## Tecnologias e bibliotecas

| Ferramenta / biblioteca | Aplicação no projeto |
| --- | --- |
| Python e Google Colab | Execução e organização das análises |
| Pandas | Leitura do Excel, tratamento e agregação de dados |
| NumPy e `re` | Tratamento de valores ausentes e conversão de expressões de tempo |
| Matplotlib | Criação de gráficos de pizza e de barras |
| Hugging Face Transformers | Classificação de sentimentos com o modelo `nlptown/bert-base-multilingual-uncased-sentiment` |
| Sentence Transformers | Vetorização dos títulos com `distiluse-base-multilingual-cased-v1` |
| Scikit-learn | Agrupamento com `KMeans` em seis clusters |
| WordCloud e NLTK | Nuvem de palavras com remoção de *stopwords* em português |
| Instant Data Scraper | Extração dos dados apresentados no trabalho |

## Metodologia

1. **Coleta e preparação:** extração de reclamações do Reclame Aqui e organização em planilha Excel.
2. **Análise descritiva:** contagem dos status e visualização em gráficos de barras e pizza.
3. **Análise temporal:** conversão aproximada de expressões como “há X dias” e “há X meses” em número de dias, com cálculo da média por status. Para meses, o código adota 30 dias.
4. **Análise de sentimentos:** classificação dos títulos como negativos, neutros ou positivos a partir das categorias de estrelas previstas no modelo multilíngue.
5. **Agrupamento temático:** criação de vetores semânticos dos títulos e aplicação de `KMeans` com seis grupos, seguida de inspeção de exemplos para interpretação dos temas.
6. **Análise textual:** criação de nuvem de palavras a partir dos títulos, removendo palavras comuns e termos personalizados.

## Principais resultados

Os resultados a seguir foram apresentados pelo grupo na entrega final do projeto e referem-se à amostra analisada, **não à totalidade das reclamações da empresa**.

### Status das reclamações

- **46,7%**: resolvidas;
- **41,6%**: respondidas;
- **9,6%**: não respondidas.

A apresentação também identifica uma parcela de reclamações **não resolvidas**. Os percentuais acima estão arredondados e não incluem essa categoria separadamente.

### Análise de sentimentos

| Sentimento | Percentual |
| --- | ---: |
| Negativo | **86,7%** |
| Positivo | **8,2%** |
| Neutro | **5,1%** |

A classificação foi aplicada aos **títulos** das reclamações, não ao texto completo. Os resultados representam estimativas do modelo utilizado.

### Agrupamento dos tipos de problemas

Foram identificados **seis clusters** de títulos semelhantes, interpretados na apresentação como:

- Erros operacionais nos serviços;
- Falta de transparência nos serviços;
- Cobrança indevida;
- Lentidão no atendimento;
- Inflexibilidade em alterações contratuais;
- Lentidão no serviço oferecido.

Os rótulos dos grupos foram atribuídos por interpretação dos exemplos, e não produzidos automaticamente como categorias verificadas.

### Palavras recorrentes

A nuvem de palavras destacou termos relacionados a **atendimento**, **cobrança** e **informe de rendimento**, indicando assuntos relevantes para investigação.

## Conclusões

Com base na amostra, o grupo discutiu oportunidades de melhoria no atendimento, maior clareza na comunicação sobre cobranças e investigação de possíveis problemas operacionais. Uma das recomendações foi avaliar o uso de automação e inteligência artificial para lidar com dúvidas recorrentes e encaminhar solicitações.

**Limitação importante:** as reclamações analisadas não permitem determinar, por si só, as causas dos problemas relatados nem representar todos os clientes da empresa.

## Autoria e contexto acadêmico

**Projeto acadêmico desenvolvido em grupo.**

**Disciplina:** EAC0582 – Tópicos de Tecnologia nos Negócios, FEA-USP, 1º semestre de 2025.

**Docente:** Prof. Dr. Edgard Cornacchione.

Este repositório tem finalidade **educacional e de portfólio** e não possui vínculo oficial com a Contabilizei ou com o Reclame Aqui.
