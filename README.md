vehicles = [] 


def log_vehicles(): 
    plate = input("Enter Vehicle Plate Number : ")
    time_in = input("Enter Time-In (e.g. 7:30 AM) : ")

    if plate =="" or time_in =="" :
     print("\nNo Vehicle Information Logged\n")
    else:
     vehicles.append({"plate": plate, "time_in": time_in})
     print("\nVehicle Logged Successfully!\n")

    
def view_vehicles():
    if len(vehicles) == 0:
        print("\nNo Vehicles Logged Yet\n")
    else:
        print("\n--- Vehicle List ---\n")
        for v in vehicles :
            print("Plate: " + v["plate"] + ", Time-in: " + v["time_in"])
        print()

def generate_report():
    print("\n--- Vehicles Report ---\n")
    print("Total Vehicles Logged: " + str (len(vehicles)) + "\n")


while True:
    print("\n==== Vehicle Parking Log System ====\n")
    print("[1] Log Vehicle Parking Attendant")
    print("[2] View Vehicles Security Supervisor")
    print("[3] Generate Report Security Supervisor")
    print("[4] Exit")

    choice = input("\nEnter Choice Number : ")

    if choice == "1":
        log_vehicles()
    elif choice == "2":
        view_vehicles()
    elif choice == "3":
        generate_report()
    elif choice == "4":
        print("Thank you! Have a Great Day.")
        break
    else:
        print("\nInvalid Choice. Please Try Again.\n")
