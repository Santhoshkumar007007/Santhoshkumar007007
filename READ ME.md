import tkinter as tk
from tkinter import messagebox
#from tkinter.ttk import *
index=['O','X']

matrix=[['r1','r2','r3'],
        ['r4','r5','r6'],
        ['r7','r8','r9']]


epty=[]
def reset():
    r1['text'],r1['bg']=' ','gray'
    r2['text'],r2['bg']=' ','gray'
    r3['text'],r3['bg']=' ','gray'
    r4['text'],r4['bg']=' ','gray'
    r5['text'],r5['bg']=' ','gray'
    r6['text'],r6['bg']=' ','gray'
    r7['text'],r7['bg']=' ','gray'
    r8['text'],r8['bg']=' ','gray'
    r9['text'],r9['bg']=' ','gray'
    global matrix
    matrix=[['','','',],['','',''],['','','']]
    global epty
    epty=[]



def check():
    length = len(epty)
    if matrix[0][0]=='X'and matrix[0][1]=='X' and matrix[0][2]=='X':
        r1['bg'] = 'green'
        r2['bg'] = 'green'
        r3['bg'] = 'green'
        messagebox.showinfo('RESULT', 'X wins  restart the game')


    elif matrix[1][0]=='X'and matrix[1][1]=='X' and matrix[1][2]=='X':
        r4['bg'] = 'green'
        r5['bg'] = 'green'
        r6['bg'] = 'green'
        messagebox.showinfo('RESULT', 'X wins')

    elif matrix[2][0]=='X'and matrix[2][1]=='X' and matrix[2][2]=='X':
        r7['bg'] = 'green'
        r8['bg'] = 'green'
        r9['bg'] = 'green'
        messagebox.showinfo('RESULT', 'X wins')
        #
    elif matrix[0][0]=='X'and matrix[1][0]=='X' and matrix[2][0]=='X':
        r1['bg'] = 'green'
        r4['bg'] = 'green'
        r7['bg'] = 'green'
        messagebox.showinfo('RESULT', 'X wins')
    elif matrix[0][1]=='X'and matrix[1][1]=='X' and matrix[2][1]=='X':
        r2['bg'] = 'green'
        r5['bg'] = 'green'
        r8['bg'] = 'green'
        messagebox.showinfo('RESULT', 'X wins')
    elif matrix[0][2]=='X'and matrix[1][2]=='X' and matrix[2][2]=='X':
        r3['bg'] = 'green'
        r6['bg'] = 'green'
        r9['bg'] = 'green'
        messagebox.showinfo('RESULT', 'X wins')
        #
    elif matrix[0][2]=='X'and matrix[1][1]=='X' and matrix[2][0]=='X':
        r3['bg'] = 'green'
        r5['bg'] = 'green'
        r7['bg'] = 'green'
        messagebox.showinfo('RESULT', 'X wins')
    elif matrix[0][0]=='X'and matrix[1][1]=='X' and matrix[2][2]=='X':
        r1['bg'] = 'green'
        r5['bg'] = 'green'
        r9['bg'] = 'green'
        messagebox.showinfo('RESULT', 'X wins')

    #=============
    elif matrix[0][0]=='O'and matrix[0][1]=='O' and matrix[0][2]=='O':
        r1['bg'] = 'green'
        r2['bg'] = 'green'
        r3['bg'] = 'green'
        messagebox.showinfo('RESULT','o wins')
    elif matrix[1][0]=='O'and matrix[1][1]=='O' and matrix[1][2]=='O':
        r4['bg'] = 'green'
        r5['bg'] = 'green'
        r6['bg'] = 'green'
        messagebox.showinfo('RESULT', 'o wins')
    elif matrix[2][0]=='O'and matrix[2][1]=='O' and matrix[2][2]=='O':
        r7['bg'] = 'green'
        r8['bg'] = 'green'
        r9['bg'] = 'green'
        messagebox.showinfo('RESULT', 'o wins')
        #
    elif matrix[0][0]=='O'and matrix[1][0]=='O' and matrix[2][0]=='O':
        r1['bg'] = 'green'
        r4['bg'] = 'green'
        r7['bg'] = 'green'
        messagebox.showinfo('RESULT', 'o wins')
    elif matrix[0][1]=='O'and matrix[1][1]=='O' and matrix[2][1]=='O':
        r2['bg'] = 'green'
        r5['bg'] = 'green'
        r8['bg'] = 'green'
        messagebox.showinfo('RESULT', 'o wins')
    elif matrix[0][2]=='O'and matrix[1][2]=='O' and matrix[2][2]=='O':
        r3['bg'] = 'green'
        r6['bg'] = 'green'
        r9['bg'] = 'green'
        messagebox.showinfo('RESULT', 'o wins')
        #
    elif matrix[0][2]=='O'and matrix[1][1]=='O' and matrix[2][0]=='O':
        r3['bg'] = 'green'
        r5['bg'] = 'green'
        r7['bg'] = 'green'
        messagebox.showinfo('RESULT', 'o wins')
    elif matrix[0][0]=='O'and matrix[1][1]=='O' and matrix[2][2]=='O':
        r1['bg'] = 'green'
        r5['bg'] = 'green'
        r9['bg'] = 'green'
        messagebox.showinfo('RESULT', 'o wins')

    elif length==9:
        r1['bg'] = 'orange'
        r2['bg'] = 'orange'
        r3['bg'] = 'orange'
        r4['bg'] = 'orange'
        r5['bg'] = 'orange'
        r6['bg'] = 'orange'
        r7['bg'] = 'orange'
        r8['bg'] = 'orange'
        r9['bg'] = 'orange'
        messagebox.showwarning('RESULT', '      Draw        ')


    #---------------
def check_draw():
    pass

def a():
    if r1['text'] == ' ':
        r1['text'] = index[-1]
        matrix[0][0]=index[-1]
        index.reverse()
        epty.append(1)
        check()


def b():
    if r2['text'] == ' ':
        r2['text'] = index[-1]
        matrix[0][1] = index[-1]
        index.reverse()
        epty.append(1)
        check()


def c():
    if r3['text'] == ' ':
        r3['text'] = index[-1]
        matrix[0][2]=index[-1]
        index.reverse()
        epty.append(1)
        check()



def d():
    if r4['text'] == ' ':
        r4['text'] = index[-1]
        matrix[1][0]=index[-1]
        index.reverse()
        epty.append(1)
        check()



def e():
    if r5['text'] == ' ':
        r5['text'] =index[-1]
        matrix[1][1]=index[-1]
        index.reverse()
        epty.append(1)
        check()



def f():
    if r6['text'] == ' ':
        r6['text'] = index[-1]
        matrix[1][2]=index[-1]
        index.reverse()
        epty.append(1)
        check()



def g():
    if r7['text'] == ' ':
        r7['text'] = index[-1]
        matrix[2][0]=index[-1]
        index.reverse()
        epty.append(1)
        check()
        check_draw()


def h():
    if r8['text'] == ' ':
        r8['text'] = index[-1]
        matrix[2][1]=index[-1]
        index.reverse()
        epty.append(1)
        check()



def i():
    if r9['text'] == ' ':
        r9['text'] = index[-1]
        matrix[2][2] = index[-1]
        index.reverse()
        epty.append(1)
        check()



def close():
    root.destroy()


root = tk.Tk()
root.title('Tic Tac Toe')
root.geometry('420x260')
root.resizable(False,False)
root.configure(bg='yellow')
window=tk.Frame(root)
window.pack()
#turn=tk.Label(root,text='IF THE GAME WAS DRAW \n RESET THE GAME',bg='yellow').place(x=265,y=165)
reset_button=tk.Button(root,text='RESET',bg='pink',height=2,width=8,command=reset)
exit_button=tk.Button(root,text='EXIT',bg='red',height=2,width=8,command=close)
r1=tk.Button(root,text=' ',width=10,bg='gray',height=5,command=a)
r2=tk.Button(root,text=' ',width=10,bg='gray',height=5,command=b)
r3=tk.Button(root,text=' ',width=10,bg='gray',height=5,command=c)
#
r4=tk.Button(root,text=' ',width=10,bg='gray',height=5,command=d)
r5=tk.Button(root,text=' ',width=10,bg='gray',height=5,command=e)
r6=tk.Button(root,text=' ',width=10,bg='gray',height=5,command=f)
#
r7=tk.Button(root,text=' ',width=10,bg='gray',height=5,command=g)
r8=tk.Button(root,text=' ',width=10,bg='gray',height=5,command=h)
r9=tk.Button(root,text=' ',width=10,bg='gray',height=5,command=i)

r1.place(x=5,y=5)
r2.place(x=85,y=5)
r3.place(x=165,y=5)

r4.place(x=5,y=85)
r5.place(x=85,y=85)
r6.place(x=165,y=85)

r7.place(x=5,y=165)
r8.place(x=85,y=165)
r9.place(x=165,y=165)
exit_button.place(x=305,y=85)
reset_button.place(x=305,y=5)

root.mainloop()




