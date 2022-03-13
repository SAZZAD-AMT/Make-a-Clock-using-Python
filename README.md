# Make-a-Clock-using-Python

- Install all importent pip
- make a clock using python
- make a datetime using python
- clock and datetime project
---
<h1> JUST FOR CLOCK </h1>

- Import file :

```
from tkinter import *
from tkinter.ttk import *
from time import strftime
```
```
root=Tk()
root.title("Clock")

def time():
    string= strftime('%H:%M:%S %p')
    label.config(text=string)
    label.after(1000,time)

label = Label(root,font=("ds-digital",80),background="black",foreground="cyan")
label.pack(anchor="center")
time()

mainloop()
```
---
<h1> CLOCK AND DATE </h1>

FULL CODE :

```
from datetime import datetime
from tkinter import *
import tkinter 
import pyglet

pyglet.font.add_file('DS-DIGIT.TTF')

cor1="#3d3d3d"
cor2="#21c25c"

root=Tk()
root.title("CLOCK")
root.geometry('450x180')
root.resizable(width= FALSE, height=FALSE)
root.configure(background=cor1)

def clock():
    time=datetime.now()
    hour=time.strftime("%I:%M:%S")
    weekday=time.strftime("%A")
    day=time.day
    month=time.strftime("%b")
    year=time.strftime("%Y")
    l1.config(text=hour)
    l1.after(200, clock)

    l2.config(text=weekday +" "+ "/"+str(day)+ "/" + str(month) + "/" + (year))


l1= Label(root,font=('Arial 80'),bg=cor1,fg=cor2)
l1.grid(row=0,column=0,sticky=NW)

l2= Label(root,font=('Arial 20'), bg=cor1, fg=cor2)
l2.grid(row=1,column=0,sticky=NW)

clock()
root.mainloop()
```
---
<h1>THANK YOU </h1>