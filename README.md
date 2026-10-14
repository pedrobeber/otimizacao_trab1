# otimizacao_trab1
First assignment of CI1238 Optimization (UFPR): model **"cargo transport with resource packages"** as a linear program and generate its input for the **lp_solve** solver.

**Problem.** A company ships a product from city 1 (factory) to city *n* (warehouse) over a network of *m* routes. Each route has a daily capacity in tons and requires some amount of each of *k* resources per ton shipped. Resources can only be bought in *q* package types, each with its own price. Goal: maximize profit = (gain per ton × tons delivered) − cost of the packages.

**Implementation.** `transporte.c` reads an instance from `stdin` (*n, m, k, q, p*, then the routes, then the packages) and prints the linear program in lp_solve format to `stdout`; solving it is left to `lp_solve`. `pbqv20.pdf` is the report with the modelling.

**Build and run:** `make`, then `./transporte < instance.txt | lp_solve`.
