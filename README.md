#Todo list 2 



#my set to do list that doesnt change unless the user wants it to 
todolist = ["Tangled",  "Coco", "Princess and the Frog", "Moana"]

#User input/menu 
#function that displays current to do list to the user 
def display_todo():
    print(todolist)

#Function that is the menu and gives the user optiion for what they want to do to their to do list
def mmenu():
    print("Options for To-Do list:")
    print("1. Add a task to the to-do list \n 2. View the current to-do list \n 3. Mark a task as completed \n 4. Remove a task from the to-do list \n 5. Remove all tasks from to-do list \n 6. Sort the list alphabetically \n 7. Print the number of items on the to-do list \n 8. Exit the program")
    option = input("Option: ")
    if option == "8" :
        print("Goodbye")
        quit()
    if option == "3" :
        marr = input("What item would you like to mark?")
        i = todolist.index(marr)
        todolist[i] = "¤"
        print(todolist)
        mmenu()
    if option == "2":
        display_todo()
        mmenu()
    if option == "1":
        addd = input("Please add a task to the list")
        todolist.append(addd)
        print(todolist)
        mmenu()
    if option == "4":
        remoo = input("What item would you like to remove?")
        todolist.remove(remoo)
        print(todolist)
        mmenu()
    if option == "5":
        todolist.clear()
        print("List cleared")
        mmenu()
    if option == "7":
        print(len(todolist))
        mmenu()
    if option == "6":
        print(sorted(todolist))
        mmenu()




        
#Main
mmenu()
