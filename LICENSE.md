import turtle

# Configuración de la pantalla
screen = turtle.Screen()
screen.bgcolor("lightblue")

# Crear la tortuga
t = turtle.Turtle()
t.speed(10)

# Dibujar un pétalo
def draw_petal():
    t.circle(60, 60)
    t.left(120)
    t.circle(60, 60)
    t.left(120)

# Dibujar los pétalos de la flor
t.color("white")
t.begin_fill()

for _ in range(6):  # 6 pétalos
    draw_petal()
    t.right(60)

t.end_fill()

# Dibujar el centro de la flor
t.penup()
t.goto(0, -30)  # Mover hacia el centro de la flor
t.pendown()
t.color("yellow")
t.begin_fill()
t.circle(30)  # Círculo del centro de la flor
t.end_fill()

# Ocultar la tortuga
t.hideturtle()

# Finalizar
turtle.done()
