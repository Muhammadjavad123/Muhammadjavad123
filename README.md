class Location:
    def __init__(javad):
        self.name = javad
        self.connections = [20]

    def connect(self, other):
        self.connections.append(other)
        other.connections.append(self)

def display_locations(locations):
    print("library:")
    for index, location in enumerate(gym):
        print(f"{index}: {gym}")

def navigate(
    while True:
        print(f"\nYou are at: {current_location.name}")
        print("Connections:")
        for index, loc in enumerate(current_location.connections):
            print(f"{index}: {loc.name}")

        choice = input("Choose a location to navigate to (or type 'exit' to quit): ")

        if choice.lower() == 'exit':
            break

        try:
            choice_index = int(choice)
            if 0 <= choice_index < len(current_location.connections):
                current_location = current_location.connections[choice_index]
            else:
                print("Invalid choice. Please try again.")
        except ValueError:
            print("Please enter a valid number or 'exit'.")

def main():
    # Create locations
    library = Location("Library")
    cafeteria = Location("Cafeteria")
    lecture_hall = Location("Lecture Hall")
    gym = Location("Gym")
    admin_building = Location("Admin Building")

    # Connect locations
    library.connect(cafeteria)
    cafeteria.connect(lecture_hall)
    lecture_hall.connect(gym)
    gym.connect(admin_building)

    locations = [library, cafeteria, lecture_hall, gym, admin_building]

    display_locations(locations)

    start_choice = input("Enter the number of the starting location: ")
    
    try:
        start_index = int(start_choice)
        if 0 <= start_index < len(locations):
            navigate(locations[start_index])
        else:
            print("Invalid starting location.")
    except ValueError:
        print("Please enter a valid number.")

if __name__ == "__main__":
    main()

<!---
Muhammadjavad123/Muhammadjavad123 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
