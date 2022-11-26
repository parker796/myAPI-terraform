# myAPI-terraform
es un proyecto usando terraform para levantar en un contenedor de docker jenkins
para correr este proyecto tenemos que ejecutar
1) terraform init
2) sudo terraform apply le ponemos yes una vez creada la imagen de jenkins
en docker 
3) abrimos en el navegador el puerto para ver jenkins http://localhost:8080/
4)nos pide una contraseña la sacamos con el comando sudo docker exec jenkins cat /var/jenkins_home/secrets/initialAdminPassword
una ves que sacamos la contraseña la ingresamos en jenkins 
5)dentro de jenkins nos vamos a manage jenkins e install plugins 
instalamos estos plugins Pipeline
Docker
Docker Pipeline
Environment Injector
Git
GitHub
GitHub Authenticator 
una vez instalado metemos las variables de ambiente en configure system
MYSQL_IP la vemos dentro de nuestra terminal cuando ejecutamos terraform en el value
MYSQL_PASSWORD el valor se encuentra en la parte de mysql que es la contraseña
MYSQL_USER ponemos de valor root
por ultimo creamos el pipeline en jenkins poniendo como ejecucion el git que tenemos en https://github.com/parker796/myAPI-books.git o podemos probar este igual https://github.com/parker796/myAPI-accounts.git

