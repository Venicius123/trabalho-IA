# trabalho-IA

Aluno: Venicius Santos Nunes

Professor: Arleys Castro 

Matrícula: 31221576

O objetivo do projeto é fazer com que o PACMAN encontre a comida que está em algum lugar do labirinto, para isso são aplicadas tipos de buscas conforme aprendemos durante o curso de IA.

DFS - Busca começa no nó raiz e adiciona na pilha nó raiz e explora os ramos desses nós, colando o nó a ser explorado no stack(Pilha). Depois você volta para o nó raiz, marcando os nós já visitados. 

python pacman.py -l tinyMaze -p SearchAgent

python pacman.py -l mediumMaze -p SearchAgent

python pacman.py -l bigMaze -z .5 -p SearchAgent

Video: https://drive.google.com/open?id=18NsaXxoK5BtmkDGCHIHG__qfDu0pELOk


BFS - Funciona de forma similar ao DFS, porém invés de Stack(Pilhas) utilizamos as Queue(Filas), o que melhora um pouco as buscas. 

python pacman.py -l mediumMaze -p SearchAgent -a fn=bfs

python pacman.py -l bigMaze -p SearchAgent -a fn=bfs -z .5


Video: https://drive.google.com/open?id=1cKzM1bUKLuYjgHeAXKPCU1d8E1u0I87C

USC - A implementação desse código também é similar a da DFS, entretanto agora utilizamos PriorityQueue(Filas de Prioridade) ao invés de Filas.

python pacman.py -l mediumMaze -p SearchAgent -a fn=ucs

python pacman.py -l mediumDottedMaze -p StayEastSearchAgent

python pacman.py -l mediumScaryMaze -p StayWestSearchAgent


Video: https://drive.google.com/open?id=1r34xu7E8CU-rsMRHmB92iDcXz91fMhlv

A* SEARCH - Essa busca necessita da implementação de uma Heurística que já está implementada no código, sendo assim foi necessário apenas implementar a lógica na função ASearch.

python pacman.py -l bigMaze -z .5 -p SearchAgent -a fn=astar,heuristic=manhattanHeuristic 

python pacman.py -l openMaze -z .5 -p SearchAgent -a fn=astar,heuristic=manhattanHeuristic 

python pacman.py -l trickySearch -p AStarFoodSearchAgent

Video: https://drive.google.com/file/d/1hrPT-OHvZBiwq3jiNa2y_r-yJFwKVcJ_/view?usp=sharing

PERGUNTAS

(Pergunta 1) A ordem de exploração foi de acordo com o esperado? O Pacman realmente passa por todos os estados explorados no seu caminho para o objetivo?

Quando rodei o programa o pacman passou por todos os estados explorados. 

(Pergunta 2) Essa é uma solução ótima? Senão, o que a busca em profundidade está fazendo de errado?

(Pergunta 3) A busca BFS encontra a solução ótima? Senão, verifique a sua implementação. Se o seu código foi escrito de maneira correta, ele deve funcionar também para o quebra-cabeças de 8 peças (seção 3.2 do livro-texto) sem modificações.

Ambos os algoritmos funcionaram bem, o DPS encontra uma solução boa e o BFS encontra uma solução melhor ainda. O jogo 8 pluzes rodou tambem encontrando a sequência.
