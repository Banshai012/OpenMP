# OpenMP

Cours et travaux pratiques de calcul parallèle en mémoire partagée avec **OpenMP** (ENSEEIHT, Année 2), en C et Fortran.

## Contenu

- `Cours/` — support de cours (`newcourse.pdf`) et exemples de code associés
- `TP_Chol/` — TP de factorisation de Cholesky : versions séquentielle et parallèles (boucle simple, boucle optimisée, tâches OpenMP), avec bancs d'essai en scalabilité forte et faible (`bench_strong.c`, `bench_weak.c`) et scripts de tracé (`plots.gp`)
- `BE_OpenMP_2024/` — bureau d'étude : intégration numérique, réductions manuelles, minimiseur, scan préfixe (`prefixscan`)

## Compiler et exécuter

Chaque sous-dossier a son propre `Makefile` :

```bash
cd TP_Chol
make
./chol_par_loop_improved
```

Les bancs d'essai (`bench_strong.c`/`bench_weak.c`) mesurent le passage à l'échelle en faisant varier le nombre de threads OpenMP (`OMP_NUM_THREADS`) et la taille du problème.
