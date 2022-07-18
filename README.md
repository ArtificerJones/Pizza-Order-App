# Pizza-Order-App
#This is a repository for my final Project Sdev140 in python. I need a GUI to order a Pizza Pie. 2 windows and buttons.
from tkinter import *
#Rename window
root = Tk()
root.title("Tempurature conversion")

# entry box , Not sure how to make sure user enters a float.
e = Entry(root, width = 30)
e.pack()

# convert to Celsius 
def Celsius():

    # If it's a number entered
    try:
        # convert to float
        temp = float(e.get())
        # convert to Celcius formula
        convert = ((temp-32)*(5/9))
        # convert to srting and round to 2 decimal places
        answer = str(round(convert,2))
        
    # Error is not number    
    except ValueError:
        myLabel = Label(root, text ='Non-Number error, Please enter a number')
        myLabel.pack()
        
    # If good gives the temp converted 
    else:
        # prints the answer as a label
        myLabel = Label(root, text = "The tempurature in Celsius is: " + answer)
        myLabel.pack()
    
        
# runs celsius command once button pushed
myButton = Button(root, text = " Convert to Celsius", command = Celsius)
myButton.pack()


# convert to Fahrenheit
def Fahrenheit():

    # if a number was entered
    try:
        # convert to float
        temp = float(e.get())
        # convert to Fahrenheit formula
        convert = ((temp*(9/5)+32))
        # convert to srting and round to 2 decimal places
        answer = str(round(convert,2))
        
    # Error is not number    
    except ValueError:
        myLabel = Label(root, text ='Non-Number error, Please enter a number')
        myLabel.pack()

    # If good gives converted temperature
    else:
        # prints the answer as a label
        myLabel = Label(root, text = "The tempurature in Fahrenheit is: " + answer)
        myLabel.pack()

# runs celsius command once button pushed
myButton = Button(root, text = " Convert to Feirenhieght", command = Fahrenheit)
myButton.pack()
