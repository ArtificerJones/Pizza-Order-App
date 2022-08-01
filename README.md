



# this is a Address entry button.

from tkinter import *
#Rename window
root = Tk()
root.title("Pizza Ordering")

#Window size
root.geometry("500x500")

#Name entry field visual settings
name = Entry(root, width = 20)
name.place(x = 150,y = 60)
l1 = Label(root, text = "Name:", font= 15)
l1.place(x = 150, y = 30)

#name button grabs user info from address entry field
def nameBtn():
    res="Name is; " + name.get()
    l1.configure(text = res)
Btn = Button(root, text = "Enter Name", fg="yellow", bg="blue", command = nameBtn)
Btn.place(x = 150, y = 90)



#phone number entry field visual settings
phoneNumber = Entry(root, width = 10)
phoneNumber.place(x=150,y=160)
l2 = Label(root, text = "Phone Number:", font= 15)
l2.place(x=150,y=130)

#Phone button grabs user info from  phone number entry field
def phoneBtn():
    res="Phone Number is; " + phoneNumber.get()
    l2.configure(text = res)
Btn = Button(root, text = "Enter Phone Number", fg="yellow", bg="blue", command = phoneBtn)
Btn.place(x=150,y=190)

#address entry field visual settings
address = Entry(root, width = 20)
address.place(x=150,y=270)
l3 = Label(root, text = "Address:", font= 15)
l3.place(x=150,y=240)

#address button grabs user info from address entry field
def addressBtn():
    res="Address is; " + address.get()
    l3.configure(text = res)
Btn = Button(root, text = "Enter Address", fg="yellow", bg="blue", command = addressBtn)
Btn.place(x=150,y=300)




