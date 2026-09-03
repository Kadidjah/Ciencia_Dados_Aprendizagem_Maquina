# Aula — Python para Ciência de Dados: Manipulação de Dados Tabulares com Pandas

**Curso:** Sistemas de Informação  
**Duração:** 1h30 (90 minutos)  
**Unidade:** II — Análise e Ciência de Dados  
**Pré-requisitos:** fundamentos de Python; pipeline de Ciência de Dados (19/08); análise exploratória e qualidade dos dados (26/08).  
**Referência principal:** André Carlos de Carvalho, Angelo Menezes e Robson Bonidia. *Ciência de Dados — Fundamentos e Aplicações*, capítulo “Python para Ciência de Dados”. <https://bonidia.github.io/cd-fundamentos/cp2.html>

## 1. Visão geral

### Problema norteador

> A coordenação de TI recebeu dados de chamados de suporte e precisa responder: onde estão os principais gargalos, quais registros exigem atenção e o atendimento está cumprindo o SLA?

Os estudantes assumirão o papel de analistas de dados. O mesmo dataset será usado da leitura à síntese final, formando uma sequência coerente: **problema → dados → inspeção → seleção/filtro → transformação → sumarização → interpretação → decisão**.

### Objetivo geral

Compreender e utilizar funcionalidades básicas do Pandas para carregar, explorar, selecionar, filtrar, transformar e analisar dados tabulares.

### Objetivos específicos

Ao final, os estudantes deverão ser capazes de:

- explicar a utilidade do Pandas em um processo de Ciência de Dados;
- distinguir `Series` de `DataFrame`;
- criar um `DataFrame` e carregar um CSV;
- inspecionar estrutura, tipos, ausências e estatísticas com `head()`, `tail()`, `info()`, `describe()`, `shape` e `columns`;
- selecionar linhas e colunas com colchetes, `loc` e `iloc`;
- filtrar registros por uma ou mais condições;
- criar ou alterar colunas;
- resumir dados com contagens, médias e `groupby()`;
- comunicar uma descoberta sustentada pelos dados.

## 2. Integração com as aulas anteriores

| Aula anterior | Conceito retomado | Aplicação nesta aula |
|---|---|---|
| 19/08 — Fundamentos e ciclo de dados | problema → coleta → preparação → análise → interpretação → decisão | o notebook percorre o pipeline a partir de uma pergunta de negócio |
| 26/08 — EDA | estrutura, tipos, ausências, padrões e outliers | `info()`, `describe()`, filtros e agregações revelam problemas e padrões |
| Continuidade | visualização e interpretação | as tabelas sumarizadas ficam prontas para gerar gráficos na aula seguinte |

## 3. Plano de aula resumido

| Tempo | Etapa | Conteúdo | Atividade | Objetivo |
|---:|---|---|---|---|
| 0–10 min | Abertura e retomada | pipeline, EDA e problema dos chamados | pense–compare–compartilhe sobre perguntas possíveis | ativar conhecimentos prévios e dar propósito à análise |
| 10–20 min | Introdução ao Pandas | Pandas, `Series`, `DataFrame`, linhas, colunas e índice | criação coletiva de estruturas pequenas | compreender o modelo tabular |
| 20–40 min | Demonstração prática | CSV, inspeção, seleção, filtros e nova coluna | professor programa e estudantes predizem as saídas | modelar o raciocínio antes da sintaxe |
| 40–60 min | Prática orientada | exploração progressiva do mesmo dataset | exercícios 1 a 5, individual/duplas | adquirir fluência nas operações básicas |
| 60–80 min | Desafio prático | SLA, filtros, transformação, agregação e interpretação | investigação em duplas com breve relato | integrar conceitos com autonomia |
| 80–90 min | Fechamento e avaliação | síntese, erros comuns, perguntas rápidas e exit ticket | checagem formativa + entrega de uma célula e uma frase | verificar aprendizagem e orientar próximos estudos |

**Tempo ativo:** 50 minutos (prática orientada, desafio e exit ticket), equivalente a 55,6% da aula.

## 4. Roteiro de fala do professor

### 0–10 min — Abertura e retomada

“Nas aulas anteriores, vimos que Ciência de Dados começa com um problema e termina com uma decisão. Hoje vamos trabalhar no trecho central do pipeline: transformar uma tabela bruta em evidências que respondam a perguntas.”

Mostre cinco linhas do CSV e pergunte:

- Que decisões uma coordenação de TI poderia tomar com esses dados?
- Que coluna representa uma medida? Que colunas representam categorias?
- O que precisamos verificar antes de calcular médias?

Registre duas perguntas de negócio, por exemplo: “Quais categorias demoram mais?” e “Quais chamados ultrapassaram o SLA?”. Relacione valores ausentes e o tempo de 120 horas à EDA de 26/08, sem corrigir os dados ainda.

### 10–20 min — Introdução ao Pandas

“Pandas é uma biblioteca Python voltada à manipulação e análise de dados rotulados. Uma `Series` é uma estrutura unidimensional; um `DataFrame` é bidimensional, semelhante a uma tabela, e cada coluna é uma `Series`.”

Demonstre uma `Series` e um `DataFrame` pequenos. Destaque que o índice identifica linhas e não deve ser confundido com uma coluna de negócio. Peça que a turma antecipe o tipo do resultado de `df['setor']` e de `df[['setor']]`.

### 20–40 min — Demonstração prática

Antes de executar cada comando, peça uma previsão. Após a saída, pergunte o que ela permite concluir. Use esta sequência:

1. `import pandas as pd`: disponibiliza a biblioteca pelo alias convencional `pd`.
2. `pd.read_csv(...)`: lê o arquivo e devolve um `DataFrame`.
3. `head()`/`tail()`: amostram o início/fim; não comprovam qualidade do dataset inteiro.
4. `shape`/`columns`: revelam dimensões e nomes das variáveis; são atributos, sem parênteses.
5. `info()`: mostra tipos e contagem de valores não nulos; é essencial antes de analisar.
6. `describe()`: sumariza variáveis numéricas; a média pode ser influenciada pelo valor de 120 horas.
7. seleção: uma coluna, várias colunas, `loc` por rótulo e `iloc` por posição.
8. filtros: máscara booleana, parênteses e operadores `&`/`|`.
9. transformação: criação de `tempo_dias` e, depois, de indicadores de SLA.

### 40–60 min — Prática orientada

Organize duplas com papéis alternados: uma pessoa escreve o código e a outra explica o resultado. Após cada exercício, escolha uma dupla para mostrar uma solução e outra para interpretar a saída. Circule fazendo perguntas, sem fornecer a expressão pronta.

### 60–80 min — Desafio

“Agora vocês receberão uma pergunta, não uma receita. A solução precisa conter código correto e uma conclusão em linguagem de negócio.”

Exija quatro evidências: inspeção, recorte relevante, coluna derivada e resumo por grupo. Nos cinco minutos finais, duas duplas apresentam uma descoberta em até 45 segundos.

### 80–90 min — Fechamento

Retome o fluxo realizado e diferencie “executar comandos” de “produzir evidência”. Corrija coletivamente as perguntas rápidas. No exit ticket, cada estudante envia uma célula de código e uma frase interpretativa.

## 5. Conceitos e demonstrações

### 5.1 `Series` e `DataFrame`

```python
import pandas as pd

prioridades = pd.Series(["Alta", "Média", "Baixa"], name="prioridade")
print(prioridades)

exemplo = pd.DataFrame({
    "id_chamado": ["CH001", "CH002"],
    "setor": ["Financeiro", "Acadêmico"],
    "tempo_horas": [3.5, 12.0]
})
exemplo
```

`Series` representa uma dimensão com rótulos. `DataFrame` representa duas dimensões: linhas (observações) e colunas (variáveis).

### 5.2 Carregamento e inspeção

```python
import pandas as pd

df = pd.read_csv("chamados_suporte_ti.csv")
df.head()
df.tail(3)
df.shape
df.columns
df.info()
df.describe()
```

- `head(n)` e `tail(n)` oferecem uma visão rápida das extremidades.
- `shape` retorna `(linhas, colunas)`.
- `columns` lista os rótulos das colunas.
- `info()` imprime tipos, valores não nulos e memória; seu retorno é `None`.
- `describe()` resume colunas numéricas por padrão; use `include="all"` apenas quando precisar incluir categorias.

### 5.3 Seleção de dados

```python
df["setor"]                         # Series
df[["id_chamado", "setor"]]       # DataFrame
df.loc[0:2, ["id_chamado", "setor"]]  # rótulos; limite final incluído
df.iloc[0:3, 0:2]                   # posições; limite final excluído
```

### 5.4 Filtros condicionais

```python
df[df["prioridade"] == "Alta"]

df[(df["prioridade"] == "Alta") &
   (df["status"] == "Resolvido")]

df[df["categoria"].isin(["Acesso", "Rede"])]
```

Em Pandas, combine condições com `&` (e) ou `|` (ou), envolvendo cada comparação entre parênteses.

### 5.5 Criação e alteração de colunas

```python
df["data_abertura"] = pd.to_datetime(df["data_abertura"])
df["tempo_dias"] = df["tempo_resolucao_horas"] / 24
df["satisfacao"] = df["satisfacao"].astype("Int64")
```

A atribuição a `df['nova_coluna']` cria a coluna; se o nome já existir, altera seus valores. `Int64` (I maiúsculo) aceita inteiros e ausências.

### 5.6 Agregações básicas

```python
df["status"].value_counts()
df["tempo_resolucao_horas"].mean()
df.groupby("categoria")["tempo_resolucao_horas"].mean().sort_values(ascending=False)
```

`groupby()` segue a lógica dividir → aplicar → combinar. A saída precisa ser interpretada no contexto; médias ignoram valores ausentes por padrão.

## 6. Dataset para copiar

Salve o conteúdo abaixo como `chamados_suporte_ti.csv` no mesmo diretório do notebook:

```csv
id_chamado,data_abertura,setor,categoria,prioridade,status,tempo_resolucao_horas,satisfacao,reaberto,analista
CH001,2026-08-20,Financeiro,Acesso,Alta,Resolvido,3.5,5,Não,Ana
CH002,2026-08-20,Acadêmico,Sistema lento,Média,Resolvido,12.0,4,Não,Bruno
CH003,2026-08-21,Biblioteca,Impressora,Baixa,Resolvido,30.0,3,Sim,Carla
CH004,2026-08-21,Financeiro,Erro de sistema,Crítica,Resolvido,2.0,5,Não,Ana
CH005,2026-08-22,RH,Acesso,Média,Em andamento,,,Não,Diego
CH006,2026-08-22,Acadêmico,Rede,Alta,Resolvido,9.5,2,Sim,Bruno
CH007,2026-08-23,Laboratório,Hardware,Média,Resolvido,20.0,4,Não,Carla
CH008,2026-08-23,Biblioteca,Sistema lento,Baixa,Resolvido,45.0,4,Não,Diego
CH009,2026-08-24,RH,Erro de sistema,Alta,Resolvido,7.0,5,Não,Ana
CH010,2026-08-24,Laboratório,Rede,Crítica,Resolvido,6.0,2,Sim,Bruno
CH011,2026-08-25,Financeiro,Hardware,Média,Aberto,,,Não,Carla
CH012,2026-08-25,Acadêmico,Acesso,Baixa,Resolvido,10.0,5,Não,Diego
CH013,2026-08-26,Biblioteca,Rede,Média,Resolvido,18.0,4,Não,Ana
CH014,2026-08-26,RH,Sistema lento,Alta,Resolvido,14.0,3,Sim,Bruno
CH015,2026-08-27,Laboratório,Erro de sistema,Crítica,Resolvido,3.0,5,Não,Carla
CH016,2026-08-27,Financeiro,Acesso,Baixa,Resolvido,52.0,2,Sim,Diego
CH017,2026-08-28,Acadêmico,Hardware,Média,Resolvido,16.0,4,Não,Ana
CH018,2026-08-28,Laboratório,Sistema lento,Média,Resolvido,120.0,1,Sim,Bruno
```

## 7. Lista de exercícios para os estudantes (sem respostas)

### Exercício 1 — Reconhecendo o dataset

**Enunciado:** carregue o CSV em `df`. Exiba as cinco primeiras e as três últimas linhas. Informe quantas linhas e colunas existem e liste os nomes das colunas.  
**Objetivo de aprendizagem:** carregar e reconhecer a estrutura de dados tabulares.  
**Dados necessários:** `chamados_suporte_ti.csv`.  
**Comandos/conceitos:** `read_csv()`, `head()`, `tail()`, `shape`, `columns`.  
**Nível:** básico.  
**Resposta esperada:** código executável e uma frase descrevendo dimensões e variáveis.

### Exercício 2 — Tipos, ausências e resumo

**Enunciado:** use `info()` e `describe()`. Quais colunas possuem valores ausentes? Qual valor merece investigação por ser muito maior que a maioria dos tempos?  
**Objetivo de aprendizagem:** avaliar estrutura, tipos, completude e estatísticas descritivas.  
**Dados necessários:** DataFrame `df`.  
**Comandos/conceitos:** `info()`, `describe()`.  
**Nível:** básico.  
**Resposta esperada:** identificação das ausências e interpretação do possível outlier.

### Exercício 3 — Seleção de linhas e colunas

**Enunciado:** (a) selecione `id_chamado`, `setor`, `prioridade` e `status`; (b) usando posições, mostre as cinco primeiras linhas e as quatro primeiras colunas; (c) explique a diferença entre selecionar uma coluna e filtrar linhas.  
**Objetivo de aprendizagem:** distinguir projeção de colunas, recorte posicional e filtro.  
**Dados necessários:** DataFrame `df`.  
**Comandos/conceitos:** listas de colunas, `iloc`.  
**Nível:** básico.  
**Resposta esperada:** dois recortes corretos e explicação conceitual.

### Exercício 4 — Filtros de negócio

**Enunciado:** encontre: (a) chamados de prioridade Alta; (b) chamados resolvidos com tempo superior a 24 horas; (c) chamados de Rede ou Acesso. Quantos registros há em cada resultado?  
**Objetivo de aprendizagem:** construir máscaras booleanas com uma ou mais condições.  
**Dados necessários:** DataFrame `df`.  
**Comandos/conceitos:** comparação, `&`, `isin()`, `shape`.  
**Nível:** intermediário.  
**Resposta esperada:** três DataFrames filtrados, suas contagens e breve interpretação.

### Exercício 5 — Nova informação e resumo

**Enunciado:** converta `data_abertura` para data, crie `tempo_dias` a partir de `tempo_resolucao_horas` e calcule o tempo médio de resolução por categoria em ordem decrescente. Qual categoria tem a maior média? A média parece ser influenciada por algum registro?  
**Objetivo de aprendizagem:** transformar colunas, agregar e interpretar.  
**Dados necessários:** DataFrame `df`.  
**Comandos/conceitos:** `to_datetime()`, atribuição, divisão vetorizada, `groupby()`, `mean()`, `sort_values()`.  
**Nível:** intermediário.  
**Resposta esperada:** coluna derivada, tabela de médias e conclusão com ressalva sobre o outlier.

## 8. Atividade final — Desafio “Painel de atenção do suporte”

### Situação

A coordenação definiu os seguintes limites de SLA: Crítica = 4 h, Alta = 8 h, Média = 24 h e Baixa = 48 h. Sua dupla deverá identificar onde o processo de suporte precisa de atenção.

### Entregável

Um notebook com:

1. inspeção do DataFrame (`shape`, `info()` e pelo menos uma estatística);
2. seleção das colunas relevantes;
3. filtro de chamados resolvidos;
4. criação de `limite_sla_horas` e `dentro_sla`;
5. quantidade e percentual de chamados resolvidos dentro/fora do SLA;
6. tempo médio por categoria;
7. uma conclusão de 3 a 5 linhas com duas evidências numéricas e uma recomendação.

### Regras

- Preserve os valores ausentes; explique por que chamados abertos/em andamento não entram na avaliação do tempo final.
- Não remova o valor de 120 h sem justificativa. Compare-o com as demais observações e registre a decisão.
- Cada conclusão deve citar a operação que gerou a evidência.

**Objetivo de aprendizagem:** integrar exploração, seleção, filtro, transformação, agregação e comunicação.  
**Comandos/conceitos:** `info()`, seleção, máscara booleana, `map()`, nova coluna, `value_counts()`, `mean()`, `groupby()`.  
**Nível:** desafio.  
**Resposta esperada:** notebook reproduzível e interpretação fundamentada.

### Critérios de avaliação (10 pontos)

| Critério | Pontos |
|---|---:|
| Carregamento e inspeção adequados | 1,5 |
| Seleção e filtros corretos | 2,0 |
| Criação das colunas de SLA | 2,0 |
| Sumarizações corretas | 2,0 |
| Interpretação com evidências e recomendação | 2,0 |
| Clareza e organização do notebook | 0,5 |

## 9. Avaliação formativa

### Perguntas durante a aula

1. Como descobrir quantas linhas e colunas existem sem imprimir o DataFrame inteiro?
2. Por que `shape` não usa parênteses, enquanto `info()` usa?
3. Qual é a diferença entre `df['setor']` e `df[['setor']]`?
4. Quando usar `loc` e quando usar `iloc`?
5. Por que cada condição precisa de parênteses ao usar `&`?
6. O que `info()` revela que `head()` não revela?
7. Por que uma média pode induzir a uma conclusão inadequada diante de um outlier?
8. Se criarmos uma informação a partir de duas colunas, por que é melhor usar operações vetorizadas em vez de percorrer linha a linha?

### Checagem rápida (3–5 perguntas)

1. Qual comando mostra os tipos e a quantidade de valores não nulos?
2. Escreva uma expressão para selecionar chamados do setor Financeiro.
3. Qual resultado é uma `Series`: `df['status']` ou `df[['status']]`?
4. O que `df.groupby('categoria')['tempo_resolucao_horas'].mean()` responde?
5. Cite um cuidado necessário antes de interpretar `describe()`.

### Exit ticket (últimos 3 minutos)

Escreva uma única expressão Pandas que selecione os chamados reabertos e mostre apenas `id_chamado`, `categoria` e `tempo_resolucao_horas`. Em seguida, escreva uma frase explicando que decisão essa informação pode apoiar.

## 10. Erros comuns e como evitá-los

| Erro | Exemplo | Como evitar |
|---|---|---|
| usar parênteses em atributo | `df.shape()` | use `df.shape` e `df.columns` |
| usar `and`/`or` em Series | `cond1 and cond2` | use `(cond1) & (cond2)` ou `(cond1) | (cond2)` |
| omitir parênteses nos filtros compostos | `df[a > 1 & b == 2]` | coloque cada comparação entre parênteses |
| confundir seleção com filtro | `df['setor']` não escolhe linhas | seleção escolhe variáveis; filtro escolhe observações |
| confundir `loc` e `iloc` | passar nomes ao `iloc` | `loc` usa rótulos; `iloc` usa posições inteiras |
| sobrescrever sem conferir | alterar coluna e seguir | valide com `head()`, `info()` ou contagens |
| ignorar ausências/outliers | calcular e aceitar a saída | inspecione completude, distribuição e contexto |

## 11. Gabarito e soluções para o professor

### Exercício 1

```python
import pandas as pd
df = pd.read_csv("chamados_suporte_ti.csv")
df.head()
df.tail(3)
print(df.shape)
print(df.columns.tolist())
```

**Comentário:** a base possui 18 linhas e 10 colunas. `head()` e `tail()` verificam rapidamente se leitura e separação parecem corretas.

### Exercício 2

```python
df.info()
df.describe()
```

**Comentário:** `tempo_resolucao_horas` e `satisfacao` têm 16 valores não nulos (duas ausências em cada). O máximo de 120 h em `tempo_resolucao_horas` merece investigação: pode ser válido, erro ou caso excepcional. Não se deve removê-lo automaticamente.

### Exercício 3

```python
recorte_colunas = df[["id_chamado", "setor", "prioridade", "status"]]
recorte_posicional = df.iloc[0:5, 0:4]
display(recorte_colunas.head())
display(recorte_posicional)
```

**Comentário:** selecionar colunas escolhe quais variáveis serão exibidas; filtrar linhas escolhe quais observações atendem a uma condição.

### Exercício 4

```python
altos = df[df["prioridade"] == "Alta"]
lentos = df[(df["status"] == "Resolvido") &
            (df["tempo_resolucao_horas"] > 24)]
rede_ou_acesso = df[df["categoria"].isin(["Rede", "Acesso"])]

print("Alta:", altos.shape[0])
print("Resolvidos acima de 24h:", lentos.shape[0])
print("Rede ou Acesso:", rede_ou_acesso.shape[0])
```

**Comentário:** resultados esperados: 4 chamados de prioridade Alta; 4 resolvidos acima de 24 h; 7 de Rede ou Acesso.

### Exercício 5

```python
df["data_abertura"] = pd.to_datetime(df["data_abertura"])
df["tempo_dias"] = df["tempo_resolucao_horas"] / 24

media_categoria = (
    df.groupby("categoria")["tempo_resolucao_horas"]
      .mean()
      .sort_values(ascending=False)
)
media_categoria
```

**Comentário:** `Sistema lento` tem a maior média (47,75 h), fortemente influenciada pelo registro de 120 h. Isso é uma descoberta para investigação, não licença para apagar o registro.

### Desafio — solução de referência

```python
import pandas as pd

df = pd.read_csv("chamados_suporte_ti.csv")
print(df.shape)
df.info()
display(df.describe())

colunas = [
    "id_chamado", "categoria", "prioridade", "status",
    "tempo_resolucao_horas", "satisfacao", "reaberto"
]
analise = df[colunas].copy()
resolvidos = analise[analise["status"] == "Resolvido"].copy()

limites = {"Crítica": 4, "Alta": 8, "Média": 24, "Baixa": 48}
resolvidos["limite_sla_horas"] = resolvidos["prioridade"].map(limites)
resolvidos["dentro_sla"] = (
    resolvidos["tempo_resolucao_horas"] <= resolvidos["limite_sla_horas"]
)

contagem_sla = resolvidos["dentro_sla"].value_counts()
percentual_sla = resolvidos["dentro_sla"].value_counts(normalize=True).mul(100).round(1)
media_categoria = (
    resolvidos.groupby("categoria")["tempo_resolucao_horas"]
              .mean()
              .sort_values(ascending=False)
              .round(2)
)

display(resolvidos)
display(contagem_sla)
display(percentual_sla)
display(media_categoria)
```

**Resultados esperados:** 16 chamados resolvidos; 11 dentro do SLA (68,8%) e 5 fora (31,2%). `Sistema lento` apresenta a maior média, 47,75 h. Uma conclusão adequada ressalta que o chamado de 120 h eleva essa média e recomenda investigar os casos fora do SLA, sobretudo o outlier, antes de decidir sobre capacidade ou processo.

### Gabarito da checagem rápida

1. `df.info()`.
2. `df[df['setor'] == 'Financeiro']`.
3. `df['status']`.
4. A média de tempo de resolução para cada categoria.
5. Verificar tipos, ausências, tamanho da amostra e possíveis outliers.

### Gabarito do exit ticket

```python
df.loc[
    df["reaberto"] == "Sim",
    ["id_chamado", "categoria", "tempo_resolucao_horas"]
]
```

**Interpretação possível:** o recorte apoia a investigação das categorias e chamados com retrabalho, ajudando a priorizar análise de causa-raiz.

## 12. Código completo para notebook/Google Colab

O arquivo `aula_pandas_chamados.ipynb` acompanha este material com células separadas em: contexto; importação; estruturas básicas; carregamento; inspeção; seleção; filtros; transformação; agregação; área do estudante; desafio; e gabarito do professor.

## 13. Estudos posteriores

- praticar ordenação com `sort_values()` e consultas com `query()`;
- revisar tipos, datas, valores ausentes, duplicatas e outliers;
- usar as tabelas agregadas para construir visualizações;
- avançar para combinação de DataFrames (`merge`, `concat`) e exportação (`to_csv`), mantendo a progressão proposta no capítulo de referência.
