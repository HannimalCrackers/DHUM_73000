# Adventures in parseltongue

&nbsp;


#### Tell me a number
num = int(input("Hello, tell me a number: ")) <br>
print("Thank you.") <br>

if num % 2 == 0: <br>
    &nbsp;&nbsp; print ("That was an even number.") <br>
else: <br>
    &nbsp;&nbsp; print("That was an odd number.")


#### My first Python script
name = input("Hello, what is your name? ") <br>
age = input("Hello again, how old are you? ") <br>
age = int(age) <br>
year = str((100-age)+2018) <br>
print ("\n") <br>
print ("Hello, " + name + ". You will be 100 years old this time of year in " + year + ".")




&nbsp; &nbsp; &nbsp; &nbsp;

Markdown is interacting with my copy/paste Python from Terminal. Having to manually insert input line breaks. Some may be missing.

&nbsp; &nbsp;

## Mathing with pet names

&nbsp; &nbsp;

>>> Earnest = 10000 <br>
>>> print(Earnest)
#### 10000

&nbsp;

>>> Earnest = 5 < 8 <br>
>>> print (Earnest)
#### True

&nbsp;

>>> print("Duvel" + "Bear")
#### DuvelBear

>>> print ("Duvel " + "Bear")
#### Duvel Bear

&nbsp;

>>> ExtraKitty = 100 <br>
>>> print (ExtraKitty > 6)
#### True

&nbsp;

>>> print ("Duvel " * 3)
#### Duvel Duvel Duvel 

&nbsp;

>>> ss = "Extra Kitty" <br>
>>> print(ss.upper())
#### EXTRA KITTY

 &nbsp;
 
>>> Earnest = "I'm going to eat too fast and puke and then eat that" <br>
>>> print (len(Earnest))
#### 52

&nbsp;

>>> Duvel = "Little orange sunshine" <br>
>>> " ".join(Duvel)
#### 'L i t t l e   o r a n g e   s u n s h i n e'

&nbsp;

>>> print("".join(reversed(Duvel)))
#### enihsnus egnaro elttiL

&nbsp;

 
>>> print(" ; ".join(["Earnest", "Extra Kitty" , "Duvel"]))
#### Earnest ; Extra Kitty ; Duvel

&nbsp; 

>>> Duvel = "Little orange sunshine" <br>
>>> print (Duvel.split())
#### ['Little', 'orange', 'sunshine']
&nbsp;
>>> NewList = (Duvel.split())
>>> print (NewList)
#### ['Little', 'orange', 'sunshine']
&nbsp;
>>> print (" ; ".join(NewList))
#### Little ; orange ; sunshine


&nbsp;

>>> name, hex = "Seafoam Blue", "89BBBC" <br>
>>> print (name)
#### Seafoam Blue
>>> print (hex)
#### 89BBBC
>>> print ("#" + hex)
#### #89BBBC

&nbsp; 

>>> x = "Earnest loves {} and {}." <br>
>>> print(x.format("treats","hugs"))
#### Earnest loves treats and hugs.

&nbsp; &nbsp;

# Things to be learned

&nbsp;

## Something going wrong here with the line breaks
&nbsp;

>>> ''' <br>
... As the wise Ralph said <br>
... My cats breath smells like cat food <br>
... This was a haiku <br>
... '''
#### '\nAs the wise Ralph said\nMy cats breath smells like cat food\nThis was a haiku\n'
&nbsp;

I don't understand **line breaks and escape characters**. Research later.

&nbsp; &nbsp; 

## Learn how to call values from dictionaries

>>> MyColor = {'name': 'seafoam blue', 'hex': '89BBBC'} <br>
>>> print(MyColor.hex)
#### Traceback (most recent call last):
#### File "<stdin>", line 1, in <module>
#### AttributeError: 'dict' object has no attribute 'hex' <br>
>>> print(hex.MyColor)
 
#### Traceback (most recent call last):
#### File "<stdin>", line 1, in <module>
#### AttributeError: 'builtin_function_or_method' object has no attribute 'MyColor'
>>> 

&nbsp; &nbsp; &nbsp; &nbsp;
  

< [There's no place like home](./index.md)
