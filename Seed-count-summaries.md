Arabis F2 Seeds
================

*Goal*: To understand what we have in terms of representation from
different populations in the F2 seeds.

``` r
library(tidyverse)
library(knitr)

seeds <- read_csv("F1_pollinations_2021.csv")

ids <- read_csv("F1_individuals_2020.csv")
```

Add ID information to the seed counts:

``` r
seed_ids <- left_join(seeds, ids, by=c("Mother_ID"="Full_ID"))
```

Summarize what we have:

``` r
##need to change NAs in seed counts to zeros to facilitate summaries

counts <- seed_ids %>% filter(Treatment=="Self") %>% mutate(N_Seeds = replace_na(N_Seeds, 0)) %>% group_by(Cross_Type, Mother_ID) %>% summarize(Seed_Count=sum(N_Seeds))

kable(counts)
```

| Cross\_Type | Mother\_ID        | Seed\_Count |
|:------------|:------------------|------------:|
| Fr2xIT10    | 409 A             |           3 |
| Fr2xIT10    | 409 B             |          74 |
| Fr2xIT10    | 409 C             |          90 |
| Fr2xIT10    | 409 D             |         149 |
| Fr2xIT17    | 388 A             |          73 |
| Fr2xIT2     | 389 A             |          26 |
| Fr2xIT2     | 389 B             |         123 |
| Fr2xIT5     | 385 C             |          74 |
| Fr2xIT5     | 385 D             |          56 |
| Fr2xIT6     | 386 A             |          14 |
| Fr2xIT6     | 386 B             |           1 |
| Fr2xIT6     | 386 D             |          12 |
| Fr2xIT6     | 386 E             |           9 |
| Fr2xIT6     | 386 F             |          22 |
| Fr2xIT6     | 386 G             |          27 |
| Fr2xIT6     | 386 H             |          19 |
| Fr2xIT6     | 386 J             |          27 |
| Fr2xIT6     | 386 K             |           0 |
| Fr2xIT6     | 386 L             |          13 |
| Fr2xIT6     | 387 A             |          32 |
| Fr2xIT6     | 387 B             |          28 |
| Fr2xIT6     | 387 C             |          29 |
| Fr2xIT6     | 387 D             |          54 |
| Fr2xIT6     | 387 F             |          65 |
| Fr2xIT6     | 387 G             |         153 |
| Fr2xIT6     | 387 H             |          26 |
| Fr2xIT6     | 387 I             |          23 |
| Fr2xIT6     | 387 J             |          43 |
| Fr2xIT6     | 387 K             |          27 |
| Fr2xIT6     | 387 M             |          42 |
| Fr2xIT6     | 387 N             |          43 |
| Fr2xIT6     | 392 A             |          33 |
| Fr2xIT8     | 410 B             |          15 |
| Fr2xIT8     | 410 C             |          22 |
| Fr2xIT8     | 410 D             |          24 |
| Fr2xIT8     | 410 E             |          16 |
| Fr2xIT8     | 410 F             |          36 |
| Fr2xIT8     | 410 H             |          26 |
| Fr2xIT8     | 410 I             |         137 |
| Fr2xIT8     | 410 J             |         161 |
| Fr2xIT8     | 410 K             |          28 |
| Fr2xIT8     | 410 L             |          17 |
| Fr2xIT8     | 410 M             |          45 |
| Fr2xIT8     | 410 N             |          63 |
| Fr2xIT8     | 410 O             |         129 |
| Fr2xIT8     | 410 P             |          46 |
| Fr2xIT9     | 391 A             |          85 |
| Fr2xIT9     | 391 B             |          84 |
| Fr2xIT9     | 391 C             |          81 |
| Fr2xIT9     | 391 D             |          34 |
| Fr2xIT9     | 391 E             |          71 |
| Fr2xIT9     | 391 F             |          51 |
| Fr2xIT9     | 391 G             |          47 |
| Fr2xIT9     | 391 H             |          21 |
| Fr2xIT9     | 391 I             |          17 |
| Fr2xIT9     | 391 J             |          24 |
| Fr2xIT9     | 391 K             |          27 |
| Fr2xIT9     | 391 L             |          39 |
| Fr2xIT9     | 391 M             |          71 |
| Fr2xIT9     | 391 O             |          28 |
| Fr2xIT9     | 391 P             |          37 |
| Fr2xIT9     | 391 Q             |          15 |
| Fr2xIT9     | 391 R             |          29 |
| Fr2xIT9     | 401 A             |          31 |
| Fr2xIT9     | 401 B             |          33 |
| Fr2xIT9     | 401 C             |          40 |
| Fr2xIT9     | 403 B             |          69 |
| Fr2xIT9     | 403 C             |          71 |
| Fr2xIT9     | 403 E             |          66 |
| Fr2xIT9     | 408 B             |          71 |
| Fr2xIT9     | 411 A             |          58 |
| IT2xFr2     | 395 A             |           3 |
| IT2xFr2     | 395 C             |          29 |
| IT2xFr2     | 395 D             |          24 |
| IT2xFr2     | 395 E             |           0 |
| IT2xFr2     | 395 F             |           0 |
| IT2xFr2     | 395 G             |           1 |
| IT2xFr2     | 395 H             |          17 |
| IT2xFr2     | 395 I             |           0 |
| IT2xFr2     | 395 J             |          11 |
| IT2xFr2     | 395 K             |          30 |
| IT2xFr2     | 395 L             |          12 |
| IT2xFr2     | 396 A             |           3 |
| IT2xFr2     | 396 B             |           5 |
| IT2xFr2     | 396 C             |           0 |
| IT2xFr2     | 396 D             |           1 |
| IT2xFr2     | 396 E             |           1 |
| IT2xFr2     | 396 F             |           0 |
| IT2xFr2     | 396 H             |          36 |
| IT2xFr2     | 396 I             |           0 |
| IT2xFr2     | 396 J             |           0 |
| IT2xFr2     | 396 K             |           0 |
| IT2xFr2     | 396 L             |           9 |
| IT2xFr2     | 396 M             |           0 |
| IT2xFr2     | 396 O             |           0 |
| IT2xFr2     | 396 P             |           0 |
| IT2xFr2     | 396 Q             |           0 |
| IT2xFr2     | 396 T             |           0 |
| IT2xFr2     | 396 U             |           0 |
| IT2xFr2     | 396 V             |           0 |
| IT2xFr2     | 396 X             |           0 |
| IT2xFr2     | 396 Y             |          18 |
| IT2xFr2     | 412 A             |          36 |
| IT6xFr2     | 397 A             |         181 |
| IT6xFr2     | 397 C             |           2 |
| IT6xFr2     | 397 D             |          46 |
| IT6xFr2     | 397 E             |          87 |
| IT6xFr2     | 397 F             |          22 |
| IT6xFr2     | 397 G             |          40 |
| IT6xFr2     | 397 H             |          13 |
| IT6xFr2     | 397 I             |         116 |
| IT6xFr2     | 397 J             |          81 |
| IT6xFr2     | 397 K             |          42 |
| IT6xFr2     | 397 L             |         303 |
| IT6xFr2     | 397 M             |         103 |
| IT6xFr2     | 397 N             |         190 |
| IT6xFr2     | 397 O             |         149 |
| IT6xFr2     | 397 P             |         160 |
| IT6xFr2     | 397 Q             |          21 |
| IT6xFr2     | 398 A             |          13 |
| IT6xFr2     | 400 A             |          33 |
| IT6xFr2     | 400 C             |          12 |
| IT6xFr2     | 400 D             |          12 |
| IT6xFr2     | 405 A             |           6 |
| IT6xFr2     | 407 A             |           9 |
| IT8xFr2     | 399 A             |          34 |
| IT9xFr2     | 393 A             |           2 |
| IT9xFr2     | 393 B             |           3 |
| NA          | 370 O             |           0 |
| NA          | 389 D             |           0 |
| NA          | 391 N             |          10 |
| NA          | 395 O             |          13 |
| NA          | 396 N             |           0 |
| NA          | IT6:9:10 e(40) cr |         381 |

``` r
counts <- seed_ids %>% filter(Treatment=="Self") %>% mutate(N_Seeds = replace_na(N_Seeds, 0)) %>% group_by(Cross_Type) %>% summarize(N_RepsPerCross=length(unique(Mother_ID)), Seed_Count=sum(N_Seeds))

kable(counts)
```

| Cross\_Type | N\_RepsPerCross | Seed\_Count |
|:------------|----------------:|------------:|
| Fr2xIT10    |               4 |         316 |
| Fr2xIT17    |               1 |          73 |
| Fr2xIT2     |               2 |         149 |
| Fr2xIT5     |               2 |         130 |
| Fr2xIT6     |              23 |         742 |
| Fr2xIT8     |              14 |         765 |
| Fr2xIT9     |              25 |        1200 |
| IT2xFr2     |              32 |         236 |
| IT6xFr2     |              22 |        1641 |
| IT8xFr2     |               1 |          34 |
| IT9xFr2     |               2 |           5 |
| NA          |               6 |         404 |
