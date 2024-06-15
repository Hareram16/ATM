# ATM
#creating a class as bank account
class BankAccount:
    # creating a counstructor to initialize the values
    def __init__(self,name,accouont_number,balance=0):
       # assiging the values
       self.__name=name
       self.__account_number=account_number
    # creating a function to deposit money
    def deposit (self,amount):
        self.balance+=amount
    # creating a function to withdraw money
    def withdraw(self,amount):
        if(amount<=self.balance):
            self.balance-=amount
            print("money is dibited")
        else:
            print("insufficient method")
    # creating a function to check the bank ballanace
    def get_balance(seLf):
       return self.__balance
    # now we write the function to transfer money
    def transfer (self,amount,other_account):
       if amount<self.balance:
          self.withdraw(amount)
          othr_account.deposit(amount)
       else:
          print("insufficient funds for transfer")
    # Here we write the function to get the account information of user
    def get_account_info(self):
       return f"Account holder: {self.__name}\nAccount number:{self.account_number}\nBalance:{self.__balance}"
    # writing a function to get the account number
    def get_account_nuumber(self):
       return self.__account_number
# creating a class name as ATM
class ATM:
    def __init__(self,account):
        self.account=account
    def show_menu(self):
        print("\n----ATM Menu----")
        print("1.Check Balance")
        print("2.Deposit Money")
        print("3.Withdraw Money")
        print("4.Transfer Money")
        print("5.View Account Information")
        print("6.Exist")
    def run(self):
        while True:
            self.show_menu()
            choice=input("Choice an option: ")
            if choice=='1':
                print(f"Your Balance is:{self.account.get_balance()}")
            elif chooice=='2':
                amount=float(input("Enter amount to deposit : "))
                self.account.deposit(amount)
                print(f"Deposited {amount).New balance is{self.account.get_balance()}.")
            elif choice=='3':
                amount=float(input("Enter Amount to withdraw"))
                self.account.withdraw(amount)
                print(f"Withdraw {amount}.New balance is {self.account.get_balance()}.")
            elif choice=='4':
                account_number =input("Enter account number to transfer to:")
                amount=float(input("Enter amount to transfer: ")
                # Simulate finding the other account
                other_account=BankAccount("Recipient",account_number)
                self.account.transfer(amount,other_account)
                print(f"Transferred {amount} to account {account_number}.New balance is{self.account.get_balance()}.")
            elif choice=='5':
                print(self.account.get_accou_info())
            elif choice=='6':
                print("Exiting ATM .Have a great day!")
            else:
                print("Invalid choice .Please try again.")
account =Bankaccount("Ram","852963",10000)
atm=ATm(account)
atm.run()
       
        
    
       


