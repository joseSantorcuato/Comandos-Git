Comandos básicos Github.
José Santorcuato Tapia
santorcuato76@gmail.com
Chile 2017

Configuración local:

sudo apt-get install git

ssh-keygen

git config --global color.ui true
git config --global user.name "tuUsuario"
git config --global user.email "tuUsuario@xmail.com"
ssh-keygen -t rsa -b 4096 -C "tuUsuario@xmail.com"

cat ~/.ssh/id_rsa.pub

Obtienes el Key SHH para establecer conexión con Github (Copia el resultado en las claves Ssh)

Prueba que se establezca la conexión:

ssh -T git@github.com

Ahora clonamos el repositorio

git clone https://github.com/tuUsuarioGit/repositorioAClonar

Clona un repositorio de Github luego:

cd repositorioAClonar

git status

git add -A agrega todos los archivos

Con un editor de texto tipo atom crea un archivo que se llame README

git add README

git commit -m "Comandos básicos de Github 01/02/2017"
//git commit -m "Comentario que describe al archivo, fecha de creación, modificación, etc"

git push origin master

Solicita nombre de usuario Github:

Username for 'https://github.com':

Password for 'https://tuUsuario@github.com':

Counting objects: x, done.
Delta compression using up to x threads.
Compressing objects: 100% (x/x), done.
Writing objects: 100% (x/x), x bytes | 0 bytes/s, done.
Total x (delta 0), reused 0 (delta 0)
To https://github.com/tuUsuario/repositorio
 * [new branch]      master -> master

Cambio de lenguaje para mostrar en repositorio

Crear archivo raíz .gitattributes

*.php linguist-language=Ruby // interpreta php como ruby
*.rb linguist-language=Ruby // interpreta .rb como ruby
