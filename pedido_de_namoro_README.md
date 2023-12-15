import tkinter as tk
from tkinter import *
import random
from tkinter import messagebox

def move_button_1(e):
    if abs(e.x - button_1.winfo_x()) < 50 and abs(e.y - button_1.winfo_y()) < 50:
        x = random.randint(0, root.winfo_width() - button_1.winfo_width())
        y = random.randint(0, root.winfo_height() - button_1.winfo_height())
        button_1.place(x=x, y=y)

def accepted():
    messagebox.showinfo('Meu amor', 'Eu te amo meu amor, lanchinho mais tarde?')

def denied():
    button_1.destroy()

root = tk.Tk()
root.title('Aceitas?')
root.geometry('600x600')
root.configure(background='#4169E1')

margin = Canvas(root, width=500, bg='#4169E1', height=100, bd=0, highlightthickness=0, relief='ridge')
margin.pack()

text_id = Label(root, bg='#4169E1', text='Quer namorar comigo?', fg='#FFFFFF', font=('Montserrat', 24, 'bold'))
text_id.pack()

button_1 = tk.Button(root, text='Não', bg='#0000CD', command=denied, relief=RIDGE, bd=3, font=('Montserrat', 8, 'bold'), fg='#FFFFFF')
button_1.pack()

root.bind('<Motion>', move_button_1)

button_2 = tk.Button(root, text='Sim', bg='#0000CD', relief=RIDGE, bd=3, command=accepted, font=('Montserrat', 14, 'bold'), fg='#FFFFFF')
button_2.pack()

root.mainloop()

<!---
HOOKITINHA/HOOKITINHA is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
