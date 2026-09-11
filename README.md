# Brawl Analytics

## Sobre o projeto

O **Brawl Analytics** é uma plataforma voltada para a análise de dados do jogo **Brawl Stars**.

A proposta é permitir que jogadores consultem e comparem o desempenho dos diferentes brawlers de acordo com o mapa e o modo de jogo em que estão sendo utilizados.

O sistema pretende apresentar informações como **percentual de uso** e **taxa de vitória**, permitindo uma visualização mais clara de quais brawlers apresentam melhores resultados em determinados cenários.

Considerando a complexidade do projeto e o tempo disponível para seu desenvolvimento, a proposta é construir inicialmente uma versão **simplificada e funcional**, concentrada na consulta e visualização das principais estatísticas.

## Objetivos

O Brawl Analytics deverá permitir inicialmente:

* Consultar os brawlers disponíveis;
* Consultar os modos de jogo;
* Consultar os mapas e seus respectivos modos;
* Visualizar o percentual de uso dos brawlers;
* Visualizar a taxa de vitória dos brawlers;
* Comparar diferentes brawlers;
* Visualizar rankings de acordo com suas estatísticas.

## Dados

Os dados utilizados pelo sistema deverão ser obtidos a partir de fontes relacionadas ao Brawl Stars, de acordo com as informações disponibilizadas por cada fonte.

A aplicação poderá trabalhar com dados básicos, como brawlers, mapas e modos de jogo, além de dados estatísticos.

As estatísticas serão armazenadas de acordo com o formato disponibilizado pela fonte de dados escolhida. Quando a fonte disponibilizar informações necessárias para o cálculo da taxa de vitória, como quantidade de vitórias e partidas, o sistema poderá realizar esse cálculo. Caso a própria fonte já disponibilize a taxa de vitória, não será necessário armazenar as informações utilizadas para calculá-la apenas para reproduzir o mesmo valor.

Dessa forma, a estrutura do banco será definida de acordo com as necessidades reais do projeto e com os dados que poderão ser obtidos das fontes utilizadas.

## Brawlers

Os brawlers serão uma das principais entidades da plataforma.

Cada brawler poderá possuir informações como:

```text
Brawler
├── ID
├── Nome
├── Raridade
├── Classe
├── Data de lançamento
└── Status
```

Essas informações serão utilizadas para identificar e organizar os diferentes personagens disponíveis no jogo.

## Modos de jogo

A plataforma também trabalhará com os diferentes modos de jogo presentes no Brawl Stars.

Cada modo poderá possuir informações como:

```text
Modo de Jogo
├── ID
├── Nome
├── Descrição
└── Status
```

Os modos de jogo serão utilizados para organizar os mapas disponíveis e permitir que o usuário consulte os dados de acordo com o cenário desejado.

## Mapas

Os mapas serão associados aos respectivos modos de jogo.

Cada mapa poderá possuir informações como:

```text
Mapa
├── ID
├── Nome
├── Modo de jogo
└── Status
```

Dessa forma, ao identificar um mapa, será possível determinar também a qual modo de jogo ele está relacionado.

## Estatísticas

As estatísticas serão o principal recurso de análise do Brawl Analytics.

Uma estatística representará o desempenho de um determinado **brawler em um determinado mapa**.

Como cada mapa está associado a um modo de jogo, não será necessário armazenar novamente o modo de jogo dentro da estatística.

A estrutura conceitual poderá ser representada como:

```text
Estatística
├── ID
├── Brawler
├── Mapa
├── Percentual de uso
└── Taxa de vitória
```

A quantidade de partidas, vitórias ou outras informações auxiliares não será definida antecipadamente como parte obrigatória da tabela. Isso dependerá dos dados realmente disponibilizados pela fonte utilizada pelo projeto.

## Relações entre as informações

A estrutura inicial do projeto considera as seguintes relações:

```text
Modo de Jogo
     │
     │ 1:N
     ↓
   Mapas
     │
     │ 1:N
     ↓
Estatísticas
     ↑
     │ N:1
 Brawlers
```

Isso significa que:

* Um modo de jogo pode possuir vários mapas;
* Um mapa pertence a um modo de jogo;
* Um brawler pode possuir várias estatísticas;
* Um mapa pode possuir várias estatísticas;
* Cada estatística está relacionada a um brawler e a um mapa.

## Consultas e comparações

O usuário poderá selecionar um modo de jogo e um mapa para visualizar as estatísticas correspondentes.

A plataforma poderá apresentar:

* Brawlers mais utilizados;
* Brawlers com maior taxa de vitória;
* Percentual de uso dos brawlers;
* Comparação entre diferentes brawlers;
* Rankings de acordo com as estatísticas disponíveis.

A proposta inicial é manter o sistema focado na consulta e análise dessas informações, evitando funcionalidades que aumentem desnecessariamente a complexidade do projeto.
