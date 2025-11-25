# python-project
class Account:
    def __init__(self, name, balance):
        self.name = name
        self.balance = balance

    def deposit(self, amt):
        self.balance += amt #new balance = old balance + deposit amount
        print(f"Deposited {amt}. New Balance = {self.balance}")

    def withdraw(self, amt):
        if amt <= self.balance:
            self.balance -= amt
            print(f"Withdrawn {amt}. New Balance = {self.balance}")
             else:
            print("Insufficient Balance")

class SavingsAccount(Account):   # Inheritance
    def interest(self):
        self.balance += self.balance * 0.05
        print("Interest added:", self.balance)


s = SavingsAccount("iam", 5000)
s.deposit(1000)
s.withdraw(2000)
s.interest()


