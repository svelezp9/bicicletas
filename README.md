# bicicletas
## Diagrama de Contexto
![Context](https://user-images.githubusercontent.com/73863024/234447359-90328c7b-d977-4341-93bb-61f9e379bdf7.jpg)
## Diagrama de Despliegue
![Despliegue](https://user-images.githubusercontent.com/73863024/234447301-cbac3cda-382a-4557-bbe2-462980ae0b13.jpg)
## Diagrama de Entidad-Relación
![EntidadRelación](https://user-images.githubusercontent.com/73863024/234447395-74a287ef-aaab-42bc-b713-b6034a68bbe8.jpg)
## Diagrama de Secuencia
![Secuencia](https://user-images.githubusercontent.com/73863024/234447425-6f46b204-7565-45cc-928c-a6695ba5fa4a.jpg)
## Diagrama de Componentes
![Componentes](https://user-images.githubusercontent.com/73863024/234447451-5feaf6ba-b3d1-4d53-831d-4c4f28ab0997.jpg)
## Diagrama de modelo
![Components model](https://user-images.githubusercontent.com/73863024/234447459-210f374a-0662-404e-b66f-0e659bfd0a97.jpg)
## Decisiones arquitecturales
1) Para la autenticación se crea un adaptador adicional que se encargará de, en este caso, hacer la autenticación especificamente con google. Esto para tener un estándar de authenticación y que si mañana se cambia la forma de autenticación no sea necesario cambiar el microservicio sino solo el adaptador
2) Para facilidad de la aplicación y del despliegue, debido a que no es muy grande se va a contenerizar todo en docker y en la misma maquina servidor, es decir se tendran multiples contenedores con los diferentes microservicios en la misma máquina. 
3) Debido a lo anterior también se usara un orquestador frontEnd que llamará a los servicios, esto es benefico para esta aplicación por el hecho de ser pequeña  y aunque se forme un cuello de botella
4) La base de datos a trabajar sera MongoDB o mongoose, dependiendo del estudio posterior al diseño para ver cual es más optima. Lo importante es que sea una base de datos no estructurada o noSQL, para poder almacenar las bicicletas que tienen un campo que es una tupla, *la ubicación*.
