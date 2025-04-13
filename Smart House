
# Smart House System using OOP

class Device:
    def __init__(self, name):
        self.name = name
        self.status = "OFF"

    def turn_on(self):
        self.status = "ON"
        print(f"{self.name} is now ON.")

    def turn_off(self):
        self.status = "OFF"
        print(f"{self.name} is now OFF.")

    def get_status(self):
        return f"{self.name} status: {self.status}"


class Light(Device):
    def __init__(self, location):
        super().__init__(f"{location} Light")


class Fan(Device):
    def __init__(self, location):
        super().__init__(f"{location} Fan")


class AirConditioner(Device):
    def __init__(self, location, temperature=24):
        super().__init__(f"{location} Air Conditioner")
        self.temperature = temperature

    def set_temperature(self, temp):
        self.temperature = temp
        print(f"{self.name} temperature set to {self.temperature}°C")


class SecuritySystem(Device):
    def __init__(self):
        super().__init__("Security System")

    def activate(self):
        self.status = "ARMED"
        print("Security System is now ARMED.")

    def deactivate(self):
        self.status = "DISARMED"
        print("Security System is now DISARMED.")


class SmartHome:
    def __init__(self):
        self.devices = []

    def add_device(self, device):
        self.devices.append(device)

    def show_all_statuses(self):
        print("\nSmart Home Device Status:")
        for device in self.devices:
            print(device.get_status())


# Example usage
if __name__ == "__main__":
    # Create smart devices
    living_light = Light("Living Room")
    bedroom_fan = Fan("Bedroom")
    ac = AirConditioner("Living Room")
    security = SecuritySystem()

    # Create Smart Home system
    home = SmartHome()
    home.add_device(living_light)
    home.add_device(bedroom_fan)
    home.add_device(ac)
    home.add_device(security)

    # Use devices
    living_light.turn_on()
    bedroom_fan.turn_on()
    ac.turn_on()
    ac.set_temperature(22)
    security.activate()

    home.show_all_statuses()
