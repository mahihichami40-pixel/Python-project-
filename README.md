students = {}

while True:
    print("\n1. Add Student")
    print("2. View Students")
    print("3. Search Student")
    print("4. Exit")

    choice = input("Enter choice: ")

    if choice == "1":
        name = input("Enter student name: ")
        marks = input("Enter marks: ")
        students[name] = marks
        print("Student added successfully!")

    elif choice == "2":
        print("\nStudent List:")
        for name, marks in students.items():
            print(f"{name} : {marks}")

    elif choice == "3":
        name = input("Enter student name to search: ")
        if name in students:
            print(f"{name}'s Marks: {students[name]}")
        else:
            print("Student not found!")

    elif choice == "4":
        print("Program Ended.")
        break

    else:
        print("Invalid choice!")