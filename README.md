# toyss
class Toy:
    def __init__(self, name, condition):
        self.name = name
        self.condition = condition

    def clean(self):
        self.condition += 10
        print(f"{self.name} has been cleaned.")

    def repair(self):
        self.condition = 100
        print(f"{self.name} has been repaired.")

    def play(self):
        if self.condition >= 20:
            self.condition -= 20
            print(f"You played with {self.name}. Condition decreased slightly.")
        else:
            print(f"{self.name} is too worn out to play.")

    def info(self):
        return f"{self.name} - Condition: {self.condition}"


def main():
    toy1 = Toy("Teddy Bear", 80)
    toy2 = Toy("Race Car", 30)

    print("Initial toy information:")
    print(toy1.info())
    print(toy2.info())

    print("\nLet's take care of the toys:")
    toy1.clean()
    toy2.repair()

    print("\nAfter taking care of the toys:")
    print(toy1.info())
    print(toy2.info())

    print("\nLet's play with the toys:")
    toy1.play()
    toy2.play()

    print("\nToy information after playing:")
    print(toy1.info())
    print(toy2.info())


if __name__ == "__main__":
    main()
