# Query Complexity of Mastermind Variants
We study variants of [Mastermind](https://en.wikipedia.org/wiki/Mastermind_(board_game)), a popular board game in which the objective is sequence reconstruction. In this two-player game, the so-called *codemaker* constructs a hidden sequence *H = (h_1, h_2, ..., h_n)* of colors selected from an alphabet *A = {1, 2, ..., k}* (*i.e.,* *h_i &#8712; A* for all *i &#8712;\{1,2, ..., n\}*). The game then proceeds in turns, each of which consists of two parts: in turn *t*, the second player (the \textit{codebreaker}) first submits a query sequence *Q_t = (q_1, q_2, ..., q_n)* with *q_i &#8712; A* for all *i*, and second receives feedback *&#916;(Q_t, H)*, where *&#916;* is some agreed-upon function of distance between two sequences with *n* components. The game terminates when *Q_t = H*, and the codebreaker seeks to end the game in as few turns as possible. Throughout we let *f(n,k)* denote the smallest integer such that the codebreaker can determine any *H* in *f(n, k)* turns. We prove three main results: First, when *H* is known to be a permutation of *\{1,2, ..., n\}*, we prove that *f(n, n)\ge n - loglog(n)* for all sufficiently large *n*. Second, we show that Knuth's Minimax algorithm identifies any *H* in at most *nk* queries. Third, when feedback is not received until all queries have been submitted, we show that *f(n,k) = &#937;(nlog(k))*.