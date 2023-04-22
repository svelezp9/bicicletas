# bicicletas
## Diagrama de Contexto
![Context](https://user-images.githubusercontent.com/73863024/233798258-5c60b47a-9c7a-4828-bb2e-8509ddd357ac.jpg)
## Diagrama de Despliegue
![Despliegue](https://user-images.githubusercontent.com/73863024/233798259-e0be34c1-b8af-4ea5-8742-e81580a852b2.jpg)
## Diagrama de Entidad-Relación
![EntidadRelación](https://user-images.githubusercontent.com/73863024/233798260-7c7471ed-20dd-45da-aa2a-b102b92fd14d.jpg)
## Diagrama de Secuencia
![Secuencia](https://user-images.githubusercontent.com/73863024/233798261-1a8b3c38-a67c-437a-886d-f22aae56fbd2.jpg)
## Diagrama de Componentes
![Componentes](https://user-images.githubusercontent.com/73863024/233798263-293970bd-c173-4711-aff9-f579d3843ca8.jpg)
## Diagrama de modelo
![Components model](https://user-images.githubusercontent.com/73863024/233798264-94c1fe73-0fba-4d9f-872b-eaf770c00dbd.jpg)
## Decisiones arquitecturales
1) Para la autenticación se crea un adaptador adicional que se encargará de, en este caso, hacer la autenticación especificamente con google. Esto para tener un estándar de authenticación y que si mañana se cambia la forma de autenticación no sea necesario cambiar el microservicio sino solo el adaptador
2) Para facilidad de la aplicación y del despliegue, debido a que no es muy grande se va a contenerizar todo en docker y en la misma maquina servidor, es decir se tendran multiples contenedores con los diferentes microservicios en la misma máquina.
3) La base de datos a trabajar sera MongoDB o mongoose, dependiendo del estudio posterior al diseño para ver cual es más optima. Lo importante es que sea una base de datos no estructurada o noSQL, para poder almacenar las bicicletas que tienen un campo que es una tupla, *la ubicación*.
