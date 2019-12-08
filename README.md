# trabalho-IA

Aluno: Venicius Nunes

Professor: Aerles 

Matricula: 

Objetivo  do projeto e fazer com que o PACMAN encontre a comida que está em algum lugar do labirito, para isso são aplicadas tipos de buscas conforme aprendemos durante o curso de IA .

DFS - Busca começar no nó raiz e adiciona na pilha nó raiz e explora os ramos desses nós, colando o nó a ser explorado no stack(Pilha). Depois você volta para o nó raiz, marcando os nós já visitados 

DFS

python pacman.py -l tinyMaze -p SearchAgent

python pacman.py -l mediumMaze -p SearchAgent

python pacman.py -l bigMaze -z .5 -p SearchAgent

Video: https://drive.google.com/open?id=18NsaXxoK5BtmkDGCHIHG__qfDu0pELOk


BFS - Funciona de Forma similar ao DFS, porém inves de Stack(Pilhas) utilizamos as Queue(Filas) o que melhora um pouco as buscas. 

BFS

python pacman.py -l mediumMaze -p SearchAgent -a fn=bfs

python pacman.py -l bigMaze -p SearchAgent -a fn=bfs -z .5


Video: https://drive.google.com/open?id=1cKzM1bUKLuYjgHeAXKPCU1d8E1u0I87C

USC - A implementação desse codigo tambem é similar a da DFS, entretanto agora utilizamos PriorityQueue(Filas de Prioridade) ao inves de Filas.

UCS

python pacman.py -l mediumMaze -p SearchAgent -a fn=ucs

python pacman.py -l mediumDottedMaze -p StayEastSearchAgent

python pacman.py -l mediumScaryMaze -p StayWestSearchAgent


Video: https://drive.google.com/open?id=1r34xu7E8CU-rsMRHmB92iDcXz91fMhlv

A* SEARCH - Essa busca necessita da implementação de uma Heuristica que já está implementada no codigo, sendo assim foi necessrio apenas implementar a logica no função ASearch .

A* search

python pacman.py -l bigMaze -z .5 -p SearchAgent -a fn=astar,heuristic=manhattanHeuristic 

python pacman.py -l openMaze -z .5 -p SearchAgent -a fn=astar,heuristic=manhattanHeuristic 

python pacman.py -l trickySearch -p AStarFoodSearchAgent

Video: https://drive.google.com/open?id=1hrPT-OHvZBiwq3jiNa2y_r-yJFwKVcJ_

