# Adventures in parseltongue

Hmmm, markdown is interacting with my copy/paste Python from Terminal

&nbsp; &nbsp; &nbsp; &nbsp;

## Mathing with pet names

&nbsp; &nbsp;

>>> Earnest = 10000
>>> print(Earnest)
#### 10000

&nbsp;

>>> Earnest = 5 < 8
>>> print (Earnest)
#### True

&nbsp;

>>> print("Duvel" + "Bear")
#### DuvelBear

>>> print ("Duvel " + "Bear")
#### Duvel Bear

&nbsp;

>>> ExtraKitty = 100
>>> print (ExtraKitty > 6)
#### True

&nbsp;

>>> print ("Duvel " * 3)
#### Duvel Duvel Duvel 

&nbsp;

>>> ss = "Extra Kitty"
>>> print(ss.upper())
#### EXTRA KITTY

 &nbsp;
 
>>> Earnest = "I'm going to eat too fast and puke and then eat that"
>>> print (len(Earnest))
#### 52

&nbsp;

>>> Duvel = "Little orange sunshine"
>>> " ".join(Duvel)
#### 'L i t t l e   o r a n g e   s u n s h i n e'

&nbsp;

>>> print("".join(reversed(Duvel)))
#### enihsnus egnaro elttiL

&nbsp;

>>> SpaciousDuvel = ("  ".join(Duvel))
>>> print(SpaciousDuvel)
#### L  i  t  t  l  e     o  r  a  n  g  e     s  u  n  s  h  i  n  e

 &nbsp;
 
>>> print(" ; ".join(["Earnest", "Extra Kitty" , "Duvel"]))
### Earnest ; Extra Kitty ; Duvel

&nbsp; 

>>> Duvel = "Little orange sunshine"
>>> print (Duvel.split())
#### ['Little', 'orange', 'sunshine']
>>> NewList = (Duvel.split())
>>> print (NewList)
#### ['Little', 'orange', 'sunshine']
>>> print (" ; ".join(NewList))
#### Little ; orange ; sunshine


&nbsp;

>>> name, hex = "Seafoam Blue", "89BBBC"
>>> print (name)
#### Seafoam Blue
>>> print (hex)
#### 89BBBC
>>> print ("#" + hex)
#### #89BBBC

&nbsp; &nbsp;



# Things to be learned

&nbsp;

## Something going wrong here with the line breaks
&nbsp;

>>> '''
... As the wise Ralph said
... My cats breath smells like cat food
... This was a haiku
... '''
#### '\nAs the wise Ralph said\nMy cats breath smells like cat food\nThis was a haiku\n'
&nbsp;

I don't understand **line breaks and escape characters**. Research later.

&nbsp; &nbsp; 

## Learn how to call values from dictionaries

>>> MyColor = {'name': 'seafoam blue', 'hex': '89BBBC'}
>>> print(MyColor.hex)
#### Traceback (most recent call last):
#### File "<stdin>", line 1, in <module>
#### AttributeError: 'dict' object has no attribute 'hex'
>>> print(hex.MyColor)
 
#### Traceback (most recent call last):
#### File "<stdin>", line 1, in <module>
#### AttributeError: 'builtin_function_or_method' object has no attribute 'MyColor'
>>> 

&nbsp; &nbsp; &nbsp; &nbsp;
  

< [There's no place like home](./index.md)
