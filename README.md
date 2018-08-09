# gui_buttons
Toggle buttons for input.

    import tkinter as tk

    class App(tk.Frame):
        def __init__(self, master=None):
            master.minsize(width=200, height=200)
            super().__init__(master)
            self.pack()
            self.create_widgets()

    def create_widgets(self):
        self.hi_there = tk.Button(self)
        self.hi_there = tk.Button(width=30, height=10, font=20, fg = "yellow", bg = "green")
        self.hi_there["text"] = "Toggle\n\n(click here)"
        self.hi_there["command"] = self.say_hi
        self.hi_there.pack(side="top")

        self.quit = tk.Button(self, text="QUIT", fg="white", bg = "red", \
                              width=10, height=5, command=root.destroy)
        self.quit.pack(side="bottom")

    def say_hi(self):
        print("Input Received")


    root = tk.Tk()
    root.title("Input Application")
    app = App(master=root)
    root.resizable(width=False, height=False)
    app.mainloop()
