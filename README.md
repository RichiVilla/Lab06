# Lab06: Desplegar mi primera aplicación en Azure
## Mi primer despliegue en la nube

# Parte I - Despliegue app React (frontend) en Azure
- Crear una cuenta institucional en Azure y crear un budget de 1 dólar para la cuenta.

![image](https://github.com/RichiVilla/Lab06/assets/124943246/dda75663-648e-45d0-b2d0-af3300c88ac7)

1. Crear una Aplicación Web Estática enlazando nuestra cuenta de GitHub junto a un repositorio que contenga la información referente al laboratorio pasado de la Calculadora con React.

- Proceso de creación de la Aplicación Web Estática.

 ![image](https://github.com/RichiVilla/Lab06/assets/124943246/4e7492f2-1e06-4d01-af56-225e0f50f61c)

![image](https://github.com/RichiVilla/Lab06/assets/124943246/90f0d121-a149-4232-8a6f-a8a8f50b394e)

![image](https://github.com/RichiVilla/Lab06/assets/124943246/c6473925-85eb-4ec7-9dec-437781b136d2)


- Creación completada.

![image](https://github.com/RichiVilla/Lab06/assets/124943246/0adc8cf4-41d3-4d3f-a9b4-499793154533)

![image](https://github.com/RichiVilla/Lab06/assets/124943246/9d71e35c-6d07-4170-bc81-92fbe2ec17c5)


- En GitHub buscamos el repositorio y vemos que haya sido captada por Azure (En este caso hubo que modificar el código ya que había inconvenientes con Oryx).

![image](https://github.com/RichiVilla/Lab06/assets/124943246/f735cf9c-a1e3-4e58-a1ba-0739e0eaffab)


- Ir a Azure, a la App Web Estática, y poder cargar la página dando clic en Examinar.

 ![image](https://github.com/RichiVilla/Lab06/assets/124943246/702ff90f-a46e-4d87-8bb3-2dd668211ea3)


 
 
 


# Parte II - Despliegue app web spring MVC (o spring-boot backend)
## Ejercicio 1: Base de datos MySQL
1. Iniciar Azure Cloud Shell desde el protal e ingresar al Bash para poder inrgesar los siguientes comandos:

   az group create --name MyResourceGroup --location westus
![image](https://github.com/RichiVilla/Lab06/assets/124943246/717331b1-4984-460d-b275-2a81b44d15c6)

   Crear un plan de servicio de aplicaciones con:
   az appservice plan create --resource-group MyResourceGroup --name MyPlan --sku F1
   
![image](https://github.com/RichiVilla/Lab06/assets/124943246/89cd4f18-ced4-41a2-9691-244feb884b0b)

    Crear un servidor MySQL con: 
    az mysql server create --resource-group MyResourceGroup --name mysqldbserver --admin-user mysqldbuser --admin-password P2ssw0rd@123 --sku-name Standard_B1ms
    
![image](https://github.com/RichiVilla/Lab06/assets/124943246/55ef2e00-83ef-4200-9445-161053d78942)

2. A continuación ir al Azure Database for MySQL server que se generó.

![image](https://github.com/RichiVilla/Lab06/assets/124943246/611d11a6-f072-4f6c-ae6a-677f6b3709f0)

3. Buscar las propiedades y tener a la mano el nombre del servidor y del administrador.

 ![image](https://github.com/RichiVilla/Lab06/assets/124943246/c93ea939-9a5e-468e-90e9-00f697607cbe)

4. Buscamos la sección de "Conectar" para habilitar los Firewall que permiten la conexión de los servidores de MySQL con los servicios de Azure.

 ![image](https://github.com/RichiVilla/Lab06/assets/124943246/87d81d87-3234-4be3-8f3e-46f3d379794e)


## Ejercicio 2: actualización de la configuración de la aplicación web
1. Ir hasta la página web creada y buscar la configuración, en especial las Configuraciones de Pila.

 ![image](https://github.com/RichiVilla/Lab06/assets/124943246/640e0468-870f-4fc0-9a96-5b932a198361)

2. Esperamos que estos cambios queden guardados y vamos a "Examinar" para ver la página.

 ![image](https://github.com/RichiVilla/Lab06/assets/124943246/94ae2d97-aaf6-4455-b5c9-046c1a33bfbe)

3. La página debe verse como a continuación.

![image](https://github.com/RichiVilla/Lab06/assets/124943246/2128f7e4-63cb-4a64-82ea-3ffafbd87964)

 4. Vamos a las "Variables del Entorno" y crearemos una nueva "Cadena de Conexión"
![image](https://github.com/RichiVilla/Lab06/assets/124943246/26504d6b-4700-4328-ad45-f03b50e77b29)

 ![image](https://github.com/RichiVilla/Lab06/assets/124943246/524bd74f-0efa-45ed-b5bb-7a40580b5b59)


 

EJERCICIO 3
  
![image](https://github.com/RichiVilla/Lab06/assets/124943246/68bae4ea-3043-44be-9997-79fbc0fe5775)


![image](https://github.com/RichiVilla/Lab06/assets/124943246/c1cc070d-c533-46f4-a1c0-6b5a237e1887)

