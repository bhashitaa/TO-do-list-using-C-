# To-do-list-using-Cpp
ToDo List is a kind of app that generally used to maintain our day-to-day tasks or list everything that we have to do, with the most important tasks at the top of the list, and the least important tasks at the bottom. It is helpful in planning our daily schedules. We can add more tasks at any time and delete a task that is completed. 


#Features:

In this version of the ToDo list, the user will be getting four options:

Create (add) a new task or adding a new ToDo in the ToDo List App.
See all the tasks or View all the ToDos that were added to the app.
Delete any ToDo from the list of ToDos.
Exit from the app.
Approach:

This program involves the basic concepts like variables, data types, structure, string, loop, inserting a node into the linked list at any position, deleting a node from the linked list at any position, linked list traversal, etc. The approach followed for constructing the ToDo application is as follows:

The splash screen will display the name of the application and the developer: This is done using some statements inside the printf() function (the predefined function used to print the (“character, string, float, integer, octal and hexadecimal values”) and some predefined-functions.
The second screen will present the user with a list of four options i.e. Add, Delete, View, and Exit: This is achieved using Switch-cases.
Depending upon the user selects a corresponding function screen will be displayed: Functions for each task are created. Since C Language is a function or procedure based language, so we should make functions for specific jobs.
All the ToDos will be written inside the data part of the node of the Linked List. The linked list should be declared globally so that data (our ToDos) will not get lost if a function’s execution is over. And by declaring it globally all functions can use the same data that is inside the linked list.
Below are the functionality of the above program:

The Splash screen: This consists of the name of the application and the developer. The code is written inside a function named interface():
interface() function contains some printf statements and a predefined function called system().
The system() function is a part of the C/C++ standard library. It is used to pass the commands that can be executed in the command processor or the terminal of the operating system and finally returns the command after it has been completed.
system(“Color 4F”) will change the color of the console i.e. background (4) and the text on the console i.e. foreground (F).
system(“pause”) will pause the screen so the user will get a message: Press any key to continue . . .
Splash screen

main() function: Use a simple switch case inside an infinite while-loop so that users will get to make choices every time and provide choices with the help of the printf() function and taking user’s input using the scanf() function. According to the input, the specific case will be executed and the required function will be called.
Linked List: Linked list named Todo is made using the structure concept of C and using the typedef we are renaming it to Todo. This Linked list consists of three parts –
The data part is made as an array of characters i.e., char buffer[101]. The ToDos can be large so declaring the size of the array as 101.
The node part contains the address of the next node i.e. *next.
An integer types variable (int count) that will take account of the number of nodes and will help in the numbering of ToDos in further defined functions.
As in a singly linked list, a start pointer (In this case- todo *start) is used to get the address of the first node, it is declared and kept NULL inside it (Initially pointing to NULL).
seetodo() function: Four concepts are coded in this function. These are as follows:
system(“cls”): to clear the screen or the console. It can be avoided if anyone wants to see all the previous operations or inputs done by the user.
Creating an object of the structure variable i.e. *temp to access the linked list structure. This temp variable will point to start initially. We can output Empty ToDo if the start is equal to NULL. This means that our list is empty.
Using a simple linked list traversal concept i.e., print the data part, node by node until the last node we can print all the ToDos. The while loop will execute till the last node, printf() inside it will print the numbering of ToDos, and puts() function will print the data which is in the form of a string of characters. fflush() is a predefined function, its purpose is to clear (or flush) the output buffer and move the buffered data to the console.
Finally using the system(“pause”) to pause the screen until the user presses any key.
createtodo() function: It contains a switch-case to ask the user if he/she wants to add ToDo or not using a character variable (char c;). Using printf() for asking the user about another input and scanf() to input the choice of the user.
Now using the concept of adding a node at the end of the linked list the nodes are added. Here two cases can be possible –
If there is no node present, in this case, the start will point to NULL.
If there are some nodes present, in that case, the start will point to the first node and use a pointer-to-node ( *add) to traverse till the last node (which contains NULL in the pointer part). Here, dynamic memory allocation (using calloc() is used, this is a predefined function to allocate memory dynamically) to allocate memory at run time.
In insertion, a new node is made, the data is taken from the user using gets() (a predefined function used to take input of characters), pointer part is made NULL as we are adding at the end and the newly created node is made to point by the previous node present in the linked list by using traversal concept explained above.

adjustcount() function: This function will take account of the numbering of the nodes of the linked list. Using the traversal concept and the help of start pointer it will update the value of the count of each node at every call.
deletetodo() function: Using the concept of deleting a node, we are deleting ToDos. We are asking the user the node that he/she wants to delete (by asking the numbering of the node). If the start is NULL then we cannot delete anything, so we can print: There is no TODO for today.

Output:

 

Splash Screen:

![image](https://user-images.githubusercontent.com/88206232/178161960-69128394-e9b8-4384-8edd-65479bdfea22.png)


List of Available Functions

![image](https://user-images.githubusercontent.com/88206232/178161968-9fc6ce9b-6e51-415c-87a5-428cb0271c5f.png)



User Presses 2
Create a New TODO

![image](https://user-images.githubusercontent.com/88206232/178161972-cdb7c289-73c6-4ec7-a0c1-a3500049ff3a.png)


User Presses 1
See TODO list

![image](https://user-images.githubusercontent.com/88206232/178161977-4d6d2359-f7c9-4826-a2c2-b1fd17ae781b.png)


Displaying ToDos

![image](https://user-images.githubusercontent.com/88206232/178161982-888f74b9-44c4-48a3-9f05-d78b97485643.png)

Deleting a ToDo


![image](https://user-images.githubusercontent.com/88206232/178161986-d0a519e7-94bb-41c8-9bf4-3bb4b6101a23.png)

Displaying ToDos after Deleting a ToDo
Changed TODO list

![image](https://user-images.githubusercontent.com/88206232/178161993-6f8e13b2-5c17-45da-b23e-2b4b1d4ba8ca.png)

User Presses 4

![image](https://user-images.githubusercontent.com/88206232/178161999-5773f815-9cec-491a-aeef-5f579b976133.png)

Exit Screen

 





