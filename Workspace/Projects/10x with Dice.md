
```python
import random

class Dice:
    @staticmethod
    def roll():
        return random.randint(1, 6)

class Player:
    def __init__(self, name):
        self.name = name
        self.score = 0
        self.last_roll = None

    def __str__(self):
        return f"{self.name}: {self.score} (Last roll: {self.last_roll})"

    def play_turn(self):
        roll = Dice.roll()
        self.last_roll = roll
        return roll

    def add_to_score(self, value):
        self.score += value

    def has_won(self, target):
        return self.score >= target

class Game:
    def __init__(self, player1, player2, target=30):
        self.players = [player1, player2]
        self.target = target
        self.turn = 0  # 0 for player1, 1 for player2

    def opposite_parity(self, roll1, roll2):
        return (roll1 % 2) != (roll2 % 2)

    def start(self):
        print("🎯 Welcome to Reach 10x with Dice!\n")
        while True:
            current = self.players[self.turn]
            opponent = self.players[1 - self.turn]

            print(f"\n{current.name}'s turn:")
            roll = current.play_turn()
            print(f"{current.name} rolled a {roll}")

            if opponent.last_roll is None:
                print("✅ First turn, score added.")
                current.add_to_score(roll)
            elif self.opposite_parity(roll, opponent.last_roll):
                print("✅ Opposite parity! Score added.")
                current.add_to_score(roll)
            else:
                print("❌ Same parity! No score this turn.")

            print(current)
            print(opponent)

            if current.has_won(self.target):
                print(f"\n🏆 {current.name} wins with a score of {current.score}!")
                break

            self.turn = 1 - self.turn  # Switch turn

# --- Runner ---
name1 = input("Enter Player 1 name: ")
name2 = input("Enter Player 2 name: ")

p1 = Player(name1)
p2 = Player(name2)

game = Game(p1, p2)
game.start()


```


