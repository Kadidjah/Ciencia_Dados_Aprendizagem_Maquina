# Atividade Prática — Detetives dos Dados

## Ciência de Dados e Aprendizagem de Máquina — Aula 01

**Tema:** Introdução à Ciência de Dados e Big Data
**Metodologia:** Trabalho em equipe
**Tempo:** 20 minutos
**Entregável:** Mapa do Problema de Ciência de Dados

---

## 1. Identificação da equipe

| Campo             | Resposta |
| ----------------- | -------- |
| **Turma:**        | Sistemas de Informação           |
| **Data:**         | 19/08        |
| **Equipe:**       | Mídia Digital e Dados          |
| **Integrante 1:** | Filipe Costa 1          |
| **Integrante 2:** | Filipe Santos 2          |
| **Integrante 3:** | Preencher Nome 3          |
| **Integrante 4:** | Preencher Nome 4          |
| **Integrante 5:** | Preencher Nome 5          |

---

## 2. Objetivo da atividade

Nesta atividade, sua equipe deverá analisar um **problema real** e pensar como uma equipe de Ciência de Dados poderia utilizar dados para compreender a situação e apoiar uma decisão.

O objetivo não é desenvolver um sistema ou modelo de Machine Learning neste momento.

O objetivo é aprender a **pensar como um cientista de dados**:

> **Problema → Dados → Informação → Análise → Decisão → Benefício**

---

## 3. Escolha do problema

Escolha uma área para investigar:

* [ ] Comércio
* [ ] Banco
* [ ] Saúde
* [ ] Transporte
* [ ] Educação
* [ ] Entretenimento
* [ ] Indústria
* [ ] Meio ambiente
* [ ] Esportes
* [x] Outra: Mídia e Plataformas Digitais

### Problema escolhido

**Descreva, em poucas linhas, o problema que sua equipe pretende analisar.**

> A alta disseminação de notícias falsas (fake news) e conteúdos sensacionalistas em redes sociais, que se espalham rapidamente antes que a moderação consiga agir, gerando desinformação em massa.
>
> ---
>
> ---

---

## 4. Quem possui esse problema?

Identifique a organização, grupo ou público afetado pelo problema.

**Quem possui ou enfrenta esse problema?**

> As empresas de tecnologia e plataformas de mídia social (como Meta, X/TikTok), que perdem credibilidade e sofrem pressões regulatórias.
>
> ---

### Quem é afetado pelo problema?

> Os usuários da plataforma e a sociedade em geral, que são expostos a informações incorretas e tomam decisões baseadas em dados falsos.
>
> ---

---

## 5. Por que esse problema é importante?

Explique por que vale a pena investigar esse problema utilizando dados.

**Qual é o impacto do problema?**

> Porque a desinformação afeta a saúde pública, processos democráticos e a segurança das pessoas.
>
> Para a empresa de mídia, o problema reduz a confiança do usuário na plataforma e afasta anunciantes importantes (impactando a receita financeira).
>
> ---

---

## 6. Qual decisão precisa ser tomada?

Imagine que sua equipe foi contratada para ajudar uma organização.

**Qual decisão a organização precisa tomar?**

> A liderança da plataforma precisa decidir quais algoritmos de moderação e penalização automática devem ser implementados para frear a viralização de conteúdos falsos sem prejudicar a liberdade de expressão legítima.
>
> ---

---

# 7. Identificação dos dados

Agora pense:

> **Quais dados seriam necessários para compreender esse problema?**

Liste pelo menos **5 dados**.

| Nº | Dado necessário | Por que esse dado é importante? |
| -: | --------------- | ------------------------------- |
|  1 | Taxa de compartilhamento (shares) | Permite identificar a velocidade com que o conteúdo está se propagando. |
|  2 | Histórico de denúncias dos usuários | Ajuda a mapear quais publicações estão sendo sinalizadas como duvidosas pela comunidade. |
|  3 | Perfil e histórico da conta que postou | Identifica se a postagem veio de um perfil autêntico ou de um robô (bot). |
|  4 | Tempo médio de permanência na página | Mostra se o usuário lê a matéria inteira ou apenas compartilha com base em títulos chamativos (clickbait). |
|  5 | Taxa de engajamento (comentários e reações) | Mede o nível de polarização ou reação emocional gerada pela postagem. |

### Exemplos

Podem ser considerados dados como:

* idade;
* localização;
* frequência;
* notas;
* compras;
* valores;
* horários;
* avaliações;
* histórico de utilização;
* registros de atendimento;
* imagens;
* textos;
* localização geográfica.

---

# 8. Que informações queremos descobrir?

Os dados, quando analisados, podem gerar informações úteis.

**O que sua equipe gostaria de descobrir a partir dos dados?**

### Pergunta 1

> Qual é o tempo médio que uma notícia falsa leva para atingir 10 mil compartilhamentos em comparação com uma notícia real?

### Pergunta 2

> Contas automatizadas (bots) são responsáveis por qual porcentagem da propagação inicial dessas notícias?

### Pergunta 3

> Quais palavras-chave ou temas geram mais reações emocionais e compartilhamentos sem leitura prévia?

### Pergunta 4

> Quais são os horários de pico em que as redes de desinformação mais atuam?

---

# 9. Quais padrões podemos procurar?

Pense como um cientista de dados.

Sua equipe poderia procurar:

* [x] Tendências
* [ ] Comparações
* [ ] Grupos semelhantes
* [x] Comportamentos recorrentes
* [x] Valores fora do padrão
* [ ] Relações entre variáveis
* [ ] Mudanças ao longo do tempo
* [ ] Outros: __________________________

### Explique um padrão que vocês gostariam de encontrar

> Procurar padrões de contas que publicam de forma massiva em horários idênticos (indicando comportamento de bot) e conteúdos que explodem em compartilhamentos nos primeiros minutos de postagem.
>
> ---

---

# 10. Qual análise poderia ser realizada?

Como os dados poderiam ser analisados?

Marque uma ou mais possibilidades:

* [x] Análise descritiva
* [ ] Comparação entre grupos
* [ ] Análise temporal
* [x] Visualização por gráficos
* [x] Identificação de padrões
* [x] Classificação
* [ ] Previsão
* [ ] Agrupamento
* [ ] Outra: __________________________

### Explique

> Utilizar classificação algorítmica para separar conteúdos confiáveis de suspeitos e gráficos de visualização de rede para entender como o fluxo de compartilhamento se espalha entre os usuários.

---

# 11. Qual decisão poderia ser tomada?

Depois de analisar os dados, imagine que sua equipe encontrou informações importantes.

**Que decisão poderia ser tomada com base nos resultados?**

> Reduzir automaticamente o alcance (diminuição de distribuição algorítmica) de conteúdos sinalizados como falsos e priorizar selos de verificação em fontes jornalísticas confiáveis.
>
> ---

---

# 12. Qual seria o benefício?

Qual seria o possível benefício da decisão para a organização ou para as pessoas envolvidas?

> Um ambiente digital mais saudável e seguro para os usuários, maior retenção de anunciantes preocupados com suas marcas e aumento da confiabilidade na plataforma de mídia.
>
> ---

---

# 13. Os 5 Vs do Big Data

Analise o problema escolhido pela equipe.

| V              | Pergunta                                                   | Resposta da equipe |
| -------------- | ---------------------------------------------------------- | ------------------ |
| **Volume**     | Existe uma grande quantidade de dados?                     | Sim, bilhões de posts e cliques diários. |
| **Velocidade** | Os dados são gerados ou processados rapidamente?           | Sim, notícias se espalham em segundos. |
| **Variedade**  | Existen diferentes tipos ou formatos de dados?             | Sim, textos, imagens, vídeos e metadados. |
| **Veracidade** | Os dados podem apresentar erros ou problemas de qualidade? | Sim, é o cerne do problema com informações falsas. |
| **Valor**      | Os dados podem gerar algum benefício ou apoiar decisões?   | Sim, ajudam a blindar a plataforma contra manipulações. |

### Qual dos 5 Vs is mais relevante para o problema?

> Veracidade e Velocidade.

### Justifique

> O maior desafio é identificar a falsidade da informação antes que ela se espalhe de forma incontrolável pela rede.
>
> ---

---

# 14. Mapa do Problema de Ciência de Dados

Complete o fluxo abaixo:

```text
┌─────────────────────┐
│       PROBLEMA      │
│  Disseminação de    │
│   fake news em      │
│   redes sociais     │
└──────────┬──────────┘
           ↓
┌─────────────────────┐
│        DADOS        │
│  Compartilhamentos, │
│ denúncias e perfis  │
│      de contas      │
└──────────┬──────────┘
           ↓
┌─────────────────────┐
│     INFORMAÇÕES     │
│   Velocidade de     │
│ propagação e origem │
│     dos boatos      │
└──────────┬──────────┘
           ↓
┌─────────────────────┐
│       ANÁLISE       │
│ Identificação de    │
│ padrões de bots e   │
│ conteúdos suspeitos │
└──────────┬──────────┘
           ↓
┌─────────────────────┐
│       DECISÃO       │
│  Reduzir alcance de │
│ conteúdos falsos e  │
│ destacar confiáveis │
└──────────┬──────────┘
           ↓
┌─────────────────────┐
│      BENEFÍCIO      │
│  Ambiente seguro e  │
│ maior confiança na  │
│      plataforma     
└─────────────────────┘

Resuma cada etapa
Problema:

Disseminação de fake news e conteúdos sensacionalistas.

Dados:

Taxas de compartilhamento, histórico de denúncias e perfis de contas.

Informação:

Velocidade que os boatos circulam e o impacto de contas automatizadas.

Análise:

Classificação de padrões de propagação e detecção de comportamentos de bots.

Decisão:

Aplicar restrição algorítmica em conteúdos falsos e promover fontes confiáveis.

Benefício:

Maior segurança para os usuários e credibilidade para a plataforma de mídia.

15. Preparação para apresentação
A equipe terá 2 minutos para apresentar sua proposta.

Organizem a apresentação seguindo esta estrutura:

1. Nosso problema
A rápida propagação de fake news em redes sociais prejudicando a sociedade e as plataformas.

2. Precisamos destes dados
Dados de compartilhamento, histórico de denúncias e metadados das contas propagadoras.

3. Queremos descobrir
O tempo que as notícias falsas levam para viralizar comparadas às verdadeiras e o papel dos bots.

4. Pretendemos analisar
O comportamento temporal das postagens e a classificação de confiabilidade do conteúdo.

5. A decisão poderia ser
Reduzir automaticamente o alcance de conteúdos falsos e sinalizar fontes confiáveis.

6. O benefício esperado é
Um ambiente digital mais confiável, ético e seguro para todos os usuários.

16. Checklist da equipe
Antes de entregar, confira:

[x] Definimos um problema real.

[x] Identificamos quem é afetado pelo problema.

[x] Explicamos por que o problema é importante.

[x] Identificamos pelo menos 5 dados necessários.

[x] Definimos perguntas que queremos responder.

[x] Identificamos possíveis padrões.

[x] Indicamos como os dados poderiam ser analisados.

[x] Definimos uma possível decisão.

[x] Identificamos o benefício esperado.

[x] Analisamos os 5 Vs do Big Data.

[x] Preenchemos o Mapa do Problema.

[x] Estamos preparados para apresentar em 2 minutos.

17. Reflexão final
Responda individualmente ou em equipe:

Ter muitos dados significa necessariamente tomar boas decisões? Por quê?

Resposta:

Não necessariamente. Ter um grande volume de dados (Big Data) só gera valor se os dados forem limpos, verificados e analisados corretamente. Dados de baixa qualidade ou mal interpretados podem levar a decisões equivocadas.

Entrega
Produto final
A equipe deverá entregar:

Mapa do Problema de Ciência de Dados

contendo:

Plaintext


Problema
   ↓
Dados necessários
   ↓
Informações desejadas
   ↓
Análise
   ↓
Decisão
   ↓
Benefício esperado
Formato sugerido: Markdown, PDF ou documento disponibilizado pelo professor.

Apresentação: 2 minutos por equipe.
