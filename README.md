# CS_class
Rocket and Home (turtle)
##### House 3d #####
import turtle
import math

screen = turtle.Screen()
screen.bgcolor("orange")

mordi = turtle.Turtle()
mordi.color("black")
mordi.shape("turtle")
mordi.speed(5)

def base(q, width, height, color):
    q.fillcolor(color)
    q.begin_fill()
    q.forward(width)
    q.left(90)
    q.forward(height)
    q.left(90)
    q.forward(width)
    q.left(90)
    q.forward(height)
    q.left(90)
    q.end_fill()


def roof(q, length, color):
    q.fillcolor(color)
    q.begin_fill()
    q.forward(length)
    q.left(135)
    q.forward(length / math.sqrt(2))
    q.left(90)
    q.forward(length / math.sqrt(2))
    q.left(135)
    q.end_fill()


def threedimensional(q, width, height, color):
    q.fillcolor(color)
    q.begin_fill()
    q.left(30)
    q.forward(width)
    q.left(60)
    q.forward(height)
    q.left(120)
    q.forward(width)
    q.left(60)
    q.forward(height)
    q.left(90)
    q.end_fill()


def foursticks(q, length, radius):
    for i in range(4):
        q.penup()
        q.forward(radius)
        q.pendown()
        q.forward(length)
        q.penup()
        q.backward(length + radius)
        q.left(90)


mordi.penup()
mordi.goto(-150, -120)
mordi.pendown()
base(mordi, 100, 110, "blue")


mordi.penup()
mordi.goto(-120, -120)
mordi.pendown()
base(mordi, 40, 60, "lightgreen")

#front facing roof

mordi.penup()
mordi.goto(-150, -10)
mordi.pendown()
roof(mordi, 100, "magenta")

#sides

mordi.penup()
mordi.goto(-50, -120)
mordi.pendown()
threedimensional(mordi, 60, 110, "yellow")

#windows 

mordi.penup()
mordi.goto(-30, -60)
mordi.pendown()
threedimensional(mordi, 20, 30, "brown")

#side of roof

mordi.penup()
mordi.goto(-50, -10)
mordi.pendown()
mordi.fillcolor("skyblue")
mordi.begin_fill()
mordi.left(30)
mordi.forward(60)
mordi.left(105)
mordi.forward(100 / math.sqrt(2))
mordi.left(75)
mordi.forward(60)
mordi.left(105)
mordi.forward(100 / math.sqrt(2))
mordi.left(45)
mordi.end_fill()

# bottom of my tree

mordi.penup()
mordi.goto(100, -130)
mordi.pendown()
base(mordi, 20, 40, "brown")

# top of tree

mordi.penup()
mordi.goto(65, -90)
mordi.pendown()
roof(mordi, 90, "lightgreen")
mordi.penup()
mordi.goto(70, -45)
mordi.pendown()
roof(mordi, 80, "lightgreen")
mordi.penup()
mordi.goto(75, -5)
mordi.pendown()
roof(mordi, 70, "lightgreen")

# Sun

mordi.penup()
mordi.goto(55, 110)
mordi.fillcolor("red")
mordi.pendown()
mordi.begin_fill()
mordi.circle(24)
mordi.end_fill()

#beams

mordi.penup()
mordi.goto(55, 134)
mordi.pendown()
foursticks(mordi, 25, 24)
mordi.right(45)
foursticks(mordi, 15, 24)
mordi.left(45)


mordi.penup()
mordi.goto(-100, -150)
mordi.left(90)
