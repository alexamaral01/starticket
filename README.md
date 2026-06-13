# star-ticket


A arquitetura foi montando pelo Renato Augusto:
[ARQUITETANDO O TICKETMASTER NA PRÁTICA | SYSTEM DESIGN](https://www.youtube.com/watch?v=3XSijmIZxXU)

A minha ideia é usar esta base de conhecimento para praticar arquitetura de sistema e explorar outros conhecimentos.

# Requesitos originais

## Etapa 1 - Entenda o problema e estabeleça os requisitos

### Requisitos Funcionais
**1. Visualização de eventos:** Os usuários devem ser capazes de visualizar os eventos disponìveis na plataforma.  
**2. Pesquisa de eventos:** Os usuários devem ser capazes de pesquisar por eventos especificos na plataforma.
**3. Compra de ingressos:** Os usuários devem ser capazes de comprar ingressos para participar desses eventos.

### Requisitos não funcionais
1. O sistema deve suportar **10 Milhões de usuaŕios ativos simultaneamente** nos dias de grandes eventos.
2. O sistema deve impedir **bots de compras** de ingressos no dias de grandes eventos e NÂO pode benificiar usuários em **geolocalizações privilegiadas**
3. A pesquisa por eventos deve ser **inteligentes, tolerar erros de digitação (typo) e encontrar palavras por proximidade (Stemming)** ex: Pesquisa = casa | Resultado = **casas, casarão, casinha etc...**
4. O sistema deve impedir que dois usuários comprem o mesmo **ingresso / assento (CONSISTÊNCIA - CONCORRÊNCIA)
5. O sistema deve ter **baixa latência** na pesquisa por eventos (< 500ms)
6. O sistema deve ser capaz de suportar uma **alta taxa de transferência de leitura** (100:1)
7. O sistema deve operar em modo de **alta disponibilidade**
