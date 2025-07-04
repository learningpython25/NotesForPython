**Goal:**

* There are different types of **accounts** (`SavingsAccount`, `CheckingAccount`)
* Each account has **transactions** and uses a **TransactionManager** to process them
* The system should keep track of **total accounts** created
* It should support comparisons, readable representations, and some operator overloading

---

### Complete Code Example

```python
from abc import ABC, abstractmethod

# ---------- Transaction Manager using Composition ----------
class TransactionManager:
    @staticmethod
    def validate(amount):
        return amount > 0

    def process(self, account, amount, operation):
        if operation == "deposit":
            if self.validate(amount):
                account._balance += amount
        elif operation == "withdraw":
            if self.validate(amount) and amount <= account._balance:
                account._balance -= amount

# ---------- Base Account Class ----------
class Account(ABC):
    bank_name = "Global Bank"
    account_count = 0  # class variable

    def __init__(self, owner, balance=0):
        self.owner = owner
        self._balance = balance  # "protected" instance variable
        self.tx_manager = TransactionManager()
        Account.account_count += 1

    @abstractmethod
    def account_type(self):
        pass

    @classmethod
    def total_accounts(cls):
        return cls.account_count

    @staticmethod
    def bank_info():
        return f"Welcome to {Account.bank_name}!"

    def deposit(self, amount):
        self.tx_manager.process(self, amount, "deposit")

    def withdraw(self, amount):
        self.tx_manager.process(self, amount, "withdraw")

    def __str__(self):
        return f"{self.account_type()} - {self.owner}: ${self._balance}"

    def __eq__(self, other):
        return self._balance == other._balance

    def __add__(self, other):
        return self._balance + other._balance

# ---------- Inherited Account Types ----------
class SavingsAccount(Account):
    def account_type(self):
        return "Savings Account"

class CheckingAccount(Account):
    def account_type(self):
        return "Checking Account"

# ---------- Usage ----------
acc1 = SavingsAccount("Alice", 500)
acc2 = CheckingAccount("Bob", 300)

acc1.deposit(200)
acc2.withdraw(100)

print(acc1)  # Savings Account - Alice: $700
print(acc2)  # Checking Account - Bob: $200

print("Equal?", acc1 == acc2)      # False
print("Combined balance:", acc1 + acc2)  # 900

print(Account.bank_info())         # Static method
print("Total accounts:", Account.total_accounts())  # Class method
```

---

### Output

```
Savings Account - Alice: $700
Checking Account - Bob: $200
Equal? False
Combined balance: 900
Welcome to Global Bank!
Total accounts: 2
```

---

### Summary

| Concept                 | Shown In                                        |
| ----------------------- | ----------------------------------------------- |
| **Inheritance**         | `SavingsAccount`, `CheckingAccount` → `Account` |
| **Composition**         | `TransactionManager` inside `Account`           |
| **Magic Methods**       | `__str__`, `__eq__`, `__add__`                  |
| **Abstract Class**      | `Account(ABC)` with `@abstractmethod`           |
| **Encapsulation**       | `_balance` as "protected" attribute             |
| **Polymorphism**        | `account_type()` overridden                     |
| **Class Method**        | `total_accounts()`                              |
| **Static Method**       | `bank_info()`                                   |
| **Instance/Class Vars** | `self.owner`, `bank_name`, `account_count`      |

