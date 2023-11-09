# Api-Whatsapp
Este es un proyecto pensado para crear un chatbot utilizando node y python utilizando la api gratuita de whatsapp.js. Estes proyecto fue inspirado en los videos de Leifer Mendez y con codigo extra para utilizarlo con python. Aparte de todo lo mencionado en el video, la funcion de sendMessage se puede utilizar para infinidad de utilidades en Python, tanto asi como para utilizarla con tkinter, django, etc.

# Pasos para realizar el proceso

Paso 1:
```
git clone https://github.com/leifermendez/api-whatsapp-ts

```

Paso 2:
```
cd api-whatsapp-ts

```

Paso 3:
```
npm install

```

Paso 4:
```
npm run build

```

Paso 5:
```
npm run dev

```

Paso 6:
Crear un archivo .py con el siguiente codigo y luego ejecutarlo.
```
import requests
import time 

def sendMessage(para, mensaje):
    url = 'http://localhost:3001/lead'
    
    data = {
        "message": mensaje,
        "phone": para
    }
    headers = {
        'Content-Type':'application/json'
    }
    print(data)
    response = requests.post(url, json=data, headers=headers)
    time.sleep(10)
    return response
```
Paso 7:
en el archivo .py creado en el punto anterior agregar la siguiente linea especificando un numero de telefono real al que se va a mandar el mensaje y el mensaje correspondiente entre ''
```
sendMessage('XXXXXXXXX', 'Este es el mensaje')
```
