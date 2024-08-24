# pokelib2

```
pip install git+https://github.com/novast1024/pokelib2
```
import
```
from pokelib.combo import *
from pokelib.constants import *
from pokelib import settings
```
initialize
```
settings.python_command = self
settings.input_seconds = 0.05
settings.minimum_interval = 0.05
```
```
from Commands.PythonCommandBase import PythonCommand, ImageProcPythonCommand

from pokelib import settings
from pokelib.constants import *
from pokelib.combo import *

class Test(ImageProcPythonCommand):
    NAME = "テスト"

    def do(self):
        settings.python_command = self
        settings.input_seconds = 0.01
        settings.minimum_interval = 0.0

        c = Combo()
        for i in range(0, 360, 15):
            c += Combo(LS.UP.rotate(i))
        
        send(c*5)
```
