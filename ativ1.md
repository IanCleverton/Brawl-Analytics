# Atividade 1

## 1. Quais tabelas você definiu inicialmente?

Inicialmente, foram definidas quatro tabelas para o projeto Brawl Analytics:

- `brawlers`: armazena as informações dos brawlers;
- `game_modes`: armazena os modos de jogo;
- `maps`: armazena os mapas disponíveis;
- `statistics`: armazena as estatísticas dos brawlers de acordo com o modo de jogo e o mapa.

## 2. Você utilizou migrations? Se sim, quantas migrations? Descreva em uma frase o que cada uma faz.

Não. Até o momento, não utilizei migrations, pois a implementação da estrutura do banco de dados ainda não foi realizada. A estrutura inicial das tabelas já foi definida e será criada posteriormente por meio de uma migration.

## 3. Qual o caminho do arquivo que gera a seed do seu banco?

O caminho do arquivo que gera a seed do banco é `backend/seed.sql`.

## 4. Quais os endpoints que você irá implementar inicialmente? Cada endpoint deve ser um método e um path. Explique em um parágrafo por que você resolveu priorizar a implementação desses endpoints.

Inicialmente, serão implementados os seguintes endpoints:

- `GET /api/brawlers`
- `GET /api/game-modes`
- `GET /api/maps`
- `GET /api/statistics`

Esses endpoints foram priorizados porque representam as principais informações que serão disponibilizadas pelo Brawl Analytics. O sistema precisa permitir que o usuário consulte os brawlers, os modos de jogo, os mapas e as estatísticas relacionadas a esses elementos. Dessa forma, esses endpoints formam a base das consultas que serão utilizadas inicialmente pela aplicação.

## 5. Você está usando algum framework para escrever os endpoints da sua API? Se sim, qual?

Sim. O framework escolhido para a implementação dos endpoints da API é o Express, utilizado com Node.js.