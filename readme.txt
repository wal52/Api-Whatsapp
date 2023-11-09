git clone https://github.com/leifermendez/api-whatsapp-ts
cd api-whatsapp-ts
npm install
npm run build
npm run dev


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
sendMessage('5493795301804', 'Hola')