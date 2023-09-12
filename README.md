from os import name
import pathlib
from tkinter import *
import tkinter
from tkinter.ttk import Combobox
from tkinter import messagebox
import pathlib
import tkinter as tk
from PIL import Image , ImageTk
import webbrowser
root = Tk()


def clear():
    nameValue.set('')
    contactValue.set('')
    AgeValue.set('')
    SkillsEntry.delete(1.0, END)
    EmilValue.set('')
    EducationalBackgroundValue.set('')
    WorkExperienceValue.set('')
    NationalityValue.set('')
    SecondNameValue.set('')
    passwordValue.set('')
    UsernameValue.set('')
    QualificationsValue.set('')
    ConfirmpasswordValue.set('')

# Labels


Label(root, text="please fill out this form :", font="arial 20",
      bg="#326273", fg="#fff").place(x=20, y=20)
Label(root, text="First Name :", font=23,
      bg="#326273", fg="#fff").place(x=50, y=100)
Label(root, text="Last Name :", font=23,
      bg="#326273", fg="#fff").place(x=50, y=150)
Label(root, text="Age :", font=23, bg="#326273", fg="#fff").place(x=50, y=200)
Label(root, text="Geder :", font=23, bg="#326273", fg="#fff").place(x=370, y=200)
Label(root, text="Skills :", font=23,
      bg="#326273", fg="#fff").place(x=50, y=250)
Label(root, text="Gmail :", font=23,
      bg="#326273", fg="#fff").place(x=50, y=350)
Label(root, text="Education :", font=23,
      bg="#326273", fg="#fff").place(x=50, y=400)
Label(root, text="Work Experience:", font=23,
      bg="#326273", fg="#fff").place(x=50, y=450)
Label(root, text="Nationality :", font=23,
      bg="#326273", fg="#fff").place(x=50, y=500)
Label(root, text="Username :", font=23,
      bg="#326273", fg="#fff").place(x=650, y=100)
Label(root, text="password :", font=23,
      bg="#326273", fg="#fff").place(x=650, y=150)
Label(root, text="Confirm password :", font=23,
      bg="#326273", fg="#fff").place(x=650, y=200)
Label(root, text="Qualifications :", font=23,
      bg="#326273", fg="#fff").place(x=650, y=250)
Label(root, text="Languages :", font=23,
      bg="#326273", fg="#fff").place(x=650, y=300)
Label(root, text="Location :", font=23,
      bg="#326273", fg="#fff").place(x=650, y=350)
Label(root, text="Other :", font=23,
      bg="#326273", fg="#fff").place(x=1040, y=250)

# values

nameValue = StringVar()
contactValue = StringVar()
AgeValue = StringVar()
EmilValue = StringVar()
EducationalBackgroundValue = StringVar()
WorkExperienceValue = StringVar()
NationalityValue = StringVar()
SecondNameValue = StringVar()
UsernameValue = StringVar()
passwordValue = StringVar()
QualificationsValue = StringVar()
ConfirmpasswordValue = StringVar()
LocationValue = StringVar()

# Entry

nameEntry = Entry(root, textvariable=nameValue, width=45, bd=2, font=20)
contactEntry = Entry(root, textvariable=contactValue, width=45, bd=2, font=20)
ageEntry = Entry(root, textvariable=AgeValue, width=15, bd=2, font=20)
EmilEntry = Entry(root, textvariable=EmilValue, width=30, bd=2, font=20)
EducationalBackground = Entry(
    root, textvariable=EducationalBackgroundValue, width=45, bd=2, font=20)
WorkExperience = Entry(root, textvariable=WorkExperienceValue,
                       width=45, bd=2, font=20)
Nationality = Entry(root, textvariable=NationalityValue,
                    width=45, bd=2, font=20)
SecondName = Entry(root, textvariable=SecondNameValue,
                   width=45, bd=2, font=20)
Username = Entry(root, textvariable=UsernameValue,
                 width=45, bd=2, font=20)
password = Entry(root, textvariable=passwordValue,
                 width=45, bd=2, font=20)
Qualifications = Entry(root, textvariable=QualificationsValue,
                       width=18, bd=2, font=20)
Confirmpassword = Entry(root, textvariable=ConfirmpasswordValue,
                        width=45, bd=2, font=20)
Location = Entry(root, textvariable=LocationValue,
                 width=45, bd=2, font=20)

# combobox

gender_combbox = Combobox(
    root, values=['Male', 'Female'], font='arial 14', state='r', width=14)
gender_combbox.place(x=440, y=200)
gender_combbox.set('Male')


gender_combbox = Combobox(
    root, values=['university', 'Ph.D', 'M.A', 'BSC', 'Other'], font='arial 14', state='r', width=25)
gender_combbox.place(x=800, y=250)
gender_combbox.set('university')


gender_combbox = Combobox(
    root, values=['Al-Asimah', 'Al-Ahmadi', 'Al-Farwaniyah', 'Al-Jahra', 'Mubarak Al-Kabeer', 'Hawally', 'Other'], font='arial 14', state='r', width=35)
gender_combbox.place(x=800, y=350)
gender_combbox.set('Al-Asimah')


SkillsEntry = Text(root, width=50, height=4, bd=4)

nameEntry.place(x=200, y=100)
contactEntry.place(x=200, y=150)
ageEntry.place(x=200, y=200)
SkillsEntry.place(x=200, y=250)
EmilEntry.place(x=200, y=350)
EducationalBackground.place(x=200, y=400)
WorkExperience.place(x=200, y=450)
Nationality.place(x=200, y=500)
SecondName.place(x=800, y=95)
Username.place(x=800, y=150)
password.place(x=800, y=200)
Qualifications.place(x=1110, y=248)
Confirmpassword.place(x=800, y=300)
# Location.place(x=800, y=350)


def new_window():
    top = Toplevel()
    top.title("FORSATAK")
    top.geometry("1300x3400")

    #Load and display the image
    image = Image.open("done.png")  # Replace with the path to your image
    photo = ImageTk.PhotoImage(image)
    image_label = Label(top, image=photo)
    image_label.image = photo  # Store a reference to the image to prevent it from being garbage collected
    image_label.pack(pady=20)
    lab = Label(top, text="Thank you! You will be answered shortly via your email")
    lab.pack() 




def open_local_website():
    url = "file:///path/to/your/local/website/indexcopy.html"  # Replace with your local website's file path
    webbrowser.open(url)

app = tk.Tk()
app.title("Local Website Opener")

button = tk.Button(app, text="Open Local Website", command=open_local_website)
button.pack(pady=20)


# Button(text="click", command=new_window).pack()
# Buttons

Button(root, text="submit", bg='#326273', fg="#326273",
       width=15, height=2, command=new_window).place(x=200, y=550)

Button(root, text="Clear", bg='#326273', fg="#326273",
       width=15, height=2, command=clear).place(x=340, y=550)

Button(root, text="Exit", bg='#326273', fg="#326273",
       width=15, height=2, command=lambda: root.destroy()).place(x=480, y=550)

# root.geometry("400*300")
root.geometry("10000x3700")
root.title("FORSATAK")
root.mainloop()
app.mainloop()

