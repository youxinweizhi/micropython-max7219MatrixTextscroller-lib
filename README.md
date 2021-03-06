A text scroller extension library for Micropython.

# Required:
max7219.py van https://github.com/mcauser/micropython-max7219

# Installeren
Hoe om deze lib te gebruiken.

1. Installereer <a href="http://Micropython.org">Micropython</a> op een ESP8266 bord bijvb Wemos D1 Mini.
2. Download <a href="http://thonny.org">Thonny</a> IDE en max7219.py van https://github.com/mcauser/micropython-max7219
3. Installeer Thonny, en upload max7219.py als 'script with current name.
4. Verbind een LED matrixbord aan jouw Micropython apparaat volgens SPI pin.
5. Check pinout specifiek aan jouw bord, bijvb pin=15 voor Wemos D1 mini, zoals vermeld op micropython-max7219 lib.
6. Run voorbeeld hieronder in ThonnyIDE.

Let op: laat jouw text altijd met 4x spaties voorlopen, anders scrollt hij te snel.

## Dependencies
Deze lib gebruikt max7219.py van https://github.com/mcauser/micropython-max7219

# Voorbeeld code:
Hoe je die lib gebruik.

## Voorbeeld 1 - default hallo world text
```python
from Max7219Textscroller import MatrixTextscroller

scoller1 = MatrixTextscroller()
scoller1.debug = False
scoller1.scrollText(textToScroll='     MAX7219 TUTORIAL')
```

bij start zult de scrpller een hello world tekstjes laten zien.


<img src='https://www.makerguides.com/wp-content/uploads/2020/06/MAX7219-LED-dot-matrix-display-Arduino-tutorial-scrolling-text.gif' alt='led matrix'/>

## Voorbeeld 2

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

Je kunt hem dan uitvoeren
```shell
MicroPython v1.11-8-g48dcbbe60 on 2019-05-29; ESP module with ESP8266

Type "help()" for more information. [backend=GenericMicroPython]
>>> %Run led_scroller_demo.py
  App start
  App eind
>>> 

```

# Credits
door Michiel Erasmus
