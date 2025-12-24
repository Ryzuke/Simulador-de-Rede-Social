Social Media Simulator - Data Structures & Algorithms
Este projeto é um simulador de backend de uma rede social desenvolvido em Python. O objetivo principal foi aplicar estruturas de dados fundamentais e algoritmos de busca e ordenação para criar um sistema eficiente, escalável e robusto.

##Funcionalidades
- Gestão de Usuários: Cadastro e alteração de perfis.
- Feed Cronológico: Postagens exibidas em ordem de publicação utilizando Deques.
- Sistema de Curtidas: Interação entre usuários e posts com notificações em tempo real.
- Trending Feed: Visualização dos posts mais curtidos utilizando o algoritmo Mergesort.
- Sistema de Undo (Desfazer): Reversão de ações (posts, curtidas, nomes) baseada em pilha.
- Soft Delete: Remoção lógica de posts para preservação da integridade de dados.

##Estruturas de Dados Utilizadas
A escolha de cada estrutura foi baseada na complexidade de tempo das operações (Big O):

- Estrutura	Aplicação	Justificativa Técnica
- Lista	Armazenamento de Usuários	Permite acesso sequencial e serviu de base para a implementação da busca binária.
- Pilha (Stack)	Sistema de Undo	Segue o princípio LIFO (Last-In, First-Out), ideal para reverter a última ação do usuário.
- Deque	Feed e Notificações	Utilizado pela eficiência de O(1) em inserções no início (appendleft), garantindo um feed sempre atualizado sem custo de deslocamento de memória.

##Algoritmos e Otimizações
- Busca Binária ($O(\log n)$)Em vez de utilizar uma busca linear comum, aproveitei o fato de os IDs de usuários serem incrementais e a lista estar sempre ordenada para implementar a Busca Binária. Isso reduz drasticamente o tempo de procura em grandes bases de dados.
- Mergesort ($O(n \log n)$)Para o feed de posts mais curtidos, implementei o Mergesort. Diferente do Quicksort, o Mergesort garante uma performance estável de $O(n \log n)$ mesmo no pior caso, além de ser um algoritmo estável, o que permite manter a ordem cronológica em posts com o mesmo número de curtidas.

##Autor
Desenvolvido por Diego Amaral como projeto prático para a disciplina de Estrutura de Dados (4º Período).
