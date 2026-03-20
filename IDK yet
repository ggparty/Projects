import turtle, random
def setup():
    turtle.penup()
    turtle.goto(0,-335)
    turtle.pendown()
    turtle.goto(0,335)
    turtle.penup()
    turtle.goto(-350,0)
    turtle.pendown()
    turtle.goto(350,0)
    
def triangle(length,colors):
    color(colors)
    turtle.begin_fill()
    for i in range(3):
        turtle.forward(length)
        turtle.left(120)
    turtle.end_fill()

def square (width, height, colors):
    color(colors)
    turtle.begin_fill()
    for i in range(2):
        turtle.forward(width)
        turtle.right(90)
        turtle.forward(height)
        turtle.right(90)
    turtle.end_fill()

def circle(r, colors):
    color(colors)
    turtle.begin_fill()
    turtle.circle(r)
    turtle.end_fill()

def octagon(length, colors):
    color(colors)
    turtle.begin_fill()
    for i in range(8):
        turtle.forward(length)
        turtle.left(45)
    turtle.end_fill()

def set_color(colors):
    if colors == 1:
        turtle.pencolor('red')
        turtle.fillcolor('red')
    elif colors == 2:
        turtle.pencolor('blue')
        turtle.fillcolor('blue')
    elif colors == 3:
        turtle.pencolor('green')
        turtle.fillcolor('green')
    else:
        turtle.pencolor('black')
        turtle.fillcolor('black')

def coordinates(choice):
    if choice == 1:
        x = random.randrange(-300,-50)
        y = random.randrange(50,300)
    elif choice == 2:
        x = random.randrange(50,300)
        y = random.randrange(50,300)
    elif choice == 3:
        x = random.randrange(-300,-50)
        y = random.randrange(-300,-250)
    else:
        x = random.randrange(50,300)
        y = random.randrange(-300,-50)
    return x, y


def decideShape(shape,colors):
    if shape == 1 or shape == 4:
        length = random.randrange(25,70)
        if shape == 1:
            triangle(length,colors)
        else:
            octagon(length,colors)
    elif shape == 2:
        height = random.randrange(25,70)
        width = random.randrange(25,70)
        square(width, height, colors)
    elif shape == 3:
        r = random.randrange(25,70)
        circle(r, colors)

            

def main():
    setup()
    while True:
        info = """Choose a shape:
1: Circle
2: Square
3: Triangle
4: Octagon"""
        print(info)
        shape = int(input("Enter choice (1-4): "))
        print()
        info = """Choose a color:
1: Red
2: Blue
3: Green
4: Black"""
        print(info)
        colors = int(input("Enter choice (1-4): "))
        print()
        times = int(input("Enter number of times to draw the shape (1-5): "))
        print()
        info = """Select a quadrant for placement:
1: Top-Right
2: Top-Left
3: Bottom-Left
4: Bottom-Right"""
        print(info)
        choice = int(input("Enter choice (1-4): "))
        print()
        for i in range(times):
            x,y = coordinates(choice)
            turtle.penup()
            turtle.goto(x,y)
            turtle.pendown()
            decideShape(shape,colors)
        stay = input("Draw another shape? (y/n): ")
        if stay == "n":
            break
        turtle.done()
    turtle.hideturtle()
main()


