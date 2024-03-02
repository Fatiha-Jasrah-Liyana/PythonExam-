class NIDManagementSystem:
    def __init__(self):
        self.nid_numbers = []

    def add_nid_number(self, nid):
        self.nid_numbers.append(nid)

    def display_nid_numbers(self):
        if self.nid_numbers:
            print("List of NID Numbers:")
            for nid in self.nid_numbers:
                print("-", nid)
        else:
            print("No NID Numbers found.")

    def delete_nid_number(self, nid):
        if nid in self.nid_numbers:
            self.nid_numbers.remove(nid)
            print("NID Number", nid, "deleted successfully.")
        else:
            print("NID Number", nid, "not found.")

    def update_nid_number(self, old_nid, new_nid):
        if old_nid in self.nid_numbers:
            index = self.nid_numbers.index(old_nid)
            self.nid_numbers[index] = new_nid
            print("NID Number", old_nid, "updated to", new_nid)
        else:
            print("NID Number", old_nid, "not found.")


if __name__ == "__main__":
    nid_system = NIDManagementSystem()

    nid_system.add_nid_number("123456789")
    nid_system.add_nid_number("987654321")

    nid_system.display_nid_numbers()

    nid_system.delete_nid_number("123456789")

    nid_system.update_nid_number("987654321", "111222333")
    
    nid_system.display_nid_numbers()
