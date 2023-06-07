Potential asymmetries in Arabis F2 reproductive success
================

*Background*: Crosses were performed between Fr2 plants (France2), which
are self-compatible and have very low scent emission, and plants from
multiple Italian populations, which are self-incompatible and have
variable scent profiles across populations but generally high emission
rates. These F1s were then selfed to create F2s.

**Table 1**. A summary of the parentage of the F1s that were selfed to
make the F2s. Maternal and paternal seed sources refer to the parental
generation.

| Maternal seed source | Paternal seed source(s)             |
|----------------------|-------------------------------------|
| Fr2                  | It2, It5, It6, It8, It9, It10, It17 |
| It2                  | Fr2                                 |
| It6                  | Fr2                                 |
| It8                  | Fr2                                 |
| It9                  | Fr2                                 |

The crosses that we have represented in the F2s in both directions are
Fr2 with It2, It6, It8, and It9.

**Table 2**: A summary of seed production by F1 cross type. `Cross_Type`
is mother population x father population. `N_Cross` is the number of
crosses of unique crosses of the cross type that were performed (e.g.,
different parental plants from the populations). `N_F1` is the total
number of F1 plants from a given cross that were selfed to make the F2s.
`N_Fruits` is the total number of fruits from that cross (e.g., the sum
of all of the fruits from each of the plants from the particular cross
type). `Seed_Count` is the total number of seeds generated from all of
the fruits and plants of the particular cross type. `SeedsperFruit` is
the average number of seeds in a fruit, to help identify which plants
produced fruits with more seeds and compare across crosses that had
different number of plants or fruits.

| Cross\_Type | N\_Cross | N\_F1 | N\_Fruits | Seed\_Count | SeedsperFruit |
|:------------|---------:|------:|----------:|------------:|--------------:|
| Fr2xIT10    |        1 |     4 |        17 |         316 |            19 |
| Fr2xIT17    |        1 |     1 |         3 |          73 |            24 |
| Fr2xIT2     |        1 |     2 |         7 |         149 |            21 |
| Fr2xIT5     |        1 |     2 |         5 |         130 |            26 |
| Fr2xIT6     |        3 |    23 |        45 |         742 |            16 |
| Fr2xIT8     |        1 |    14 |        38 |         765 |            20 |
| Fr2xIT9     |        5 |    26 |        61 |        1210 |            20 |
| IT2xFr2     |        3 |    34 |        84 |         249 |             3 |
| IT6xFr2     |        6 |    23 |       147 |        2022 |            14 |
| IT8xFr2     |        1 |     1 |         7 |          34 |             5 |
| IT9xFr2     |        1 |     2 |         3 |           5 |             2 |

*Observation*: Aside from the IT6 x Fr2 cross, which set a lot of seeds
in both directions, in general it seems like crosses with Italian
mothers set fewer seeds overall and fewer seeds per fruit.

To test if reproductive success is asymmetric depending on the cross
direction, I analyzed whether reproductive success measures (seeds per
fruit, total seed set) differ between crosses with a French mother vs
crosses with an Italian mother. The specific parents used to create a
particular F2 (because sometimes there were multiple F1s from a specific
cross, see `N_Cross` in Table 2 above) was nested within the Italian
population involved in the cross (because the French population was
always Fr2) and this was included as a random effect in the model.

Here is the anova output for the model of seeds/fruit:

    ## Type III Analysis of Variance Table with Satterthwaite's method
    ##             Sum Sq Mean Sq NumDF DenDF F value    Pr(>F)    
    ## Cross_Type2 1194.9  1194.9     1 19.33  26.665 5.238e-05 ***
    ## ---
    ## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1

And the numerical results of the contrast between the groups and a plot
of the estimated marginal means:

    ##  contrast estimate   SE   df t.ratio p.value
    ##  Fr - It      13.4 3.03 17.3   4.410  0.0004
    ## 
    ## Degrees-of-freedom method: kenward-roger

![](Arabis_F2_for_Tanya_files/figure-gfm/unnamed-chunk-6-1.png)<!-- -->

*Crosses with French mothers set more seeds than crosses with Italian
mothers.* Analyzing total seed set rather than seeds per fruit gives the
same result.
