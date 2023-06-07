Arabis F2 Seeds
================

*Goal*: To understand what we have in terms of representation from
different populations in the F2 seeds.

**Table 1**. A summary of the F1s that were selfed. Maternal and
paternal seed sources refer to the parental generation.

| Maternal seed source | Paternal seed source(s)             |
|----------------------|-------------------------------------|
| Fr2                  | It2, It5, It6, It8, It9, It10, It17 |
| It2                  | Fr2                                 |
| It6                  | Fr2                                 |
| It8                  | Fr2                                 |
| It9                  | Fr2                                 |

The crosses that we have represented in the F2s in both directions are
Fr2 with It2, It6, It8, and It9.

Fr2 plants produce very little scent, while the Italian populations are
variable but generally all highly scented (relative to populations from
Sweden and other populations from France).

List for Hanna

``` r
kable(seed_ids %>% 
   filter(Treatment=="Self") %>% mutate(N_Seeds = replace_na(N_Seeds, 0)) %>% filter(N_Seeds!=0) %>% 
  group_by(`Maternal ID`, `Paternal ID`) %>% summarize(N=length(Mother_ID)) %>% pivot_longer(cols = c(`Maternal ID`, `Paternal ID`), names_to = "Parents") %>% arrange(value) %>% distinct(value))
```

    ## `summarise()` has grouped output by 'Maternal ID'. You can override using the `.groups` argument.

| value                |
|:---------------------|
| Fr2:105:1 a(31) cr   |
| Fr2:105:1 b(31) cr   |
| Fr2:105:11 b(124) cr |
| Fr2:39 a Self b      |
| Fr2:39:10 b(31) cr   |
| Fr2:39a self b       |
| Fr2:56 self a        |
| Fr2:56 self b        |
| Fr2:61 self a        |
| Fr2:85:8 b(30) cr    |
| Fr2:S16:13 a(124) cr |
| Fr2:S16:13 b(124) cr |
| IT10:2018 1:366:2 b  |
| IT17:115 b           |
| IT2:3a               |
| IT2:3b               |
| IT5:M5b 1b           |
| IT6:13:8 a(9) cr     |
| IT6:15:14 a(6) cr    |
| IT6:15:14 b(6) cr    |
| IT8:18a              |
| IT8:VL31b            |
| IT9:11:5 b(3) cr     |
| IT9:2:3 a(4) cr      |
| IT9:3:9 b(3) cr      |
| IT9:P3:12 b(4) cr    |
| NA                   |

**Table 2**: A summary of seed production by F1 cross type. `Cross_Type`
is mother x father. `N_F1` is the number of F1 plants from a given cross
Hanna selfed to make the F2s. `N_Fruits` is the total number of fruits
from that cross (e.g., the sum of all of the fruits from each of the
plants from the particular cross). `Seed_Count` is the total number of
seeds generated from all of the fruits and plants of the particular
cross. `SeedsperFruit` is the average number of seeds in a fruit, to
help identify which plants produced fruits with more seeds (could relate
to viability). The `NA` cross type refers to plants that were not in the
spreadsheet but did have fruits collected.

| Cross type | N\_F1 | N\_Fruits | Seed\_Count | SeedsperFruit |
|:-----------|------:|----------:|------------:|--------------:|
| Fr2xIT10   |     4 |        17 |         316 |            19 |
| Fr2xIT17   |     1 |         3 |          73 |            24 |
| Fr2xIT2    |     2 |         7 |         149 |            21 |
| Fr2xIT5    |     2 |         5 |         130 |            26 |
| Fr2xIT6    |    23 |        45 |         742 |            16 |
| Fr2xIT8    |    14 |        38 |         765 |            20 |
| Fr2xIT9    |    26 |        61 |        1210 |            20 |
| IT2xFr2    |    33 |        83 |         249 |             3 |
| IT6xFr2    |    22 |       127 |        1641 |            13 |
| IT8xFr2    |     1 |         7 |          34 |             5 |
| IT9xFr2    |     2 |         3 |           5 |             2 |
| NA         |     4 |        23 |         381 |            17 |

*Observations*

-   Fr2 and It6 crosses in both directions yielded a lot of total seeds.
-   Fr2 x It8 and Fr2 x It9 have a lot of seeds, but the reverse crosses
    don’t. This is in large part due to the fact that fewer plants with
    Italian mothers were selfed (as opposed to the selfed plants having
    poor seed set).
-   Some of the crosses where we have greater average seed set per fruit
    (e.g., Fr2 x It17, It2, It5) have fewer unique F1s and fruits in the
    seed pool.

**Table 3**: The same data as above, but broken out by individual F1s.
This table shows how plants varied in terms of how many selfed fruits
were done. `Cross_Type` is as above. `F1_ID` is the code for specific F1
individual (that was selfed to make these seeds). `N_Fruits` is the
total number of fruits made by the plant. `Seed_Count` is the total
number of seeds made by the plant. `SeedsperFruit` is the average number
of seeds in a fruit.

| Cross type | Cross\_ID | N\_plants | N\_Fruits | Seed\_Count | SeedsperFruit |
|:-----------|----------:|----------:|----------:|------------:|--------------:|
| Fr2xIT10   |       409 |         4 |        17 |         316 |            19 |
| Fr2xIT17   |       388 |         1 |         3 |          73 |            24 |
| Fr2xIT2    |       389 |         2 |         7 |         149 |            21 |
| Fr2xIT5    |       385 |         2 |         5 |         130 |            26 |
| Fr2xIT6    |       386 |        10 |        12 |         144 |            12 |
| Fr2xIT6    |       387 |        12 |        32 |         565 |            18 |
| Fr2xIT6    |       392 |         1 |         1 |          33 |            33 |
| Fr2xIT8    |       410 |        14 |        38 |         765 |            20 |
| Fr2xIT9    |       391 |        18 |        43 |         771 |            18 |
| Fr2xIT9    |       401 |         3 |         5 |         104 |            21 |
| Fr2xIT9    |       403 |         3 |         7 |         206 |            29 |
| Fr2xIT9    |       408 |         1 |         3 |          71 |            24 |
| Fr2xIT9    |       411 |         1 |         3 |          58 |            19 |
| IT2xFr2    |       395 |        12 |        25 |         140 |             6 |
| IT2xFr2    |       396 |        20 |        54 |          73 |             1 |
| IT2xFr2    |       412 |         1 |         4 |          36 |             9 |
| IT6xFr2    |       397 |        16 |       117 |        1556 |            13 |
| IT6xFr2    |       398 |         1 |         5 |          13 |             3 |
| IT6xFr2    |       400 |         3 |         3 |          57 |            19 |
| IT6xFr2    |       405 |         1 |         1 |           6 |             6 |
| IT6xFr2    |       407 |         1 |         1 |           9 |             9 |
| IT8xFr2    |       399 |         1 |         7 |          34 |             5 |
| IT9xFr2    |       393 |         2 |         3 |           5 |             2 |

Is reproductive success asymmetric depending on the cross dimension?
Here I analyze whether reproductive success measures (seeds per fruit,
or total seed set) differ between crosses with French mother vs crosses
with an Italian mother.

Here is the anova output for this model:

And the numerical results of the contrast between the groups and a plot
of the estimated marginal means:

*Crosses with French mothers set more seeds than crosses with Italian
mothers.* Analyzing total seed set rather than seeds per fruit gives the
same result.
