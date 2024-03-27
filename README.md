# Registration-form-using-Python
class UserRegistration:
    def __init__(self):
        self.users = {}

    def register(self, name, rollno, email, password):
        if email in self.users:
            print("User already registered with this email.")
            return False
        self.users[email] = {'Name': name, 'Roll No': rollno, 'Password': password}
        print("Registration successful.")
        return True

    def login(self, email, password):
        if email in self.users and self.users[email]['Password'] == password:
            print("Login successful.")
            return True
        else:
            print("Invalid email or password.")
            return False

    def display_details(self, email):
        if email in self.users:
            user_info = self.users[email]
            print("User Details:")
            for key, value in user_info.items():
                print(f"{key}: {value}")
        else:
            print("User not found.")

    def logout(self):
        print("Logged out successfully.")

UserRegistration = UserRegistration()
UserRegistration.register("jithin", "20", "jithin@example.com", "password12345")
UserRegistration.register("jithin", "20", "jithin@example.com", "password12345")
#UserRegistration.login("jithin@example.com", "password12345")
UserRegistration.display_details("jithin@example.com")
UserRegistration.logout()
