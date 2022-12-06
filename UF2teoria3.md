## Proves de caixa negra:

![image](https://user-images.githubusercontent.com/110727546/204654653-25f97c6c-fb51-4fbf-a311-4ab3553fde7e.png)

Les proves de caixa negra proven la funcionalitat del programa, per al qual es dissenyen casos de prova que comprovin les especificacions del programa.

Les proves de caixa negra, a diferencia de les proves de caixa blanca són proves en les que no hem de conèixer el codi a testejar.

**No són una alternativa a les proves de caixa blanca**, si no un complement.

### Partició equivalent:

La técnica de partició equivalent serveix per identificar les entrades vàlides i invàlides per a un determinat codi.

Si un codi té més d'una entrada possible, per exemple dues variables, s'hauran d'identificar els possibles valors de cada variable per separat.

#### Exemple:

Tenim una funció que rep l'edat d'una persona i retorna si pot entrar o no a la discoteca, anomenarem a aquesta funció **porterDiscoteca()**

##### Classes d'equivalència:

En aquest cas podem definir les classes d'equivalència del programa d'aquesta manera:

| Paràmetre entrada | Regla a aplicar | Classes vàlides | Classes no vàlides |
| ----------- | ----------- | ----------- | ----------- |
| Edat | És un número? + rang valors (>=18) | 1. 18<=edat<=120 | 2. edat < 18 <br> 3. edat >120 <br> 4. no és un número.|

##### Classes d'equivalència vàlides:

Ara haurem de dissenyar els casos de prova per cobrir totes les classes vàlides (1).

| Edat | Classe vàlida coberta|
| ----------- | ----------- |
| 40 | 1 |

##### Classes d'equivalència no vàlides:

Ara generarem proves per cobrir totes les calsses de proves no vàlides (2,3 i 4).

| Edat | Classe no vàlida coberta|
| ----------- | ----------- |
| 15 | 2 |
| 199 | 3 |
| cinc | 4 |


### Anàlisi dels valors límit:

Per alguna raó que no està clara, els errors solen donar-se més vegades als límits del camp d'entrada que al centre.

Per aquest motiu s'ha desenvolupat l'anàlisi dels valors límits com a tècnica de prova.

D'aquesta manera seleccionarem casos de prova que provin els valors l'imits d'entrada del codi.

**Aquestes proves són adicionals a la partició equivalent**

Les proves d'anàlisi dels valors límits contemplen agafar els valors límits del rang de valors possibles, el valor immediatament inferior i el valor immediatament superior.

| Paràmetre entrada | Regla a aplicar | Classes vàlides | Classes no vàlides |
| ----------- | ----------- | ----------- | ----------- |
| Edat | És un número? + rang valors (>=18) | 5. edat=18 <br> 6. edat=19 <br> 7. edat=119 <br> 8. edat=120  | 9. edat=17 <br> 10. edat=121|

Ara haurem de dissenyar els casos de prova per cobrir totes les classes vàlides (5 a 8).

| Edat | Classe vàlida coberta|
| ----------- | ----------- |
| 18 | 5 |
| 19 | 6 |
| 119 | 7 |
| 120| 8 |

I els casos no vàlids (9 i 10):

| Edat | Classe vàlida coberta|
| ----------- | ----------- |
| 17 | 9 |
| 121 | 10 |

