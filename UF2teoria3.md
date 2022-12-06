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

Si la persona pot passar la funció retornarà Passa, en cas  de no tenir l'edat necessària retornarà No Passa, si l'entrada de dades no és vàlida retornarà Error.

##### Classes d'equivalència:

En aquest cas podem definir les classes d'equivalència del programa d'aquesta manera:

| Paràmetre entrada | Regla a aplicar | Classes vàlides | Classes no vàlides |
| ----------- | ----------- | ----------- | ----------- |
| Edat | És un número? + rang valors (18..120) | 1. 18 <= edat <= 120 | 2. edat < 18 <br> 3. edat >120 <br> 4. no és un número.|

##### Classes d'equivalència vàlides:

Ara haurem de dissenyar els casos de prova per cobrir totes les classes vàlides (1).

| Edat | Classe vàlida coberta| Resultat |
| ----------- | ----------- | ----------- |
| 40 | 1 | Passa |

##### Classes d'equivalència no vàlides:

Ara generarem proves per cobrir totes les calsses de proves no vàlides (2,3 i 4).

| Edat | Classe no vàlida coberta| Resultat |
| ----------- | ----------- | ----------- |
| 15 | 2 | No Passa |
| 199 | 3 | No Passa |
| cinc | 4 | Error |


### Anàlisi dels valors límit:

Per alguna raó que no està clara, els errors solen donar-se més vegades als límits del camp d'entrada que al centre.

Per aquest motiu s'ha desenvolupat l'anàlisi dels valors límits com a tècnica de prova.

D'aquesta manera seleccionarem casos de prova que provin els valors l'imits d'entrada del codi.

**Aquestes proves són adicionals a la partició equivalent**

Les proves d'anàlisi dels valors límits contemplen agafar els valors límits del rang de valors possibles, el valor immediatament inferior i el valor immediatament superior.

| Paràmetre entrada | Regla a aplicar | Classes vàlides | Classes no vàlides |
| ----------- | ----------- | ----------- | ----------- |
| Edat | És un número? + rang valors (18..120) | 5. edat=18 <br> 6. edat=19 <br> 7. edat=119 <br> 8. edat=120  | 9. edat=17 <br> 10. edat=121|

Ara haurem de dissenyar els casos de prova per cobrir totes les classes vàlides (5 a 8).

| Edat | Classe vàlida coberta| Resultat |
| ----------- | ----------- | ----------- |
| 18 | 5 | Passa |
| 19 | 6 | Passa |
| 119 | 7 | Passa |
| 120| 8 | Passa |

I els casos no vàlids (9 i 10):

| Edat | Classe vàlida coberta| Resultat |
| ----------- | ----------- | ----------- |
| 17 | 9 | No passa |
| 121 | 10 | No passa |

Amb aquestes tècniques provem totes les clàsses d'equivalència vàlides i no vàlides amb uns valors suficientment representatius de cada classe.

Només amb aquestes proves no podem assegurar que el codi estigui lliure d'errors.

## Exercici per fer a classe:

Tens que provar un programa que rep dos valors diners i preu, els diners són els que insereix un usuari en una màquina de café i el preu és el preu del producte, com a màxim un usuari podrà introduir 50€.

El programa tornarà -1 si els diners són més petits que el preu, en cas contrari tornaran la diferència entre els diners entrats i el preu del producte. Si alguna de les entrades no és un número tornarà Error.

**Per exemple:**
- preu = 2
- diners = 1
- RETORNA = -1

- preu = 2
- diners = 3
- RETORNA = 1

**Calculeu la partició equivalent i valors per les classes d'equivalència vàlides i no vàlides:**

### Classes d'equivalència:

| Paràmetre entrada | Regla a aplicar | Classes vàlides | Classes no vàlides |
| ----------- | ----------- | ----------- | ----------- |
| diners | És un número? + rang valors (0..50) | 1. 0 <= diners <= 50 | 2. diners < 0 <br> 3. diners > 50 <br> 4. no és un número.|
| preu | És un número? + rang valors (0--50) | 5. 0 < preu <= 50 | 6. preu < 0 <br> 7. preu > 50 <br> 8. no és un número.|



### Classes d'equivalència vàlides (1 i 5):

Ara haurem de dissenyar els casos de prova per cobrir totes les classes vàlides (1).

| diners | preu | Classe vàlida coberta| Resultat |
| ----------- | ----------- | ----------- | ----------- |
| 10 | 11 | 1, 5 | -1 |


##### Classes d'equivalència no vàlides:

Ara generarem proves per cobrir totes les calsses de proves no vàlides (2,3 i 4).


| diners | preu | Classe vàlida coberta| Resultat |
| ----------- | ----------- | ----------- | ----------- |
| -10 | 11 | 2 | -1 |
| 60 | 2 | 3 | -1 |
| cinquanta | 4 | 3 | Error |
| 10 | -1 | 6 | -1 |
| 10 | 100 | 7 | -1 |
| 10 | sis | 8 | Error |






