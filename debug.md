# Depurador:

El depurador, debugger o debug és una part del IDE que ens serveix per depurar el codi, deixant-nos executar el programa de forma controlada.

Per això ens deixa crear punts d'interrupció que pararan l'execució del programa i ens deixaran inspeccionar l'estat de les variables en aquell moment.

Per exemple tenim el següent codi:

![image](https://user-images.githubusercontent.com/110727546/206019554-8bb40f5c-2e8f-41cb-86d1-784fe74be132.png)

Els punts vermells corresponen a dos punts d'interrupció, el codi es pararà cada vegada que s'executi la línia de codi i podrem inspeccionar les variables i decidir què fer amb l'execució:

![image](https://user-images.githubusercontent.com/110727546/206019838-b50eb53b-b62c-4ad3-b784-4e5c091c07f1.png)

## Exemple averageFinder:

```
public class averageFinder {
    public static void main(String[] args) {
        System.out.println("Average finder v0.1");
        double avg = findAverage(args);
        System.out.println("The average is " + avg);
    }

    private static double findAverage(String[] input) {
        double result = 0;
        for (String s : input) {
            result += Integer.parseInt(s);
        }
        return result;
    }

}
```

- Modificar les variables de paràmetre d'entrada.
- Comprovar funcionament amb punst d'interrupció.
- Detectar perquè no funciona i arraglar-ho.

### Modificar paràmetres d'entrada:

![image](https://user-images.githubusercontent.com/110727546/206020199-9c83e1c6-d145-4a9b-888f-6b2ee08f639e.png)

![image](https://user-images.githubusercontent.com/110727546/206020278-c6882186-12a5-4711-bd5e-d5d88888ec81.png)

## Exemple matrius:

- Podem canviar els valors de les variables als punts d'execució.
- Comprovar que sortim dels límits del bucle.

![image](https://user-images.githubusercontent.com/110727546/206021220-5973f0ab-d103-4b60-85b7-3bfffa06c7c8.png)

![image](https://user-images.githubusercontent.com/110727546/206021422-5fb8fd1f-622d-4d00-8965-cdba34493628.png)






