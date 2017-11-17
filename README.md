# paqueteComposerExterno
Repositorio de prueba para descargar via composer

Definición de un paquete de tipo librería para utilizar con el manejador de dependencias composer. Básicamente permite agregar código a tus proyectos via composer (externo a packagist).

Primero en un repositorio (público) crear colocar el código fuente y el archivo composer.json en el raíz con la siguiente estructura (o similar) [https://github.com/lucasaguilar/paqueteComposerExterno/blob/master/composer.json]

Luego para utilizar un paquete externo en el composer.json de tu proyecto agregar lo siguiente, (ejemplo):

"repositories": [
     
        {
            "type": "git",
            "url":  "https://github.com/lucasaguilar/paqueteComposerExterno"
        }
    ],
    
    "minimum-stability" : "dev",
    "prefer-stable" : true
    
 ]
 
 Y luego ejecutar:  php composer.phar require isimultanea/componente-prueba:* --verbose (ultimo comando opcional)
 
 
Si todo sale bien (con un repo publico!!! ojo!):

Installs: isimultanea/componente-prueba:dev-master 95ea516
  - Installing isimultanea/componente-prueba (dev-master 95ea516): Cloning 95ea516fa589776dead16ccd5c1
  
Luego van a poder utilizar el código gestionado via composer e incluido por el autoloader.



Inspirado en:

https://stackoverflow.com/questions/12954051/use-php-composer-to-clone-git-repo

https://github.com/l3pp4rd/DoctrineExtensions/blob/master/composer.json
