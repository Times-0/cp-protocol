Action `rndK`
============

__Action name__ : `rndK`

__Action abbreviation__ : `Request client's random key`

## Flow of XML Packet
1. Responses to client with the random key generated, which is used during client's password authentication process.

## Packet Structure
```xml
<msg t='sys'>
  <body action='rndK' r='-1'>
    <k> <![CDATA[RANDOMKEY*]]> </k>
  </body>
</msg>
```
__NOTE__ : HERE `RANDOMKEY` is a variable string, varies from client to client and from one login request to another. It's advised to keep it a random one than a static key. It's also advised to send it as `CDATA` to prevent loss of data due to presence of `<>!--` in the key.

## Example of usage
```py
import random

#example of random key generation
def generateRndK (length=10):
    strings = list ('1234567890ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz!?;:"-/^&*()#@+×÷=%_,.<>{}[]|\\~`')
    
    return ''.join (random.choice(strings) for i in range(length))

def randomKey (client, request):
    random_key = client.authentication.randomKey
    client.sendXML (action = 'rndK', r = '-1', params = random_key)
```
