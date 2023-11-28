from tkinter import *
import settings
import utils
from cell import Cell

root = Tk()
root.configure(bg="black")
root.geometry(f'{settings.Width}x{settings.Height}')
root.title("Minesweeper")
root.resizable(False, False)

top_frame = Frame(
    root,
    bg='black',
    width=settings.Width,
    height=utils.height_percentage(25)
)
top_frame.place(x=0, y=0)

left_frame = Frame(
    root,
    bg='black',
    width=utils.width_percentage(25),
    height=utils.height_percentage(75)
)
left_frame.place(x=0, y=180)

center_frame = Frame(
    root,
    bg='black',
    width=utils.width_percentage(75),
    height=utils.height_percentage(75),
)
center_frame.place(
    x=utils.width_percentage(25),
    y=utils.height_percentage(25)
)

for x in range(settings.Grid_Size):
    for y in range(settings.Grid_Size):
        c = Cell(x, y)
        c.create_btn_object(center_frame)
        c.cell_btn_object.grid(
            column=x, row=y
        )

Cell.randomize_mines()

root.mainloop()
