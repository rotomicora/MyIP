# MyIP
**Simple programa que muestra tu IP, país, y tu código de país con la API de [myip.com](https://myip.com)**

<p><img src="https://user-images.githubusercontent.com/48841069/212543043-a08e0787-0049-4d01-bcbc-736724c45333.png" height="400px" alt="franafp myip"></p>

# Code

```python
# Importamos los modulos que usaremos
import os, requests
from pystyle import Write, Colors

iprequest = requests.get("https://api.myip.com").json() # Hacemos una peticion a la API de myip.com
ip = iprequest["ip"] # Definimos la variable ip con el valor de la IP que nos devuelve la API
country = iprequest["country"] # Definimos la variable country con el valor del pais que nos devuelve la API
cc = iprequest["cc"] # Definimos la variable cc con el valor del codigo del pais que nos devuelve la API

os.system("title franafp - MyIP") # Definimos el titulo de la consola
while True: # Creamos un bucle infinito al pulsar cualquier tecla para refrescarlo infinitamente
    os.system("cls") # Limpiamos la consola
    Write.Print(f"[MyIP] User: {os.getlogin()}\n", Colors.green_to_yellow, interval=0.02) # Mostramos el usuario del sistema operativo
    Write.Print(f"[MyIP] IP: {ip}\n", Colors.green_to_yellow, interval=0.02) # Mostramos la IP
    Write.Print(f"[MyIP] Country: {country}\n", Colors.green_to_yellow, interval=0.02) # Mostramos el pais
    Write.Print(f"[MyIP] Country Code: {cc}\n", Colors.green_to_yellow, interval=0.02) # Mostramos el codigo del pais
    os.system("pause >nul") # Una pausa para refrescar la consola
```

# Credits
<p align="center">
<a href="https://www.twitter.com/fran_afp_" target="_blank" rel="noreferrer"><img
src="https://img.shields.io/twitter/follow/fran_afp_?logo=twitter&style=for-the-badge&color=0891b2&labelColor=1c1917"
/></a><a href="https://www.github.com/franafp" target="_blank" rel="noreferrer"><img
src="https://img.shields.io/github/followers/franafp?logo=github&style=for-the-badge&color=0891b2&labelColor=1c1917" /></a>
 <a><img alt="YouTube Channel Views" src="https://img.shields.io/youtube/channel/views/UCDIMj1pa2HqUMegbemddwCw?color=0891b2&label=VIEWS&logo=youtube&logoColor=FF0000&style=for-the-badge&labelColor=1c1917"></a>
 <a><img href="https://franafp.es" src="https://img.shields.io/badge/website-franafp.es-0891b2?style=for-the-badge&logo=data:image/png;base64,aHR0cHM6Ly9mcmFuYWZwLmVzL21lZGlhL2toZWlzLnBuZw==&logoWidth=14&color=0891b2&labelColor=1c1917"></a>
</p>
