A text scroller extension library for Micropython.

# Instructies
Hoe om deze lib te gebruiken.

1. Installereer Micropython op een ESP8266 bord bijvb Wemos D1 Mini.
2. Download <a href="http://thonny.org">Thonny</a> IDE en max7219.py van https://github.com/mcauser/micropython-max7219
3. Installeer Thonny, en upload max7219.py als 'script with current name.
4. Verbind een LED matrixbord aan jouw Micropython apparaat volgens SPI pin.
5. Check pinout specifiek aan jouw bord, bijvb pin=15 voor Wemos D1 mini, zoals vermeld op micropython-max7219 lib.
6.  

# Voorbeeld code:
```python
from Max7219Textscroller import MatrixTextscroller


def init():
    scoller1 = MatrixTextscroller()
    scoller1.debug = False
    scoller1.scrollText(textToScroll='    Hallo1239809876543210')


print('App start')
init()
print('App eind')
```

# Credits
door Michiel Erasmus
