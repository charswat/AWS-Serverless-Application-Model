# AWS-Serverless-Application-Model
1.	Se creó	 un repositorio llamado serverless-site en aws en codecommit.
![repo](https://user-images.githubusercontent.com/72947118/97511650-9228e400-1955-11eb-9309-74add1bfaa6a.png)
2. se clono el repositorio.
![image](https://user-images.githubusercontent.com/72947118/97515929-12544700-1960-11eb-98ac-fd24117478f0.png)
3.Se descargo la pagina web y se subio al repositorio.
![image](https://user-images.githubusercontent.com/72947118/97524716-57ce3f80-1973-11eb-8e1a-724739d3e406.png)
Habilite el alojamiento web con la consola de AWS Amplify
1. Lance la página de la consola de la consola de Amplify
2. Haga clic en Comenzar bajo Implementar con la consola de Amplify
<img width="405" alt="amplify" src="https://user-images.githubusercontent.com/72947118/97525449-d5467f80-1974-11eb-90f6-80da0ccabb20.PNG">
3. Seleccione el proveedor del servicio de repositorio utilizado hoy y seleccione Siguiente
<img width="620" alt="seleccionaRepo" src="https://user-images.githubusercontent.com/72947118/97525485-eabba980-1974-11eb-996a-4313f099f645.PNG">
4.pagina en contruccion.
<img width="727" alt="Contruccionweb" src="https://user-images.githubusercontent.com/72947118/97526061-518d9280-1976-11eb-9ba9-040be5203cb1.PNG">
5.Una vez finalizado el proceso, haga clic en la imagen del sitio para lanzar el sitio de Web.
<img width="958" alt="desplegada" src="https://user-images.githubusercontent.com/72947118/97526085-610cdb80-1976-11eb-9fc0-2afb9c5caa27.PNG">
Modificación del sitio.
Modificando la linea del titulo  “index.html”  <title>Wild Rydes - Rydes of the Future!</title>
git:
<img width="447" alt="gitUpdate" src="https://user-images.githubusercontent.com/72947118/97526933-2c9a1f00-1978-11eb-9090-a1eabd7f2183.PNG">
resultado:
<img width="161" alt="cambio titulo" src="https://user-images.githubusercontent.com/72947118/97526982-4176b280-1978-11eb-8c1d-d5321fc9609f.PNG">

Crear un grupo de usuarios de Amazon Cognito
1 En servicios buscar cognito
<img width="730" alt="cognito" src="https://user-images.githubusercontent.com/72947118/97528264-47ba5e00-197b-11eb-8979-0b7684ee8395.PNG">
2crear un grupo de usuarios llamado WildRydes seleccionando Review Defaults (Revisar valores predeterminados).
<img width="738" alt="cerando grupoPNG" src="https://user-images.githubusercontent.com/72947118/97528319-6b7da400-197b-11eb-87cd-a16552a69912.PNG">
<img width="941" alt="grupoUsuariocread" src="https://user-images.githubusercontent.com/72947118/97528283-56a11080-197b-11eb-8b71-ae3d1450913f.PNG">

Añadir una aplicación al grupo de usuarios
Se crea usuario que tendra acceso  a la aplicación
<img width="469" alt="grup" src="https://user-images.githubusercontent.com/72947118/97528926-d67baa80-197c-11eb-94d1-76d90c4b85fe.PNG">

<img width="464" alt="clientecreado" src="https://user-images.githubusercontent.com/72947118/97528950-e72c2080-197c-11eb-84f0-d0ca20475e70.PNG">

Actualización sitio web
Edicion de js/config.js
<img width="766" alt="edicion" src="https://user-images.githubusercontent.com/72947118/97529733-86054c80-197e-11eb-87f9-20789a899da3.PNG">
<img width="423" alt="gitacceso" src="https://user-images.githubusercontent.com/72947118/97529669-64a46080-197e-11eb-87db-36256d658dc9.PNG">

Validar su implementación
Crear cuenta en la pagia 
<img width="510" alt="registro" src="https://user-images.githubusercontent.com/72947118/97530472-36278500-1980-11eb-9f28-f3fb83272bd5.PNG">
Como coloque mi correo personal llego la notificacion y autenqtiue cirrectamente.
![codigo](https://user-images.githubusercontent.com/72947118/97530710-b1893680-1980-11eb-91ce-4cc7013c8d5c.jpeg)
Ahora me logueare.
<img width="453" alt="registro correcto" src="https://user-images.githubusercontent.com/72947118/97530568-68d17d80-1980-11eb-8fa1-26f3b979c3a6.PNG">

Crear una tabla de Amazon DynamoDB llamada Rides y asígnele una clave de partición llamada RideId con el tipo String (Cadena).
<img width="332" alt="accesodinamo" src="https://user-images.githubusercontent.com/72947118/97532233-df23af00-1983-11eb-97f3-cd1dfa4b8b94.PNG">
<img width="926" alt="creacion tabla" src="https://user-images.githubusercontent.com/72947118/97532327-1befa600-1984-11eb-8f59-a31c203d24b1.PNG">
Crear un rol de IAM para su función Lambda
<img width="899" alt="rolesiam" src="https://user-images.githubusercontent.com/72947118/97534970-e4372d00-1988-11eb-9c63-992244623b72.PNG">
seleccionamos lambda
<img width="814" alt="rol3" src="https://user-images.githubusercontent.com/72947118/97535087-147ecb80-1989-11eb-886a-5856bcefb828.PNG">
Espefificamos el tipo de rol
<img width="830" alt="rol2" src="https://user-images.githubusercontent.com/72947118/97535015-f749fd00-1988-11eb-831b-74d857fe2250.PNG">

creamos el rol con el nombre WildRydesLambda
<img width="814" alt="rol3" src="https://user-images.githubusercontent.com/72947118/97535249-590a6700-1989-11eb-83d1-84d09a8af4b6.PNG">

Agregamos una politica insertada llamada DynamoDBWriteAccess 
<img width="580" alt="polity3" src="https://user-images.githubusercontent.com/72947118/97535403-9a9b1200-1989-11eb-8a77-a5c68bca8948.PNG">

<img width="780" alt="polity2" src="https://user-images.githubusercontent.com/72947118/97535415-9ec72f80-1989-11eb-8d99-66fe25f374f7.PNG">

<img width="780" alt="polity1" src="https://user-images.githubusercontent.com/72947118/97535428-a25ab680-1989-11eb-8803-083002b8b17c.PNG">

Crear una función Lambda para administrar las solicitudes
<img width="866" alt="lambda" src="https://user-images.githubusercontent.com/72947118/97536605-67f21900-198b-11eb-9f89-ce88e0238809.PNG">
Al parecer el repositorio para tomar el js de base no funciona
<img width="469" alt="lambda1" src="https://user-images.githubusercontent.com/72947118/97536615-6cb6cd00-198b-11eb-9066-06a56bfde08e.PNG">

Probar implementacion
Se crea una test y se realiza prueba con codigo por defecto llamado TestRequestEvent 

<img width="874" alt="prueba" src="https://user-images.githubusercontent.com/72947118/97537872-7f320600-198d-11eb-8b43-1a723818e83f.PNG">

Crear un autorizador de grupos de usuarios de Cognito llamado WildRydes 
<img width="838" alt="api1" src="https://user-images.githubusercontent.com/72947118/97539875-bc4bc780-1990-11eb-96fd-ec308a1879c6.PNG">
Se verifica el autorizador
<img width="353" alt="api2" src="https://user-images.githubusercontent.com/72947118/97539899-c7065c80-1990-11eb-8915-eaecbfbc5647.PNG">
Se prueba direccionamiento
<img width="728" alt="api3prueba" src="https://user-images.githubusercontent.com/72947118/97539918-cd94d400-1990-11eb-8035-d2c5c3bd2f52.PNG">
se prueba autorización, la cual fallo me imagino que por el script anterior
que falto.
<img width="728" alt="api3prueba" src="https://user-images.githubusercontent.com/72947118/97540191-46942b80-1991-11eb-8fb6-88ee433348f0.PNG">
Crear un nuevo recurso y método
<img width="776" alt="service1" src="https://user-images.githubusercontent.com/72947118/97542429-b657e580-1994-11eb-9aef-0ee7f3b1306e.PNG">
se habilito el cross
<img width="794" alt="serviceo" src="https://user-images.githubusercontent.com/72947118/97542439-b952d600-1994-11eb-81df-e1312861d49e.PNG">
se implemento
<img width="721" alt="implement1" src="https://user-images.githubusercontent.com/72947118/97542462-bfe14d80-1994-11eb-9f15-5a34a336e4b1.PNG">
Actualizar la configuración del sitio web, se edita el archivo index.js
<img width="882" alt="conf" src="https://user-images.githubusercontent.com/72947118/97543077-b99fa100-1995-11eb-8793-956deffc8f43.PNG">
se sube al repositorio
<img width="490" alt="conf1" src="https://user-images.githubusercontent.com/72947118/97543082-bb696480-1995-11eb-871d-9aa7853cd709.PNG">
Validar su implementación la cual el final no funciono en mi caso.
<img width="490" alt="conf1" src="https://user-images.githubusercontent.com/72947118/97543657-890c3700-1996-11eb-981e-ee0b757b416c.PNG">

Muchas gracias
