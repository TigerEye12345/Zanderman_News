# Zanderman_News
#logo
import time
import turtle
wn = turtle.Screen()
wn.screensize(1000, 1000)
john = turtle.Turtle()
def undo (times, t):
    for i in range (times):
       t.speed(0)
       t.undo()
       t.undo()
john.hideturtle()
# Making the Z
john.speed(0)
john.color("green")
john.begin_fill()
 
john.left(60)
john.forward(100)
john.left(120)
john.forward(100)
 
john.right(90)
john.forward(10)
john.right(90)
john.forward(120)
 
john.right(120)
john.forward(200)
john.left(120)
john.forward(100)
 
john.right(90)
john.forward(10)
john.right(90)
 
john.forward(120)
john.right(120)
john.forward(100)
 
john.end_fill()
 
# Making the circle
 
john.penup()
 
john.left(120)
john.forward(120)
john.left(90)
john.color("red")
john.pendown()
john.circle(140)
for i in range(10):
    john.left(10)
    john.circle(140)



  
undo(42, john)

#drawing triangle


def channel_one():
    john.fillcolor("blue")
    john.begin_fill()
    john.left(120)
    john.forward(100)
    john.left(120)
    john.forward(100)
    john.left(120)
    john.forward(100)
    john.end_fill()
    john.penup()
#getting to center of triangle (pythagorean theoream)
    john.goto(0,1/2*((10000-2500)**0.5))
    john.pendown()
#writing 1
    style=('normal', 20, 'bold')
    john.pencolor('white')
    john.write('1', font=style, align='center')

    john.right(90)
    john.penup()
    john.forward(100)
    john.pencolor('black')
    style=('normal', 30, 'bold')
    john.pendown()
#top, writing to show channel 1
    john.write('Channel', font=style, align='center')
    john.hideturtle()
    wn.bgcolor('lavender')
#timer (john stalls time)
    time.sleep(3)
#undo
    undo(42, john)


def daily_news():
  '''shows the daily news'''
  style=('normal', 20, 'bold')
  john.write('Daily News', font=style, align='center')
  john.hideturtle()
  time.sleep(3)
  undo(3, john)
  john.penup()
  style2=('normal', 20, 'bold')
  story="Today's story is about SpaklyFlower's Avatar maker."
  john.left(90)
  john.forward(100)
  john.write(story, font=style2, align='center')
  wn.bgcolor('lightblue')
  john.hideturtle()
  john.forward(-100)
  style3=('normal', 10, 'bold')
  report = 'This week SparklyFlowers made history by making a AOPS avatar maker. "\n" Look at post 28 on the messing around with turtles thread to see the program.'
  john.write(report, font = style3, align = 'center')
  time.sleep(7)
  undo(43, john)
  john.speed(0)

def weather_report():
  '''does the weather'''
  style=('normal', 30, 'bold')
  john.fillcolor('navy')
  john.goto(0,0)
  john.begin_fill()
  john.forward(-50)
  for i in range(3):
    john.forward(100)
    john.left(120)
  john.end_fill()
  john.forward(50)
  john.penup()
  john.goto(0, 16)
  john.pencolor('white') #We make the second story, channel 2
  john.write('2', font=style, align='center')
  john.left(90)
  john.penup()
  john.forward(100)
  john.write('Channel', font=style, align='center')
  john.hideturtle()
  time.sleep(3)
  undo(20, john)
  john.hideturtle()
  john.penup()
  style3=('normal', 15, 'bold')
  john.home()
  john.left(90)
  john.forward(100)
  john.left(90)
  john.forward(100)
  john.left(90)
  style4=('normal', 10, 'bold')
  john.color('purple')
  john.write("Weather in \n Canada:", font = style4, align = 'center')
  john.forward(90)
  john.write("Thunderstorms\n at noon \n till afternoon, \n partly cloudly in\n the evening", font=style4, align = 'center') #We tell the weather
  john.forward(-90)
  john.left(90)
  john.forward(200)
  john.right(90)
  john.color('black')
  john.write("Weather in central US:", font=style4, align='center')
  john.forward(70)
  john.write("Thunderstorms all \nacross the country,\n stay safe.", font=style4, align='center')
  john.forward(-70)
  john.right(90)
  john.forward(100)
  john.left(90)
  john.forward(200)
  john.write ("It's 6/23/20 and...", font=style3, align = 'center') #Tell the date
  john.forward(50)
  john.write("That's it folks!", font=style3, align = 'center')#We end with a that's it folks!
  time.sleep(8)
  undo(19,john)
  john.hideturtle()
  john.speed(0)

def tiger_jokes():
  '''tiger jokes'''
  john.penup()
  john.goto(0, 16)
  john.pendown()
  john.pencolor('white') #We make the third story, channel 3
  john.write('3', font=style, align='center')#make john write the 3
  undo(8, john)
  john.home()
  john.left(90)
  john.forward(100)
  john.write('Jokes with TigerEye', font=style, align='underline')#make john write tiger watch with tigereye
  john.home()
  john.right(90)
  style5 = ('normal', 20, 'bold')
  style6 = ('normal', 10, 'bold')
  john.write("My boss asked me why I don't like coding in python", font = style5,align='center')
  john.forward(100)
  john.write("I just find it too constricting.", font = style5, align='center')

channel = input("What channel do you want to watch? Please input 1, 2, or 3. If you'd like a full replay, please input anything else")
if channel==1:
  channel_one()
  daily_news()
elif channel == 2:
  weather_report()
elif channel == 3:
  tiger_jokes()
else:
  channel_one()
  daily_news()
  weather_report()


# Credits
style=('normal', 20, 'underline')
john.home()
john.color('black')
john.write("Credits", font = style, align = 'center')#And here are the credits
john.left(90)
john.forward(100)
style7=('normal', 20, 'bold')
wn.bgcolor('lightgreen')
john.write("ZANDERMAN NEWS",font = style7, align = 'center')
john.right(180)
john.forward(150)
john.write("SparklyFlowers",font = style7, align = 'center')#SparklyFlowers
john.forward(50)
john.write('TigerEye123', font = style7, align = 'center')#TigerEye123
john.forward(50)
john.write("Zanderman", font = style7, align = 'center')#And Zanderman

wn.mainloop()