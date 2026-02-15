# Priority Queue ADT using List

priority_queue = []

def insert():
    element = input("Enter element: ")
    priority = int(input("Enter priority (lower number = higher priority): "))
    priority_queue.append((priority, element))
    priority_queue.sort()
    print("Element inserted successfully.")

def delete():
    if len(priority_queue) == 0:
        print("Priority Queue is empty.")
    else:
        item = priority_queue.pop(0)
        print("Deleted element is:", item[1])

def display():
    if len(priority_queue) == 0:
        print("Priority Queue is empty.")
    else:
        print("Priority Queue elements are:")
        for item in priority_queue:
            print("Element:", item[1], " Priority:", item[0])

while True:
    print("\n--- Priority Queue ADT ---")
    print("1. Insert")
    print("2. Delete")
    print("3. Display")
    print("4. Exit")

    choice = int(input("Enter your choice: "))

    if choice == 1:
        insert()
    elif choice == 2:
        delete()
    elif choice == 3:
        display()
    elif choice == 4:
        print("Exiting program.")
        break
    else:
        print("Invalid choice.")# Data-structure-4
        --- Priority Queue ADT ---
1. Insert
2. Delete
3. Display
4. Exit
Enter your choice: 1
Enter element: A
Enter priority (lower number = higher priority): 2
Element inserted successfully.

Enter your choice: 1
Enter element: B
Enter priority (lower number = higher priority): 1
Element inserted successfully.

Enter your choice: 3
Priority Queue elements are:
Element: B  Priority: 1
Element: A  Priority: 2

Enter your choice: 2
Deleted element is: B
