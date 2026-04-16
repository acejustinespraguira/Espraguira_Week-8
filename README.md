messages = []

while True:
    print("\nWelcome to the messaging App!\n")
    print("1. Send Message")
    print("2. View Messages")
    print("3. Exit")

    choice = input("Enter Your Choice: ")

    if choice == "1":
        message = input("Enter your message: ")
        if message.strip() == "":
            print("Message cannot be empty")
        else:
            messages.append(message)
            print("Message sent!")

    elif choice == "2":
        if len(messages) == 0:
            print("No messages yet.")
        else:
            print("\nMessages:")
            for m in messages:
                print(m)

    elif choice == "3":
        print("Goodbye!")
        break

    else:
        print("Invalid choice.")
