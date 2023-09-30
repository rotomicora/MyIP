# MyIP
**Simple programa que muestra tu IP, país, y tu código de país con la API de [myip.com](https://myip.com)**


# Code

```python
# Importamos los modulos que usaremos
import os, requests
from pystyle import Write, Colors

iprequest = requests.get("https://api.myip.com").json() # Hacemos una peticion a la API de myip.com
ip = iprequest["ip"] # Definimos la variable ip con el valor de la IP que nos devuelve la API
country = iprequest["country"] # Definimos la variable country con el valor del pais que nos devuelve la API
cc = iprequest["cc"] # Definimos la variable cc con el valor del codigo del pais que nos devuelve la API

os.system("title MyIP") # Definimos el titulo de la consola
while True: # Creamos un bucle infinito al pulsar cualquier tecla para refrescarlo infinitamente
    os.system("cls") # Limpiamos la consola
    Write.Print(f"[MyIP] User: {os.getlogin()}\n", Colors.green_to_yellow, interval=0.02) # Mostramos el usuario del sistema operativo
    Write.Print(f"[MyIP] IP: {ip}\n", Colors.green_to_yellow, interval=0.02) # Mostramos la IP
    Write.Print(f"[MyIP] Country: {country}\n", Colors.green_to_yellow, interval=0.02) # Mostramos el pais
    Write.Print(f"[MyIP] Country Code: {cc}\n", Colors.green_to_yellow, interval=0.02) # Mostramos el codigo del pais
    os.system("pause >nul") # Una pausa para refrescar la consola
```

