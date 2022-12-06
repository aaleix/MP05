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

En aquest cas podem definir les classes d'equivalència del programa d'aquesta manera:

| Paràmetre entrada | Regla a aplicar | Classes vàlides | Classes no vàlides |
| ----------- | ----------- | ----------- | ----------- |
| Edat | És un número? + rang valors (>=18) | 1. 18<=edat<=120 | 2. edat < 18 <br> 3. edat >120 <br> 4. no és un número.|
