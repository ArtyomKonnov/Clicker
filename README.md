# Clicker
from tkinter import*
from tkinter import messagebox
num = 0
def click():
    global num
    num += 1
    label.configure(text =  f'Счёт:{num}')
    if num == 10:
        messagebox.showinfo('Молодец','Ты прошёл уровень :Лёгкий')
    if num == 100:
        messagebox.showinfo('Молодец','Ты прошёл уровень :Нормальный')
    if num == 500:
        messagebox.showinfo('Молодец','Ты прошёл уровень :Сложный')
    if num == 1000:
        messagebox.showinfo('Молодец','Ты прошёл уровень :Трудный')
    if num == 10000:
        messagebox.showinfo('Молодец','Ты прошёл уровень :Невозможный')
        label.configure(text = 'Игра окончена')
        if num == 10001:
            label.configure(text = 'Игра окончена')
            messagebox.showinfo('', 'Чтобы начать с начала, вы должны перезапустить игру')
        
root = Tk()
root['bg']='white'
root.title('Clicker')
root.geometry('700x500')
label=Label(text='Счёт:0',height=5,width=100,font='consolas',fg='black', bg ='white' )
button=Button(text='Click', height=15, width = 30,command=click,bg='blue')
label.pack()
button.pack(side=BOTTOM)
root.mainloop()
