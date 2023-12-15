import tkinter as tk
from time import strftime
def time():
    string = strftime('%H:%M:%S %p')
    label.config(text=string)
    label.after(1000, time)  
root = tk.Tk()
root.title("Relógio Digital")

label = tk.Label(root, font=('calibri', 40, 'bold'), background='purple', foreground='white')
label.pack(anchor='center')

time()

root.mainloop()


<!---
HOOKITINHA/HOOKITINHA is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
