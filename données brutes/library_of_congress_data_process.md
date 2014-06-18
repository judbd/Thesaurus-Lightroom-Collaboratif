retirer les retours à la ligne inutiles :
`\s{11}`

retirer les parenthèses inutiles :
`\s\(.+\)`

retirer toutes les entrées dont on a pas besoin (toutes sauf les futurs synonymes use et uf (use for) :
`\s(\s+(FUN:|SN:|BT:|RT:|TTCSubj:|TNR:|FCNlctgm:|Facet:|TTCForm:|FCNgmgpc:|CN:|HN:|MF:|TTCSubd:|TTCRef:)\s+.+)`

rechercher use et use UF (use for) :
`\s\s+(UF:|USE:)\s+(.+)`
remplacer en synonymes lightroom avec des accolades et une tab :
`\n\t\{$2\}`

rechercher NT (narrow term) pour en faire un sous ensemble de mots clés :
`\s\s+NT:\s+(.+)`
remplacer sous mots-clés lightroom avec une tab :
`\n\t$1`

retirer les sauts de ligne en trop :
`\n\n`
remplacer par un seul saut :
`\n`
