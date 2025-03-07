# youngLA-first-project


class GymInventoryManager:
    def __init__(self):
        self.gym_clothing = {"Over sized": [], "Compression": [], "Super sized": []}
        self.supplements = {"Creatine": [], "Protein": [], "Pre-Workout": []}
        self.accessories = {"Shakers": [], "Bracelets": [], "Notebooks": []}

    
    class YoungLA_Gym_clothing:
        def __init__(self):
            self.gym_clothing = {"Over sized": [], "Compression": [], "Super sized": []}

        def add_gym_clothing(self, category, name, price, stock):
            if category in self.gym_clothing:
                self.gym_clothing[category].append({"name": name, "price": price, "stock": stock})
            else:
                print("Invalid category!")

        def display_gym_clothing(self):
            print("\nGym Clothing Inventory:")
            for category, items in self.gym_clothing.items():
                print(f"{category}:")
                for item in items:
                    print(f"  - {item['name']} (Price: ${item['price']}, Stock: {item['stock']})")

        def search_gym_clothing(self, name):
            for category, items in self.gym_clothing.items():
                for item in items:
                    if item['name'].lower() == name.lower():
                        return item
            return "Item not found"

        def update_gym_clothing(self, name, new_price, new_stock):
            for category, items in self.gym_clothing.items():
                for item in items:
                    if item['name'].lower() == name.lower():
                        item['price'] = new_price
                        item['stock'] = new_stock
                        return "Updated successfully"
            return "Item not found"

        def remove_gym_clothing(self, name):
            for category, items in self.gym_clothing.items():
                for item in items:
                    if item['name'].lower() == name.lower():
                        items.remove(item)
                        return "Removed successfully"
            return "Item not found"

    class Supplements_manager:
        def __init__(self):
            self.supplements = {"Creatine": [], "Protein": [], "Pre-Workout": []}

        def add_supplement(self, category, name, flavor, price, stock):
            if category in self.supplements:
                self.supplements[category].append({"name": name, "flavor": flavor, "price": price, "stock": stock})
            else:
                print("Invalid category!")

        def display_supplements(self):
            print("\nSupplement Inventory:")
            for category, items in self.supplements.items():
                print(f"{category}:")
                for item in items:
                    print(f"  - {item['name']} ({item['flavor']} flavor) (Price: ${item['price']}, Stock: {item['stock']})")

        def search_supplement(self, name):
            for category, items in self.supplements.items():
                for item in items:
                    if item['name'].lower() == name.lower():
                        return item
            return "Item not found"

        def update_supplement(self, name, new_price, new_stock):
            for category, items in self.supplements.items():
                for item in items:
                    if item['name'].lower() == name.lower():
                        item['price'] = new_price
                        item['stock'] = new_stock
                        return "Updated successfully"
            return "Item not found"

        def remove_supplement(self, name):
            for category, items in self.supplements.items():
                for item in items:
                    if item['name'].lower() == name.lower():
                        items.remove(item)
                        return "Removed successfully"
            return "Item not found"

    

    class Acessory_manager:
        def __init__(self):
            self.accessories = {"Shakers": [], "Bracelets": [], "Notebooks": []}

        def add_accessory(self, category, name, price, stock):
            if category in self.accessories:
                self.accessories[category].append({"name": name, "price": price, "stock": stock})
            else:
                print("Invalid category!")

        def display_accessories(self):
            print("\nAccessories Inventory:")
            for category, items in self.accessories.items():
                print(f"{category}:")
                for item in items:
                    print(f"  - {item['name']} (Price: ${item['price']}, Stock: {item['stock']})")

        def search_accessory(self, name):
            for category, items in self.accessories.items():
                for item in items:
                    if item['name'].lower() == name.lower():
                        return item
            return "Item not found"

        def update_accessory(self, name, new_price, new_stock):
            for category, items in self.accessories.items():
                for item in items:
                    if item['name'].lower() == name.lower():
                        item['price'] = new_price
                        item['stock'] = new_stock
                        return "Updated successfully"
            return "Item not found"

        def remove_accessory(self, name):
            for category, items in self.accessories.items():
                for item in items:
                    if item['name'].lower() == name.lower():
                        items.remove(item)
                        return "Removed successfully"
            return "Item not found"
