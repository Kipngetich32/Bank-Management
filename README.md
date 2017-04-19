# Bank-Management-Sytem
#Its a simple CLI bank Management Program with Python
class BankAccount(object):
    def __init__(self):
        pass
    def deposit (self):
        pass
    def withdraw (self):
        pass
class SavingsAccount(BankAccount):
    def __init__(self):
        self.balance= 500

    def deposit (self, amount):
        if (amount<0):
            print ('Invalid deposit amount' )
        else:
            self.balance+=amount
            return (self.balance)
    def withdraw (self ,amount):
        if (amount <0):
            return ('Invalid withdraw amount')
        elif (self.balance-amount)<0:
            return ('Cannot withdraw beyond the current account balance')
        elif (self.balance-amount)>0 and (self.balance-amount)<500:
            return ('Cannot withdraw beyond the minimum account balance')
        else:
            self.balance-=amount
            return (self.balance)
class CurrentAccount (BankAccount):
    def __init__(self):
        self.balance=0
    def deposit (self, amount):
        if (amount<0):
            return ('Invalid deposit amount' )
        else:
            self.balance+=amount
            return (self.balance)
    def withdraw (self ,amount):
        if (amount <0):
            return ('Invalid withdraw amount')
        elif (self.balance-amount)<0:
            return ('Cannot withdraw beyond the current account balance')
        else:
            self.balance-=amount
            return (self.balance)        
        
Savings= SavingsAccount()
Savings.deposit(500)
Savings.withdraw (600)
Savings.withdraw (400)

Current= CurrentAccount()
Current.deposit(500)
Current.withdraw (600)
Current.withdraw (400)

        
