import math
import tkinter as tk
window = tk.Tk()
window.title('Calculator')
#Calculator
a = [0]
b = [0]
c = [1]
i = [10]
bool_point = [False,False]#[False,False]で初期化,小数点以下の計算を含むか判断,
#[False,False]→整数部分,[True,False]→小数第2位以下,[False,False]→小数第1位,b15により[True,True]に
bool_op = [False,False]
bool_calculation_error = [False]


l0 = tk.Label(window,text = '0',width = 25,height = 5)
l1 = tk.Label(window,text = '',width = 25,height = 5)

def Calculation_error():
    l1.configure(text = 'Calculation error')


def Delete():
    l1.configure(text ='')

entry = tk.Entry(window)
entry.insert(0,'0')

def Calculationj(j):
    if bool_calculation_error[0]:
        Calculation_error()
    else:
        bool_op[1] = False
        z = entry.get()
        display = float(z)
        if bool_point[1] and display.is_integer():
            bool_point[1] = False
            y = display+j/10
            x = str(y)
        elif bool_point[0]:
            x = z+str(j)
        else:
            y = 10*display+j
            x = str(y)
        entry.delete(0,tk.END)
        entry.insert(0,x)
        entry_text = entry.get()
        l0.configure(text = entry_text)


def Calculation0():
    j = 0
    Calculationj(j)


def Calculation1():
    j = 1
    Calculationj(j)


def Calculation2():
    j = 2
    Calculationj(j)


def Calculation3():
    j = 3
    Calculationj(j)


def Calculation4():
    j = 4
    Calculationj(j)


def Calculation5():
    j = 5
    Calculationj(j)


def Calculation6():
    j = 6
    Calculationj(j)


def Calculation7():
    j = 7
    Calculationj(j)


def Calculation8():
    j = 8
    Calculationj(j)


def Calculation9():
    j = 9
    Calculationj(j)


def addition():
    a[0] = a[0]+b[0]
    b[0] = 0
    c[0] = 1


def subtracton():
    a[0] = a[0]-b[0]
    b[0] = 0
    c[0] = 1


def multiplation():
    a[0] = a[0]*c[0]
    c[0] = 1
    b[0] = 0


def division():
    if c[0] == 0:
        bool_calculation_error[0] = True
        Calculation_error()
    else:
        a[0] = a[0]/c[0]
        b[0] = 0
        c[0] = 1


def Calculation_special(): #演算子が連続して押された時の対応
    if bool_calculation_error[0]:
        Calculation_error()
    else:
        bool_point[0] = False
        bool_point[1] = False
        z = entry.get()
        if bool_op[0]:
            bool_op[0] = False
            b[0] = 0
            c[0] = 1
            if i[0] == 10:
                addition()
            elif i[0] == 11:
                subtracton()
            elif i[0] == 12:
                multiplation()
            else:
                division()
        else:
            a[0] = float(z)
        x = str(a[0])
        entry.delete(0,tk.END)
        entry.insert(0,x)
        l0.configure(text = x)


def Calculation14():
    if bool_calculation_error[0]:
        Calculation_error()
    else:
        bool_point[0] = False
        bool_point[1] = False
        z = entry.get()
        if bool_op[0]:
            bool_op[0] = False
            b[0] = float(z)
            c[0] = float(z)
            if i[0] == 10:
                addition()
            elif i[0] == 11:
                subtracton()
            elif i[0] == 12:
                multiplation()
            else:
                division()
        else:
            a[0] = float(z)
        x = str(a[0])
        entry.delete(0,tk.END)
        entry.insert(0,x)
        l0.configure(text = x)


def Calculationi(i):
    if bool_calculation_error[0]:
        Calculation_error()
    else:
        bool_point[0] = False
        bool_point[1] = False
        if bool_op[1]:
            bool_op[1] = False
            Calculation_special()
        bool_op[1] = True
        Calculation14()
        z = entry.get()
        entry.delete(0,tk.END)
        entry.insert(0,'0')
        if bool_op[0]:
            b[0] = float(z)
            c[0] = float(z)
            if i[0] == 10:
                addition()
            elif i[0] == 11:
                subtracton()
            elif i[0] == 12:
                multiplation()
            else:
                division()
        else:
            bool_op[0] = True
            a[0] = float(z)
        x = str(a[0])
        entry.delete(0,tk.END)
        entry.insert(0,'0')
        l0.configure(text = x)


def Calculation10():
    i[0] = 10
    Calculationi(10)


def Calculation11():
    i[0] = 11
    Calculationi(11)


def Calculation12():
    i[0] = 12
    Calculationi(12)


def Calculation13():
    i[0] = 13
    Calculationi(13)


def Calculation15():
    if bool_calculation_error[0]:
        Calculation_error()
    else:
        bool_point[0] = True
        bool_point[1] = True


def Calculation16():
    if bool_calculation_error[0]:
        Calculation_error()
    else:
        entry.delete(0,tk.END)
        entry.insert(0,'0')
        l0.configure(text = '0')


def Calculation17():
    Delete()
    a[0] = 0
    b[0] = 0
    c[0] = 1
    i[0] = 10
    bool_point[0] = False
    bool_point[0] = False
    bool_op[0] = False
    bool_op[1] = False
    bool_calculation_error[0] = False
    entry.delete(0,tk.END)
    entry.insert(0,'0')
    l0.configure(text = '0')


def Calculation18():
    if bool_calculation_error[0]:
        Calculation_error()
    else:
        z = entry.get()
        display = float(z)
        if bool_op[0]:
            Calculation_error()
            bool_calculation_error[0] = True
        elif display < 0:
            Calculation_error()
            bool_calculation_error[0] = True
        else:
            y = math.sqrt(display)
            x = str(y)
            entry.delete(0,tk.END)
            entry.insert(0,x)
            entry_text = entry.get()
            l0.configure(text = entry_text)


def Calculation19():
    if bool_calculation_error[0]:
        Calculation_error()
    else:
        z = entry.get()
        display = float(z)
        if bool_op[0]:
            Calculation_error()
            bool_calculation_error[0] = True
        else:
            y = display*display
            x = str(y)
            entry.delete(0,tk.END)
            entry.insert(0,x)
            entry_text = entry.get()
            l0.configure(text = entry_text)


b0 = tk.Button(window,text = '0',width = 5,height = 5,command = Calculation0)
b1 = tk.Button(window,text = '1',width = 5,height = 5,command = Calculation1)
b2 = tk.Button(window,text = '2',width = 5,height = 5,command = Calculation2)
b3 = tk.Button(window,text = '3',width = 5,height = 5,command = Calculation3)
b4 = tk.Button(window,text = '4',width = 5,height = 5,command = Calculation4)
b5 = tk.Button(window,text = '5',width = 5,height = 5,command = Calculation5)
b6 = tk.Button(window,text = '6',width = 5,height = 5,command = Calculation6)
b7 = tk.Button(window,text = '7',width = 5,height = 5,command = Calculation7)
b8 = tk.Button(window,text = '8',width = 5,height = 5,command = Calculation8)
b9 = tk.Button(window,text = '9',width = 5,height = 5,command = Calculation9)
b10 = tk.Button(window,text = '+',width = 5,height = 5,command = Calculation10)
b11 = tk.Button(window,text = '-',width = 5,height = 5,command = Calculation11)
b12 = tk.Button(window,text = 'x',width = 5,height = 5,command = Calculation12)
b13 = tk.Button(window,text = '÷',width = 5,height = 5,command = Calculation13)
b14 = tk.Button(window,text = '=',width = 5,height = 5,command = Calculation14)
b15 = tk.Button(window,text = '.',width = 5,height = 5,command = Calculation15)
b16 = tk.Button(window,text = 'C',width = 5,height = 5,command = Calculation16)
b17 = tk.Button(window,text = 'AC',width = 5,height = 5,command = Calculation17)
b18 = tk.Button(window,text = '√x',width = 5,height = 5,command = Calculation18)
b19 = tk.Button(window,text = 'x^2',width = 5,height = 5,command = Calculation19)

b0.grid(row = 4,column = 1)
b1.grid(row = 3,column = 1)
b2.grid(row = 3,column = 2)
b3.grid(row = 3,column = 3)
b4.grid(row = 2,column = 1)
b5.grid(row = 2,column = 2)
b6.grid(row = 2,column = 3)
b7.grid(row = 1,column = 1)
b8.grid(row = 1,column = 2)
b9.grid(row = 1,column = 3)
b10.grid(row = 4,column = 4)
b11.grid(row = 3,column = 4)
b12.grid(row = 2,column = 4)
b13.grid(row = 1,column = 4)
b14.grid(row = 4,column = 3)
b15.grid(row = 4,column = 2)
b16.grid(row = 3,column = 0)
b17.grid(row = 4,column = 0)
b18.grid(row = 1,column = 0)
b19.grid(row = 2,column = 0)
l0.grid(row = 0,column = 0,columnspan = 5)
l1.grid(row = 5,column = 0,columnspan = 5)
entry.grid(row = 6,column = 0,columnspan = 5)



window.mainloop()
