## Descripción 
How about trying to match a regular expression

Additional details will be available after launching your challenge instance.
## Hints
1. Access the webpage and try to match the regular expression associated with the text field
## Solución
```
|   |
|---|
|function send_request() {|
|let val = document.getElementById("name").value;|
|// ^p.....F!?|
|fetch(`/flag?input=${val}`)|
|.then(res => res.text())|
|.then(res => {|
|const res_json = JSON.parse(res);|
|alert(res_json.flag)|
|return false;|
|})|
|return false;|
|}|

^p.....F!?| == picoCTF{}

el match es picoCTF{}

picoCTF{succ3ssfully_matchtheregex_f89ea585}
```
## Notas

## Referencias
