# Brawl-Analytics

# Sobre o projeto

O Brawl Analytics é uma plataforma voltada para a análise de dados do jogo Brawl Stars.

A proposta é criar um ambiente onde jogadores possam consultar e comparar o desempenho dos diferentes brawlers de acordo com o modo de jogo e o mapa em que estão sendo utilizados.

O sistema pretende apresentar informações como percentual de uso e taxa de vitória, permitindo que o usuário tenha uma visão mais clara de quais brawlers apresentam melhores resultados em determinados cenários.

Considerando o meu nível atual de conhecimento e a complexidade que o projeto pode alcançar, a ideia inicial é desenvolver uma versão simplificada da plataforma, concentrando-se na consulta e visualização das principais estatísticas.

A princípio, penso em criar um ambiente onde o usuário possa selecionar um modo de jogo e um mapa e visualizar os brawlers utilizados naquele cenário, juntamente com suas respectivas estatísticas.

* Permitir a consulta dos brawlers disponíveis;
* Permitir a consulta dos modos de jogo;
* Permitir a consulta dos mapas de cada modo;
* Exibir o percentual de uso dos brawlers;
* Exibir a taxa de vitória dos brawlers;
* Permitir a comparação entre diferentes brawlers;
* Exibir rankings dos brawlers de acordo com suas estatísticas.

---

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

Essas informações poderão ser utilizadas para identificar e organizar os diferentes personagens disponíveis no jogo.

---

## Modos de jogo

A plataforma também deverá trabalhar com os diferentes modos de jogo presentes no Brawl Stars.

Cada modo poderá possuir informações como:

```text
Modo de Jogo
├── ID
├── Nome
├── Descrição
```

Os modos serão utilizados para organizar as estatísticas e relacioná-las aos mapas disponíveis.

---

## Mapas

Os mapas serão associados aos respectivos modos de jogo.

Cada mapa poderá possuir informações como:

```text
Mapa
├── ID
├── Nome
├── Modo de jogo
```

Dessa forma, será possível identificar em qual modo cada mapa está disponível.

---

## Estatísticas

O principal recurso do Brawl Analytics será a consulta das estatísticas dos brawlers.

As informações poderão ser apresentadas de acordo com a combinação entre brawler, modo de jogo e mapa.

Exemplo:

```text
Estatística
├── ID
├── Brawler
├── Mapa
├── Modo de jogo
├── Percentual de uso
├── Taxa de vitória
```

A partir dessas informações, o usuário poderá visualizar quais brawlers apresentam maior utilização e melhores resultados em cada cenário.

## Consultas e comparações

O usuário poderá selecionar um modo de jogo e um mapa para visualizar as estatísticas correspondentes.

A plataforma poderá apresentar:

* Brawlers mais utilizados;
* Brawlers com maior taxa de vitória;
* Comparação entre diferentes brawlers;
* Percentual de uso de cada brawler.

A proposta inicial é manter o sistema focado na consulta e análise dessas informações, podendo novas funcionalidades ser adicionadas conforme o desenvolvimento do projeto avance.
