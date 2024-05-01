# basic-gui
import tkinter as tk

def say_hello():
    label.config(text="Hello, World!")

root = tk.Tk()
label = tk.Label(root, text="Welcome to Tkinter!")
button = tk.Button(root, text="Say Hello", command=say_hello)

label.pack()
button.pack()

root.mainloop()
import PySimpleGUI as sg

layout = [
    [sg.Image(filename="path/to/your/image.png")],
    [sg.Button("Exit")]
]

window = sg.Window("Image Viewer", layout)

while True:
    event, values = window.read()
    if event == sg.WINDOW_CLOSED or event == "Exit":
        break

window.close()
