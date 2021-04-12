# CCI_ACC_W3_PythonTextGame
This is a simple text game in Python, and I also wrote my answer in the document; if I have more ability to write plots or mathematics, there should be a more exciting and rich story:

```python
"""
--- readMe ---
I added some obfuscator,
and the code under print("Task...") should be written by the player
I have provided some examples.
The normal version can be viewed in copy_main.py


--- BRGIN ---
one day, an email appeared in your mailbox:
ouch! dear friends, their plan has already begun...you have to give this code to Math as soon as...

FIBONA in CCI <20

attachment：secretImage.png
"""

# You don't know who send the mail...and check the .png, where is the code?
# Maybe you should find one way to convert it to ..string?

msg = input("Task1: convert the image to base64...Yes?")


import base64
import time
from PIL import Image
from io import BytesIO


# how to solve the Q1
def get_base64_encoded_image(image_path):
    with open(image_path, "rb") as img_file:
        return base64.b64encode(img_file.read()).decode('utf-8')

data = get_base64_encoded_image('secretImage.png')
print(type(data))
print(data)
print(len(data))
print(data[0])


"""
but...who would choose a 3048 password? maybe we need to further filter the data...
you check the email again and notice "FIBONA in CCI <20"
...Fibonacci sequence? (I can't make up this story =_=!)
"""

# Then you try to use the Fibonacci sequence and try to mix array again
msg = input("Task2: Create a Fibonacci list of size=19...yes?")

# how to solve the Q2
array = [0, 1]
mix_array = []

def fibonacci():
    count = 2
    n1 = 0
    n2 = 1
    nterms = 19
    while count < nterms:
        nth = n1 + n2
        array.append(nth)
        n1 = n2
        n2 = nth
        count += 1
    else:
        print(array)

def mapcode():
    for i in array:
        mix_array.append(data[i])
        print(data[i], end = '')
    print()
    print(mix_array)


fibonacci()
mapcode()


"""
Great! You finally got a bunch of keys, but termina...
"""


print('???:who are there?')
time.sleep(2)
print('???:who are there???')
time.sleep(2)

msg_count = 0
while msg_count <= 20:
    print("Warning!warning!")
    msg_count += 1
    time.sleep(0.5)

# Although you don't know what happened. . But you know you need to escape
# But no matter how you type on the keyboard, nothing happens

print("Data[] overflow_index1:[2] [0] [8]")
print("Data[] overflow_index2:[2] [4] [10] [78] [67] [19] [4]")
print("Data[] overflow_index3:[0] [16]")
print("Data[] overflow_index4:[5] [13] [78] [32] [67] [0] [15] [9]")
print("Data[] overflow_index5:[76] [10] [17]")

msg = input("Task3:print those data, check in data?...yes?")

# how to solve the Q3
print()
print(data[2],data[0],data[8])
print(data[2],data[4],data[10],data[78],data[67],data[19],data[4])
print(data[0],data[16])
print(data[5],data[13],data[78],data[32],data[67],data[0],data[15],data[9])
print(data[76],data[10],data[17])


"""
The end?

I want to create a sense of tension through a cold interactive method like the command line, 
but it's obvious...I lack sufficient skills and interactive methods, 
such as richer command line interaction, simple digital interface, etc., 
or make the terminal more active and intelligent =_=!
"""
```

```
"""
88888888888888888888888888888888888888888888888888888888888888888888888888888888
88888888888888888888888888888888888888888888888888888888888888888888888888888888
88888888888888888888888888888888888888888888888888888888888888888888888888888888
88888888888888888888888888888888888888888888888888888888888888888888888888888888
88888888888888888888888888888888888888888888888888888888888888888888888888888888
88888888888888888888888888888888888888888888888888888888888888888888888888888888
88888888888888888888888888888888888888888888888888888888888888888888888888888888
88888888888888888888888888888888888888888888888888888888888888888888888888888888
88888888888888888888888888888888888888888888888888888888888888888888888888888888
88888888888888888888888888888888888888888888888888888888888888888888888888888888
88888888888888888888888888888888888888888888888888888888888888888888888888888888
888888888888888888888888888888888888888888888888888#dddd*88888888888888888888888
888888888888888888888888888888888888888888888888888C....z88888888888888888888888
888888888888888888888888888888888888888888888888888J    z88888888888888888888888
8888888888888OUUULW88888kUUUUk8888&bQcr/\/jvJqM8888J    z8888*mmmmp&888888888888
8888888888888~   ,#88888X    X88Wci.  ^l!l`  .Ic&88J    z8888U    lW888888888888
8888888888888+   ;#88888Y    Y88QI;l!vM888*~   `h88J    z8888C::::+W888888888888
8888888888888+   ;#88888Y    Y88&&#bmZLYvj}^   `k88J    z8888W*##*#8888888888888
8888888888888+   ;M88888Y    Y88d|!^..:i~-(>   ^k88J    z88888888888888888888888
8888888888888-   `q8888W}    Y8*;   ib&8888?   ^k88J    z8888oZmmZq&888888888888
8888888888888z    :[aa\i.    Y8#!   :XZwZX?    'b88J    c8888U    lW888888888888
88888888888888C?;`   'l\CI:::C88k/i".  '"l1t::::L88Q::::U8888C::::+W888888888888
8888888888888888#kpqdo&88####W8888&obqpbo&88####M88W####W8888W#####&888888888888
88888888888888888888888888888888888888888888888888888888888888888888888888888888
88888888888888888888888888888888888888888888888888888888888888888888888888888888
88888888888888888888888888888888888888888888888888888888888888888888888888888888
88888888888888888888888888888888888888888888888888888888888888888888888888888888
88888888888888888888888888888888888888888888888888888888888888888888888888888888
88888888888888888888888888888888888888888888888888888888888888888888888888888888
88888888888888888888888888888888888888888888888888888888888888888888888888888888
88888888888888888888888888888888888888888888888888888888888888888888888888888888
88888888888888888888888888888888888888888888888888888888888888888888888888888888
88888888888888888888888888888888888888888888888888888888888888888888888888888888
88888888888888888888888888888888888888888888888888888888888888888888888888888888
"""
```

